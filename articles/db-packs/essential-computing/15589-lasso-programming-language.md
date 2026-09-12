# Lasso (programming language)

Lasso is both an application server and a general-purpose, high-level programming language designed to build and serve database-driven web pages. It began as a tool for exposing FileMaker databases to the web and grew into a proprietary, cross-platform language that supports procedural, object-oriented, and reflective styles.

## Core language

Lasso is object-oriented: every value is an object, and the language uses traits and multiple dispatch extensively. A trait is a reusable bundle of methods that types can mix in, and multiple dispatch means a method is chosen by the types of all its arguments, not just the receiver. Procedural programming is also supported through unbound methods (methods not attached to any object), and the language is dynamically typed with constraints (types checked at runtime, but contracts can require certain types up front), blending nominative typing (objects match a declared type) with duck typing (objects match by what they can do). Memory is managed automatically.

Lasso offers three execution modes for the same source: dynamic interpretation (like PHP or Python), just-in-time compilation (like Java or .NET), and pre-compilation (like C). Query Expressions provide a SQL-like syntax for iterating, filtering, and transforming sequences. Strings are fully Unicode and transparently converted to UTF-8 when written to the network or filesystem.

Templates use square brackets (`[ ... ]`) to embed Lasso code inside markup. HTML entities must stand in for literal brackets in output, unless a page opens with `[no_square_brackets]`. A typical snippet is `<?lasso 'Hello World!' ?>`, which prints `Hello World!` into the response.

The standard tool for database work is the `inline` command, which speaks a database-independent metalanguage so the same code works against MySQL, FileMaker, or any supported source. Parameters use leading dashes (e.g. `-database`, `-table`, `-findall`) and may appear in any order; raw SQL can be passed through `-sql` when the backend supports it.

## Application server

Lasso Server runs as a system service and receives requests through FastCGI (a protocol that hands web requests from a front-end web server to a back-end application). It passes each request to a separate Lasso Instance, so one machine can host many sites as isolated processes. I/O is handled by a green-threading scheduler (cooperative scheduling within a single OS process) built for multi-core hosts. The language core is implemented in C. Lasso code can also be packaged into standalone executables called LassoApps, where a folder structure compiles into a single file.

Lasso 9.0 (January 2010) was a major rewrite that added 64-bit support, strong-versus-weak typing, JIT compilation, and native serialisation. The stable release listed is 9.3.1 from October 23, 2015.

## Origins and ownership

The mid-1990s saw two AppleScript-based CGI tools that let FileMaker Pro serve web pages: Eric Bickford's WEB-FM and Russell Owens' FileMaker CGI (ROFM), both reliant on FileMaker calculation fields for formatting. In late 1995 Vince Bonfanti rewrote the ROFM idea in C/C++, replacing calculation fields with HTML templates. Bill Doerrfeld of Blue World Communications bought the code, named it Lasso, and shipped Lasso 1.0 in September 1996 for FileMaker Pro 3.x with WebSTAR on Mac OS 8.

Blue World licensed the post-1.2 source to Claris (then part of Apple), which bundled a derivative called CDML (Claris Dynamic Markup Language) with FileMaker 4.0 and Claris Homepage. Kyle Jessup became lead programmer; Lasso 2.0 followed in July 1997 with variables, math, and richer database actions.

Version 5 (February 2002) jumped from 3 to 5, dropping the FileMaker-only model. It was rewritten for OS X, Windows, and Linux, embedded MySQL, added Apache support on all three, and introduced LassoScript. The shift was driven by FileMaker's slow latency and high licensing cost compared to SQL engines, a problem no client-side change could fix.

FileMaker's 2004 pivot toward XML, XSLT, ODBC, and JDBC on the premium Server Advanced product pushed Blue World further from FileMaker; Lasso Pro earned MySQL Network certification in 2005. Blue World sold Lasso to OmniPilot Software in August 2004; OmniPilot shipped Lasso 8 in October 2004, splitting the server into separate "sites" and offering a free edition limited by IP address. In 2007 three employees, including Kyle Jessup, formed LassoSoft LLC to buy the IP from OmniPilot.

To compete with PHP and ASP, LassoSoft produced Lasso 9 in January 2010, a sweeping architectural rewrite. Documentation gaps and limited marketing caused a sharp community decline. A new Canadian firm, LassoSoft Inc., was founded in December 2010 to fund 9.x and its successors. Kyle Jessup remains Lead Developer and Benevolent Dictator for Life (a title from open-source tradition that grants the holder final say on language design).

## Position

Lasso runs on macOS, Windows, and Linux, with file extensions `.lasso` and `.LassoApp`. It is proprietary, influenced by Dylan, Smalltalk, and Scala, and is most often compared to PHP, Python, Ruby, and ColdFusion as a server-side scripting language.
