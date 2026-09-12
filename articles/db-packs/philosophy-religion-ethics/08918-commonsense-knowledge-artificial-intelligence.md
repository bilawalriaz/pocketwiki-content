# Commonsense knowledge (artificial intelligence)

In artificial intelligence, commonsense knowledge is the background of everyday facts that all humans are expected to know, such as "lemons are sour" or "cows say moo." Acquiring and reasoning over this knowledge is currently an unsolved problem in artificial general intelligence. The first AI program to address it was John McCarthy's Advice Taker in 1959.

A commonsense knowledge base can be paired with a natural language processing layer to answer questions about the world, and with a commonsense reasoning layer to draw plausible inferences, for example inferring "you might bake a cake" from "you want people to eat the cake."

## Default reasoning and belief revision

A practical use of commonsense knowledge is filling gaps in incomplete information. Because everyone knows "typically birds fly," an AI told "Tweety is a bird" can assume "Tweety can fly" with no other evidence. Such assumptions are expressed as rules like "Normally P holds" or "Usually P, so assume P."

A truth maintenance system records every assumption and its dependencies, allowing the program to revise its beliefs when new facts arrive. Learning later that "Tweety is a penguin" triggers automatic revision, since the system also knows "penguins do not fly." Truth maintenance doubles as an explanation facility: the dependency records show why any conclusion was drawn, which matters for explainable AI.

Human-level commonsense reasoning remains far beyond current systems. Benchmarks such as the Winograd Schema Challenge expose this gap, with machines performing extremely poorly compared with people. Many researchers treat commonsense reasoning as AI-complete, meaning that solving it would require fully human-level intelligence, though some argue compassionate intelligence is also required. Commonsense reasoning has nevertheless been applied successfully in narrower domains such as natural language processing and automated diagnosis.

## Building commonsense knowledge bases

A central engineering effort is commonsense knowledge base (CSKB) construction. Early projects such as Cyc and WordNet were expert-curated. The crowdsourced OpenMind Commonsense project then produced ConceptNet, a large multilingual graph of everyday assertions. Newer systems automate extraction: WebChild, Quasimodo, TransOMCS, and Ascent mine the web, while AutoTOMIC harvests assertions directly from pre-trained language models. These resources are larger than ConceptNet but tend to be of moderately lower quality because they rely on automated rather than human judgement.

Most CSKBs store assertions as triples of the form X relation Y. A triple works well for simple facts like "rabbit HasA tail" but is awkward for richer natural language statements. GenericsKB sidesteps this by storing full unnormalised sentences. As an example, ConceptNet defines roughly 21 language-independent relations, including IsA ("RV is a vehicle"), UsedFor, HasA, Causes, HasPrerequisite, and MotivatedByGoal, covering what things are, what they are for, what they cause, and how their typical events unfold.

## Applications

Around 2013, MIT researchers built BullySpace, an extension of ConceptNet containing over 200 stereotype-based semantic assertions, to flag taunting social media comments. By drawing on commonsense gender associations, the system could recognise that phrases like "put on a wig and lipstick and be who you really are" are more likely to be insults when directed at a boy than a girl. ConceptNet has also powered chatbots and helped computers compose original fiction. At Lawrence Livermore National Laboratory, a commonsense-enabled intelligent software agent detected violations of the comprehensive nuclear test ban treaty.
```
