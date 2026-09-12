# Trigonometry

Trigonometry is the branch of mathematics that links angles to side lengths in triangles. The name comes from Greek words meaning "triangle measure." At its core are six ratios, called trigonometric functions, that take an angle and return a number; from these ratios, plus a handful of universal identities, you can recover any unknown side or angle in any triangle, model waves, and reason about anything circular or oscillating.

## The six functions from a right triangle

Start with a right triangle containing angle A. The side opposite A is *a*, the side next to A (not the hypotenuse) is *b*, and the longest side, opposite the 90° angle, is the hypotenuse *h*. Any two right triangles that share angle A are similar, so the ratios between their sides are identical: the ratios depend only on A, not on the triangle's size. Three primary ratios:

- **Sine**: sin A = a / h (opposite over hypotenuse)
- **Cosine**: cos A = b / h (adjacent over hypotenuse)
- **Tangent**: tan A = a / b = sin A / cos A

The remaining three are reciprocals: **cosecant** csc = h/a, **secant** sec = h/b, and **cotangent** cot = b/a = cos/sin. The "co-" prefix signals that each is the sine, tangent, or secant of the complementary angle (the one that sums with A to give 90°). A common mnemonic is **SOH-CAH-TOA**.

Because these definitions rely on a right angle, they cover only acute angles. To handle any angle, drop the triangle and use the **unit circle**, a circle of radius 1 centred at the origin. Place angle A in standard position (vertex at the origin, one side along the positive x-axis) and read off where the other side meets the circle: the point is (cos A, sin A). This extends sine and cosine to every real number, positive or negative.

## Laws for any triangle

The right-triangle ratios alone cannot solve a triangle that has no right angle. Three identities fill the gap, and they work for any triangle with sides a, b, c opposite angles A, B, C:

- **Law of sines**: a/sin A = b/sin B = c/sin C = 2R, where R is the radius of the circumscribed circle. The common value also equals abc / (2Δ), where Δ is the triangle's area.
- **Law of cosines**: c² = a² + b² − 2ab cos C. This is the Pythagorean theorem with a correction term, and it reduces to c² = a² + b² when C = 90° (cos 90° = 0).
- **Law of tangents**: (a − b)/(a + b) = tan[½(A − B)] / tan[½(A + B)]. François Viète developed this as a shortcut that was easier to evaluate with the trigonometric tables of his era.

Together with the area formula Δ = ½ ab sin C, these laws let you compute any missing side or angle given just two sides and the included angle, two angles and a side, or all three sides.

The most basic identities come straight from the unit circle. Because every point on it satisfies x² + y² = 1, and x = cos A, y = sin A, we get sin²A + cos²A = 1. Dividing by cos²A gives tan²A + 1 = sec²A; dividing by sin²A gives cot²A + 1 = csc²A. These Pythagorean identities hold for every angle.

## Inverse functions and complex numbers

The six functions are periodic: sine and cosine repeat every 360°, tangent every 180°, so each output comes from infinitely many inputs. That makes them non-injective and non-invertible as written. Restricting the domain (for example, sine to −90° to 90°) yields a unique inverse; these are the inverse trigonometric functions, written arcsin, arccos, arctan, and so on.

Sine and cosine also have power-series expansions around zero: sin x = x − x³/3! + x⁵/5! − ⋯ and cos x = 1 − x²/2! + x⁴/4! − ⋯. These Maclaurin series extend the functions to complex arguments, and they encode **Euler's formula** e^(ix) = cos x + i sin x, which gives sin x and cos x in terms of the exponential function and the imaginary unit i. For real x, e^(x+iy) = e^x(cos y + i sin y).

## A short history

Trigonometry grew out of astronomy. In the 3rd century BC, Euclid and Archimedes proved results equivalent to modern trigonometric formulae. Around 140 BC, Hipparchus of Nicaea compiled the first tables of chords, where chord length was the Greek stand-in for sine. In the 2nd century AD, Ptolemy's *Almagest* contained chord tables so accurate they remained standard for about 1200 years. In the 5th century AD the modern sine definition appeared in the Indian *Surya Siddhanta*; in 830 AD Habash al-Hasib al-Marwazi produced the first cotangent table. By the 10th century, Abū al-Wafā' al-Būzjānī was using all six functions and sine tables to 8 decimal places at 0.25° increments. In the 13th–14th centuries, Nasir al-Din al-Tusi made trigonometry a discipline independent of astronomy, stated and proved the law of sines and the spherical law of tangents, and worked out six cases of right-angled spherical triangles. The word "trigonometry" was coined in 1595 by Bartholomaeus Pitiscus.

When the *Almagest* and Arabic works reached Western Europe in translation, trigonometry was so unfamiliar in 16th-century northern Europe that Copernicus devoted two chapters of *De revolutionibus orbium coelestium* to its basics. Gemma Frisius then described **triangulation**, measuring positions by chains of triangles, which is still the basis of surveying. In the 18th century, Euler tied trigonometry to complex numbers, and Brook Taylor defined the general Taylor series that underlies the Maclaurin expansions above.

## Where it shows up

Because the unit circle gives a point for every angle, sine and cosine are the natural language of anything that rotates or oscillates. Sound and light are sums of sine waves; Fourier showed that every continuous periodic function is an infinite sum of trigonometric functions, and the Fourier transform extends the idea to non-periodic signals, with applications from quantum mechanics to audio compression. In navigation, spherical trigonometry historically located stars, planets, and ships at sea, and the geometry still underlies GPS. In surveying, triangulation maps landmarks by measuring angles between them. Historically important but now rarely used are the chord (crd θ = 2 sin(θ/2)), versine (1 − cos θ), coversine, haversine, and exsecant, all expressible in terms of the six main functions. Modern calculators offer degrees, radians, and sometimes gradians; programming languages expose the functions as library calls; PC processors have dedicated floating-point instructions for them.
