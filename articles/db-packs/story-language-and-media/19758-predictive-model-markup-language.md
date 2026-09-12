# Predictive Model Markup Language

The Predictive Model Markup Language (PMML) is an XML-based format for describing and exchanging predictive models produced by data mining and machine learning algorithms. A tool exports a trained model as a PMML file, and another tool loads and runs it without retraining or rewriting the model. PMML was conceived by Robert Lee Grossman, then director of the National Center for Data Mining at the University of Illinois at Chicago, and first published as version 0.9 in 1998. The Data Mining Group (DMG), a consortium managed by the nonprofit Center for Computational Science Research, Inc., founded in 2008, has developed subsequent versions. The current release is 4.4 (November 2019), and over 30 organisations have announced PMML-supporting products.

Because PMML is an XML standard, the specification itself is an XML schema. A PMML document is built from a small set of components that together describe a model: the fields it expects, how raw inputs are reshaped, what algorithm it uses, which fields play which role, and what the output should look like.

## Components of a PMML document

**Header.** General metadata: copyright, description, the application and version that produced the model, and a creation timestamp.

**Data Dictionary.** Definitions for every field the model could use. Each field carries an *optype* (operational type) marking it continuous, categorical, or ordinal, together with its data type (string, double, etc.) and its allowed value range.

**Data Transformations.** Mappings that reshape user data into the form the model expects:
- *Normalization*: map values to numbers; input may be continuous or discrete.
- *Discretization*: map continuous values to discrete values.
- *Value mapping*: map discrete values to other discrete values.
- *Functions*: derive a value by applying a built-in or custom function to parameters.
- *Aggregation*: summarise or collect groups of values.

**Model.** The definition of the mining algorithm itself. A multi-layer feedforward neural network, for example, is represented by a `NeuralNetwork` element with attributes for model name, function name, algorithm name, activation function, and number of layers, followed by three layer kinds — `NeuralInputs`, `NeuralLayer`, and `NeuralOutputs` — that fix the architecture. PMML also supports support vector machines, association rules, Naive Bayes classifiers, clustering models, text models, decision trees, and several regression models.

**Mining Schema.** The subset of fields from the data dictionary that the model actually uses. Each entry declares its name, its *usage type* (`active`, `predicted`, or `supplementary`), how outliers are handled (as missing, as extreme values, or as-is), and how missing values are replaced (literal, mean, or median).

**Targets.** Post-processing of the predicted value, including scaling for continuous outputs and, for classification, a `priorProbability` that supplies a default probability for a target category when the prediction logic produced no result.

**Output.** Names the desired output fields: predicted value, probability, cluster affinity for clustering models, standard error, and similar features. PMML 4.1 extended `Output` so the built-in and custom functions previously limited to pre-processing could also post-process results.

## Version history

PMML's first ten years produced incremental0.x through 3.2 releases (July 1997 to May 2007). The four 4.x releases then introduced most of the modern feature set:

- **4.0** (June 2009): Boolean and If-Then-Else pre-processing functions; time-series models including exponential smoothing, with placeholders for ARIMA, seasonal trend decomposition, and spectral density estimation; saving evaluation and performance measures inside the PMML file; model composition, ensembles, and segmentation; multi-class classification for SVMs; richer association rules; Cox regression models.
- **4.1** (December 2011): Scorecards, k-Nearest Neighbors, and baseline models; a unified representation for segmentation, ensembles, and chaining; explicit field scope and names; an attribute marking whether a model is ready for production; enhanced `Output` post-processing.
- **4.2** (February 2014): text-mining transformations; built-in regular-expression functions (`matches`, `concat`, `replace`); simplified post-processing outputs; scorecard and Naive Bayes enhancements. A 4.2.1 patch followed in March 2015.
- **4.3** (August 2016): Gaussian process and Bayesian network model types, new built-in functions, and documentation improvements.
- **4.4** (November 2019): the current release.

## Related standards

The DMG also developed the Portable Format for Analytics (PFA), a complementary standard that targets the same problem of moving analytic models between systems from a different design point. The Open Neural Network Exchange is a separate, neural-network-focused sibling standard.

PMML's practical value is the round-trip: a model trained in one tool can be exported and scored by another because the schema captures not just the algorithm and its weights but the surrounding metadata — field types, transformations, missing-value handling, outlier treatment, and post-processing.

Source: adapted from "Predictive Model Markup Language" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Predictive_Model_Markup_Language
