# R (programming language)

R is a free, open-source programming language for statistical computing and data visualization. It runs an interpreted core through a command line, and most users interact with it through RStudio, Jupyter notebooks, or browser environments like Google Colab. The implementation is written mainly in C, Fortran, and R itself, and the language is licensed under the GPL.

R was created in 1993 by statisticians Ross Ihaka and Robert Gentleman at the University of Auckland, originally to teach introductory statistics. R inherits its syntax and statistical design from the older S language, and borrows Scheme's lexical scoping, the rule that a function's local variables are resolved from the function's own definition rather than from wherever the function happens to be called. Most S programs run unaltered in R. The name "R" comes from S and from the shared first letter of both authors. R became a GNU project in 1997 and reached 1.0 on 29 February 2000. The current stable release is 4.6.1, dated 24 June 2026.

R is multi-paradigm (procedural, functional, object-oriented, reflective, imperative, and array-based) with dynamic typing. Its design influenced Julia and Python's pandas library.

## Packages and the tidyverse

R's strength is its package ecosystem. A package bundles reusable functions, documentation, and sample data. Most packages are downloaded from the Comprehensive R Archive Network (CRAN), founded in 1997 by Kurt Hornik and Friedrich Leisch. As of mid-2025, CRAN hosts over 22,000 contributed packages across roughly 90 mirror sites, plus topic-grouped Task Views covering causal inference, finance, genetics, machine learning, spatial statistics, and other fields. CRAN's name and structure mirror the TeX (CTAN) and Perl (CPAN) archives. Other sources include Bioconductor (genomic data), R-Forge, Omegahat, and GitHub.

Installation happens once with `install.packages("name")`; loading into a session uses `library(name)`. The most prominent collection is the tidyverse, which bundles packages sharing a common API for importing, cleaning, transforming, and visualizing "tidy" data: tables where each row is one observation and each column is one variable.

## Syntax in practice

The preferred assignment operator is `<-`, though `=` works in some contexts. R's basic data structure is the vector, and most operations are vectorized, applying element-wise across a whole vector without explicit loops.

```
x <- 1:6          # numeric vector
y <- x^2          # element-wise squaring
z <- x + y        # element-wise addition
m <- matrix(z, nrow = 3)
```

A data frame is a two-dimensional table whose columns can hold different types. Columns are accessed with `$name`, `["name"]`, or a numeric index.

Functions are first-class values, meaning they can be passed as arguments, returned from other functions, and assigned to variables. Variables created inside a function's curly braces stay local to that function. Since R 4.1.0, anonymous functions can be written in a short lambda-style notation, `\(i) i^2`, for passing into higher-order functions like `sapply`. A native pipe operator, `|>`, also added in 4.1.0, chains functions left-to-right instead of nesting them: `mtcars |> subset(cyl == 4) |> nrow()` reads more naturally than the nested equivalent.

R has two native object-oriented frameworks. S3 is informal: a generic function like `summary()` examines the class attribute of its argument and dispatches to the matching method, so the same call returns one report for a numeric vector and a different one for a factor. S4 is stricter, modeled on Common Lisp's CLOS, with formal classes and multiple dispatch (selecting a method based on the types of several arguments at once).

Statistical modeling is built in. A linear regression takes one line, `model <- lm(y ~ x)`. `summary(model)` reports coefficients, standard errors, R-squared, and an F-statistic; `plot(model)` produces a 2-by-2 grid of diagnostic plots.

## Community, governance, and ecosystem

Three groups support R development. The R Core Team, founded in 1997, maintains the source code. The R Foundation for Statistical Computing, founded in 2003, provides financial backing. The R Consortium, a Linux Foundation project, develops infrastructure. The R Journal publishes open-access articles on packages and methods. The annual useR! conference, plus R-Ladies and other regional events, form the main meeting points; `#rstats` is the social-media tag for tracking developments.

Since version 2.14.0, R releases carry codenames drawn from Peanuts comics and films, inspired by Debian and Ubuntu's naming tradition. Alternative implementations include pqR (faster memory management), Renjin (running on the JVM), CXXR and Riposte (written in C++), and Oracle's FastR on GraalVM. Statistical front-ends like Jamovi and JASP run R behind a point-and-click interface.
