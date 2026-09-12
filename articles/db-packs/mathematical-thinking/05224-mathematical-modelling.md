# Mathematical modelling

A mathematical model is an abstract description of a real system using mathematical concepts and language. The process of building one is called mathematical modelling, used across the natural sciences, social sciences, engineering, and applied mathematics. A model clarifies how a system's components behave and supports predictions or problem solving. In the physical sciences, a model usually combines governing equations, defining equations, constitutive equations, assumptions, and initial and boundary conditions. Quality depends on how closely models match repeatable experiments; persistent disagreement drives new theories.

## Classifications

Mathematical models sort along several axes, and one model can belong to several at once.

**Linear vs. nonlinear.** A model is linear if its operators are linear; otherwise nonlinear. A statistical linear model is linear in parameters but may be nonlinear in predictor variables. A differential equation is linear if written with linear differential operators. Linear structure lets a problem be decomposed, recombined, or rescaled while the result stays valid. Nonlinearity is associated with chaos and irreversibility and is harder to analyse; linearisation is common but can hide exactly those phenomena.

**Static vs. dynamic.** Static (steady-state) models treat a system in equilibrium, with no time dependence. Dynamic models account for time-dependent change and are usually written as differential or difference equations.

**Explicit vs. implicit.** If known inputs yield outputs through a finite sequence of computations, the model is explicit. When outputs are known and inputs must be recovered iteratively, the model is implicit. A jet engine's physical dimensions can be computed explicitly for one design cycle, but its behaviour at other flight conditions must be solved implicitly.

**Discrete vs. continuous.** Discrete models treat objects as countable items, such as particles or states. Continuous models use fields, like the velocity of fluid in a pipe or the temperature in a solid.

**Deterministic vs. stochastic.** A deterministic model gives the same output for the same initial conditions; a stochastic one produces probability distributions because randomness is built in.

**Deductive, inductive, or floating.** A deductive model rests on theory, an inductive model generalises from data, and a "floating" model rests on neither. Critics have applied that label to catastrophe theory in science and to some uses of mathematics in the social sciences.

**Strategic vs. non-strategic.** Game-theoretic models treat agents with conflicting incentives, such as competing species or auction bidders. They assume rational players maximising an objective function, with solution concepts like the Nash equilibrium, and separate the rules of the game from the behaviour of the players.

## Building a model

In business and engineering, models often maximise an output given certain inputs. The system links inputs to outputs through decision variables, state variables, exogenous variables (sometimes called parameters), and random variables. State variables depend on the others, and outputs depend on the state. Objectives and constraints are written as functions of the outputs or states; an objective function is also called an index of performance. More objectives and constraints raise computational cost, and complex models are often compacted with vectors.

How much a modeller already knows divides problems into black-box, white-box, and the realistic middle between them. White-box models use all available a priori information; black-box models use none. Even in a partly white-box problem, such as the exponentially decaying concentration of a drug in the blood, unknown parameters still need estimation. Black-box approaches estimate both the functional form and parameters; neural networks are a common example, and NARMAX (Nonlinear AutoRegressive Moving Average with eXogenous inputs) is an alternative that produces transparent equations rather than opaque approximations.

Subjective information can be incorporated through Bayesian statistics by specifying a prior distribution and updating it with data. A bent coin flipped once illustrates the point: the true heads probability is unknown, so the analyst chooses a prior informed by the coin's shape.

## Complexity, training, and fitting

Model building trades simplicity against accuracy, formalised by Occam's razor: among models with similar predictive power, the simplest is best. Adding detail, such as embedding every mechanical part of an aircraft, raises computational cost and uncertainty. Engineers accept approximations, and Newton's classical mechanics is a deliberately approximate model, valid at everyday speeds and for macroscopic objects but failing near the speed of light or at molecular scales. Statistical models can also overfit, matching training data so closely that they lose the ability to generalise.

In machine learning, fitting parameters is called training, while tuning selects hyperparameters, often through cross-validation. In conventional modelling, parameters are set by curve fitting.

## Evaluation

The simplest check is whether the model predicts empirical data it was not built on. A standard practice splits data into a training set, which sets parameters, and a verification set, which tests them. A metric or loss function quantifies the gap between observation and prediction. More tools exist for testing statistical models than for testing differential-equation models, and nonparametric statistics can sometimes fit a distribution with minimal assumptions.

Assessing scope, the range of situations a model applies to, is harder. Fit between data points is interpolation; outside them, it is extrapolation. Newtonian mechanics does not extrapolate to near-light speeds or to single molecules.

Models also carry implicit claims about causality, especially when written as differential equations. A model is judged not only by fit but by whether it extrapolates and whether it offers insight beyond direct observation; optimal foraging theory has been criticised on exactly that ground. Mathematical modelling uses mathematical concepts but is not itself a branch of mathematics; it follows the argumentative standards of the science or technical field it serves.

## Models in the natural sciences

Physical theories are almost always expressed mathematically. Newton's laws work for everyday phenomena, but relativity and quantum mechanics take over at their respective limits. Physicists work with idealised models such as massless ropes, point particles, ideal gases, and the particle in a box, then use basic laws like Newton's laws, Maxwell's equations, and the Schrödinger equation to build computational approximations of complex situations, as with molecular orbital models and finite element analysis in engineering. Classical physics uses Euclidean geometry, while special and general relativity use non-Euclidean ones.

## A representative example

A simple illustration is dead reckoning: predicting a vehicle's position from its initial location, direction, and speed, using distance = speed × time. The same idea scales to planetary motion modelled as a point mass in a potential field, where the trajectory r(t) satisfies m d²r/dt² = −∇V[r(t)]. The point-mass assumption is known to be false, but the model remains useful within its scope.
