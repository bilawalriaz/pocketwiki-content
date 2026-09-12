# Computer programming

Computer programming, also called coding, is the composition of step-by-step instructions, called programs, that computers follow to perform tasks. A programmer designs algorithms (precise procedures for solving a problem) and expresses them as code in one or more programming languages. Proficient programming combines several kinds of knowledge: the application domain, the chosen language and its code libraries, the algorithms suited to the problem, and some formal logic.

## How programming actually works

Programs are written in high-level languages that resemble human language, then translated into machine code, the binary instructions a central processing unit executes directly. The translator is either a compiler, which converts the whole program ahead of time, or an interpreter, which executes it line by line. Low-level languages map closely to a particular machine and execute fast; high-level languages hide hardware details and are easier to read, write, and port.

Languages are grouped into paradigms, styles that shape how solutions are expressed. Imperative languages (procedural or object-oriented) describe how to do something step by step. Functional languages treat computation as the evaluation of pure functions. Logic programming languages express rules that an engine searches to satisfy. Choice of language balances the task (COBOL persists in corporate mainframes, Fortran in engineering, C in embedded systems, scripting languages on the web), team expertise, libraries, and speed required.

Every high-level language offers a common core: input, output, arithmetic, conditional execution (branching on a test), and repetition (loops). Programs call into shared libraries, reusable code any program can use, as long as both sides follow the same conventions for passing arguments.

## A short history

Programmable devices predate electronic computers. In 1206 Al-Jazari built a programmable drum machine whose patterns were set by pegs and cams. The Jacquard loom of 1801 used punched pasteboard cards to weave different patterns, an early example of instructions stored as data.

The first computer program is generally dated to 1843, when Ada Lovelace published an algorithm for computing Bernoulli numbers, intended for Charles Babbage's Analytical Engine. (Babbage himself had written a program for the same machine in 1837.) In the 1880s Herman Hollerith introduced machine-readable punched cards. The conceptual breakthrough came in 1949 with the stored-program computer, where programs and data lived in the same memory.

Early programs were written in machine code, then assembly languages, which use mnemonics like `ADD X, TOTAL` but still map one-to-one onto a specific machine. The first compiler, the A-0 System, was developed in 1952 by Grace Hopper, who coined the term. FORTRAN, released in 1957, was the first widely used high-level language with a working compiler, followed by COBOL for business data and Lisp for research. Programs were typed onto punched cards until the late 1960s, when cheap terminals let programmers work directly at a screen.

## What makes a program good

A finished program is judged on properties beyond correctness:

- Reliability: correct results, which depends on correct algorithms and freedom from mistakes like buffer overflows, race conditions, and off-by-one errors.
- Robustness: how well it handles bad data, missing memory, or network outages without crashing.
- Usability: the ergonomics of the interface.
- Portability: how easily the source runs on different hardware and operating systems.
- Maintainability: how easily future developers can fix bugs or adapt the code, often the deciding factor in a program's survival.
- Efficiency: how much processor time, memory, and network bandwidth it uses, a concern mainly when the program bottlenecks the system.

Readability cuts across all of these. Programmers spend most of their time reading existing code, so consistent indentation, meaningful names, small functions, and comments reduce bugs and speed modification. Integrated development environments (IDEs) bundle editors, debuggers, and refactoring tools to support this.

Choosing efficient algorithms matters as much as clean code. Algorithms are ranked by orders of growth using Big O notation, which expresses resource use as a function of input size. An O(n) scan scales linearly, an O(n²) nested loop scales quadratically, and the gap becomes decisive at large inputs. Expert programmers recognize common algorithms and pick one whose growth rate fits the situation.

## Debugging and the broader process

A bug, a defect causing wrong behavior, is most often a logic error. The term famously comes from a moth found in a Harvard mainframe on September 9, 1947. Debugging usually starts by reproducing the problem, then simplifying the input until the smallest case still fails, and isolating the cause by trial and error or by setting breakpoints (places where execution pauses for inspection). IDEs and standalone debuggers like GDB support this.

Programming is one part of a larger software development process that also covers requirements analysis, design, testing, build systems, and maintenance. When the process is rigorous, the field calls it software engineering. Methodologies range from waterfall (long, sequential stages) to agile approaches that fold analysis, coding, and testing into short cycles of a few weeks.

## Learning to program

In 1957 the United States had about 15,000 programmers, roughly 80 percent of the world's total; by 2014 the worldwide count was about 18.5 million. Learning to program has grown from a narrow technical skill into a broad educational movement supported by academic courses, books, online platforms (Codecademy, Khan Academy, freeCodeCamp, LeetCode, HackerRank), coding bootcamps, and initiatives such as Code.org's Hour of Code.

Influential early texts include Wilkes, Wheeler, and Gill's *Preparation of Programs for an Electronic Digital Computer* (1951), Kemeny and Kurtz's *BASIC Programming* (1967), Jensen and Wirth's *Pascal User Manual and Report* (1971), and Kernighan and Ritchie's *C Programming Language* (1978). Knuth's *The Art of Computer Programming* (from 1968) catalogued algorithms with formal analysis, and Kernighan and Plauger's *The Elements of Programming Style* (1974) argued that programs should be written for human readers, not just compilers. Since around 2000, print has given way to blogs, wikis, video tutorials, interactive sites, and AI-assisted coding tools. Research links good programming ability to strong natural-language skills, suggesting that learning to code resembles acquiring a foreign language, with syntax and idiom learned through reading and practice rather than pure logic.
