# Boosting (machine learning)

In machine learning, **boosting** is an ensemble method that builds one highly accurate model by sequentially training many less accurate ones, each correcting the mistakes of the ones before it. A "weak learner" is a classifier that performs only slightly better than random guessing; boosting turns many weak learners into one "strong learner" that closely matches the true answer. Unlike bagging, which trains models in parallel, boosting trains them one after another, which lets it reduce **bias** in particular. Boosting is supervised and works for both classification and regression.

The theory begins with a 1988–1989 question by Kearns and Valiant: can a set of weak learners be combined into a single strong learner? Robert Schapire answered yes in 1990, and with Yoav Freund later produced **AdaBoost**, the first adaptive boosting algorithm and still the standard teaching example. AdaBoost won the Gödel Prize.

## How boosting works

A typical boosting algorithm loops over rounds. In each round it trains a weak learner on the current weighted training set, measures that learner's error, gives the learner a weight tied to its accuracy, and reweights the data: misclassified examples gain weight, correctly classified ones lose weight. The next weak learner therefore focuses more on the previously missed examples. After all rounds, the final prediction is a weighted sum of every weak learner, with more accurate learners contributing more.

Most modern algorithms are *adaptive*, letting later learners depend on earlier ones. The **AnyBoost** framework shows that boosting performs gradient descent in function space under a convex cost function, which is why many later methods carry names like *LogitBoost*, *BrownBoost*, *LPBoost*, and *MadaBoost*. Practical systems today are often built on **gradient boosting** implementations such as XGBoost and CatBoost.

## Convex versus non-convex boosting

AdaBoost and LogitBoost minimise a convex loss, and in 2008 Long and Servedio showed this makes them vulnerable to random classification noise, so that on certain learnable target functions they can fail. By 2009, several authors showed that switching to a non-convex objective, as in BrownBoost, lets a booster fit such noisy data and recover the underlying rule.

## Application: object categorisation in images

Object categorisation, deciding whether an image contains a given kind of object, is hard because one category can look very different under changing viewpoint, scale, lighting, and occlusion. Simple classifiers built from a single image feature tend to be weak. Boosting fits naturally: a large pool of cheap features becomes a supply of weak learners, and the algorithm picks and combines them into one detector.

In the **binary** case, Viola and Jones used AdaBoost on a huge set of simple image features to build a face detector. After boosting, a classifier built from 200 features reached a 95% true-positive rate at a false-positive rate of 10⁻⁵. The same recipe, motion features plus appearance features, was the first pedestrian detector to combine both.

In the **multi-class** case, the algorithm encourages features shared across many categories, which generalises better from less data and needs fewer features overall. Torralba et al. showed with GentleBoost that, at a fixed performance level, the number of features required scales roughly **logarithmically** with the number of classes, against near-linear growth when each class is trained separately.

## Caveats

Strictly, only algorithms that are provable boosters in the PAC learning sense are boosting algorithms; other "leveraging" methods resemble boosting but lack the theoretical guarantee.

Source: adapted from "Boosting (machine learning)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Boosting_%28machine_learning%29
