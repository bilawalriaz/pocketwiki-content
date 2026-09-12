# Arithmetic mean

The arithmetic mean of a collection of numbers is the sum of those numbers divided by how many there are. The term is often shortened to "mean" or "average," and used in full when a writer needs to distinguish it from other means such as the geometric or harmonic mean. Per capita income, the average earnings per person in a country, is one common application.

## The formula

For observed values $x_1, x_2, \ldots, x_n$, the arithmetic mean is

$$\bar{x} = \frac{1}{n}\sum_{i=1}^{n} x_i = \frac{x_1 + x_2 + \cdots + x_n}{n}.$$

Worked example: the monthly salaries of five employees are {2500, 2700, 2300, 2650, 2450}. Their mean salary is

$$\frac{2500 + 2700 + 2300 + 2650 + 2450}{5} = 2520.$$

When the data describe an entire statistical *population* (every possible observation), the mean is the population mean, written $\mu$. When the data describe a *sample* (a subset drawn from a larger population), the mean is the sample mean, written $\bar{x}$.

## Why the mean works

Three properties explain why the arithmetic mean is so widely used as a measure of central tendency.

**Residuals sum to zero.** The deviations of every value from the mean cancel out exactly:

$$(x_1 - \bar{x}) + (x_2 - \bar{x}) + \cdots + (x_n - \bar{x}) = 0.$$

The numbers below the mean are balanced by the numbers above it, and the mean is the only number with this property. A related consequence is *translational invariance*: shifting every value by a constant $a$ shifts the mean by the same constant, so $\overline{x + a} = \bar{x} + a$.

**It minimises squared error.** Among all possible "typical" values, the mean is the one that minimises the sum of squared deviations $\sum (x_i - \bar{x})^2$, and it has the lowest root mean squared error of any constant estimate.

**It is independent of units.** Multiplying every value by a constant $c$ multiplies the mean by the same constant: $\text{avg}(c\,a_1, \ldots, c\,a_n) = c \cdot \text{avg}(a_1, \ldots, a_n)$. Converting litres to gallons after averaging gives the same result as converting before averaging, a property called first-order homogeneity.

Two by-products follow. The mean of a sample always lies between the smallest and largest values, and the mean of several equal-sized groups equals the mean of the group means.

## The weakness: sensitivity to outliers

The mean is not a *robust* statistic: values much larger or smaller than the rest can throw it off badly. For skewed distributions such as personal income, where a small number of people earn vastly more than most, the mean can sit well above what anyone would call the "middle." In such cases the *median*, the value splitting the higher half of the data from the lower half, often describes central tendency better.

The two measures agree in symmetric data. In {1, 2, 3, 4} both the mean and the median are 2.5. They diverge in lopsided data: in {1, 2, 4, 8, 16} the mean is 6.2 while the median is 4, pulled upward by the extreme value 16. The same divergence shows up in US income, where median income has grown more slowly than mean income since the 1980s because gains concentrated at the top lift the mean more than the median. Daily mean temperatures often approximate a *normal distribution*, in which mean, median, and *mode* (the most frequent value) coincide, but annual or monthly rainfall totals are usually skewed, so the median rainfall gives a more representative "typical" value.

## Generalisations

**Weighted mean.** When some observations should count more than others, each value is multiplied by a *weight*, and the weights must sum to 1. The plain arithmetic mean is the special case where every weight equals $1/n$. For instance, the mean of 3 and 5 is 4. Giving 3 twice the weight of 5 yields

$$3 \cdot \tfrac{2}{3} + 5 \cdot \tfrac{1}{3} = \tfrac{11}{3} \approx 3.67.$$

**Probability distributions.** When a variable takes any value in a continuous range, the mean of the corresponding *probability distribution* is the analogue of a weighted average, computed by integrating the value against its probability density. For the normal distribution this mean equals both the median and the mode. For skewed distributions such as the log-normal, the three diverge.

**Angles and cyclic data.** The ordinary arithmetic mean fails for cyclic quantities. Averaging 1° and 359° gives 180°, the worst summary, since both points sit only 1° from 0° but 179° from 180°. Angles are defined only up to a full turn (360° or $2\pi$ radians), so a circular mean must measure distance around the circle rather than along a line. The same caveat applies to any cyclic quantity, such as phases of the moon or times of day.

**Vectors and beyond.** The arithmetic mean of points in multiple dimensions is their *centroid*. Because it is a *convex combination* (the coefficients sum to 1), the construction generalises to any convex space, not just flat vector spaces.

Source: adapted from "Arithmetic mean" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Arithmetic_mean
