# Association rule learning

Association rule learning is a rule-based machine learning method for discovering interesting co-occurrence patterns between items in large databases. The classic setting is market basket analysis: given millions of supermarket receipts, find rules of the form "{onions, potatoes} ⇒ {burger}" that tell you which items tend to be bought together. The technique, introduced by Rakesh Agrawal, Tomasz Imieliński, and Arun Swami in 1993, is now used in web usage mining, intrusion detection, bioinformatics, and medical diagnosis. Unlike sequence mining, association rule learning ignores the order of items within a transaction.

## Formal setup

Let $I = \{i_1, i_2, \ldots, i_n\}$ be a set of items and $D = \{t_1, t_2, \ldots, t_m\}$ a database of transactions, where each transaction carries a unique ID and contains a subset of $I$. A rule is an implication $X \Rightarrow Y$ with $X, Y \subseteq I$, where $X$ (the antecedent, or left-hand side, LHS) is the "if" and $Y$ (the consequent, or right-hand side, RHS) is the "then."

A naive search over all possible rules is infeasible: the candidate itemsets form the power set of $I$, with size $2^n - 1$ excluding the empty set, which grows exponentially. Practical mining therefore filters with a small set of statistical measures.

## The core measures

**Support** measures how frequently an itemset appears:

$$\text{support}(A) = \frac{\text{transactions containing } A}{\text{total transactions}}$$

For a rule, $\text{support}(X \Rightarrow Y) = P(X \cup Y)$ is the fraction of transactions containing both $X$ and $Y$. Low support means the pattern may be coincidence.

**Confidence** measures the rule's reliability, the fraction of transactions containing $X$ that also contain $Y$:

$$\text{conf}(X \Rightarrow Y) = P(Y \mid X) = \frac{\text{supp}(X \cup Y)}{\text{supp}(X)}$$

A confidence of 1.0 means the consequent appears in every transaction that has the antecedent. Confidence is an estimate of the conditional probability $P(Y \mid X)$, but it ignores the base rate of $Y$, so a high-confidence rule can still reflect a common consequent rather than a genuine association.

**Lift** corrects that weakness by comparing observed co-occurrence to what independence would predict:

$$\text{lift}(X \Rightarrow Y) = \frac{\text{supp}(X \cup Y)}{\text{supp}(X) \times \text{supp}(Y)}$$

A lift of 1 means $X$ and $Y$ are independent. A lift above 1 means positive dependence, and a lift below 1 means the items are substitutes, with one suppressing the other. For the rule {milk, bread} ⇒ {butter} in a five-transaction example, lift is $0.2 / (0.4 \times 0.4) = 1.25$, indicating modest positive dependence.

A fourth measure, **conviction**, is the ratio of the expected frequency of $X$ without $Y$ under independence to the observed frequency of incorrect predictions: $\text{conv}(X \Rightarrow Y) = (1 - \text{supp}(Y)) / (1 - \text{conf}(X \Rightarrow Y))$.

## The downward-closure property

Support is anti-monotone: if an itemset is frequent, every subset of it is also frequent. This downward-closure property lets algorithms prune the exponential search space, and is the basis for Apriori, Eclat, and FP-Growth.

## A worked example

Consider a five-transaction database with seven items: milk, bread, butter, beer, diapers, eggs, fruit. Suppose transactions 1 and 4 both contain milk and bread, and transaction 1 also contains butter. Then {milk, bread} has support 2/5 = 0.4, and {butter, bread} ⇒ {milk} has confidence (1/5) / (1/5) = 1.0, because every basket with butter and bread also contains milk. With only two supporting transactions, this perfect confidence is not statistically meaningful; a rule usually needs hundreds of occurrences before it can be trusted.

## Thresholds and the two-step process

In practice, mining is split into two steps: first, apply a minimum support threshold to find all frequent itemsets; second, apply a minimum confidence threshold to those itemsets to generate rules. Itemsets failing either threshold are discarded. Ranking by support × confidence surfaces rules that are both frequent and reliable, while lift and conviction detect rules whose strength exceeds what independence would predict.

## Major algorithms

**Apriori** (Agrawal and Srikant, 1994) uses a breadth-first, bottom-up search. It identifies frequent single items, extends them to pairs, then triples, and so on, pruning any candidate whose support falls below the threshold. Apriori is simple but can generate large candidate sets and requires $n+1$ database scans for patterns of length $n$.

**Eclat** (Zaki, 2000) uses depth-first search through the itemset lattice and represents each itemset by a transaction-id list, intersecting lists to compute support. It uses less memory than Apriori and avoids repeated scans, but its transaction-id lists can grow unwieldy on very large datasets.

**FP-Growth** (Han, 2000) compresses the database into an FP-tree, a prefix tree (a trie) over transactions built in two database passes, and mines frequent itemsets recursively from that compressed structure without generating candidates. It typically outperforms Apriori and Eclat because it scans the database only twice.

## Statistically sound associations

A practical danger is spurious rules. With 10,000 items and rules of the form "two items on the left, one on the right," roughly one trillion candidate rules exist; at a 5% significance level, a naive test would flag about 50 billion of them as "significant" by chance. Statistically sound association discovery (Webb, 2007) controls the family-wise error rate so that the probability of finding any spurious association stays below a user-chosen threshold.

Source: adapted from "Association rule learning" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Association_rule_learning
