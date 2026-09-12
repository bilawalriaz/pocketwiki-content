# Data-driven programming

Data-driven programming is a programming paradigm in which program statements describe the data to be matched and the processing required, rather than defining a sequence of steps. The program is a collection of conditions paired with actions, and a main loop (a central cycle that repeatedly pulls the next unit of work, tests it, and dispatches it) decides which action fires for each input. Pattern matching is typically done with regular expressions (compact patterns that match character strings) or line numbers.

The standard examples are the text-processing languages sed and AWK, and the document transformation language XSLT. In these languages the data is a sequence of lines in an input stream (a flow delivered one item at a time), so they are also called line-oriented languages.

## Related paradigms

Data-driven programming is similar to event-driven programming. Both are structured as pattern matching with resulting processing and both rely on a main loop, but they are applied to different domains. The condition/action model is also similar to aspect-oriented programming, where when a join point (a condition such as a function call) is reached, a pointcut (an action) runs. A similar paradigm appears in tracing frameworks such as DTrace, where one lists probes and the actions that execute when a probe fires.

Adapting abstract data type design methods to object-oriented programming produces a data-driven design, sometimes used during software conception to define classes.

## Applications

Data-driven programming is applied to streams of structured data for filtering, transforming, aggregating (computing statistics, for example), or calling other programs. Typical streams include log files, delimiter-separated values, and email messages.

A representative AWK program takes a stream of log statements, writes every line to the console, sends lines beginning with "WARNING" to a warning file, and emails a sysadmin whenever a line begins with "ERROR", while counting warnings per day. The same approach applied to delimiter-separated values can process each line or aggregate across them, computing a sum or maximum. For email, procmail matches conditions on each message and chooses an action such as deliver, bounce, discard, or forward.

Some data-driven languages are Turing-complete (capable of computing anything a general-purpose computer can, given enough time and memory), including AWK and even sed. Others are intentionally limited to filtering. The pcap packet-capture language is an extreme case: it consists only of filters, with the single action "capture". The Sieve mail-filtering language has filters and actions, but its base standard has no variables or loops, so each input element is processed independently in a stateless filter. Variables introduce state, which permits operations that depend on more than one input element, such as aggregation or throttling (for example, allowing at most five mails per hour from each sender, or limiting repeated log messages).

Data-driven languages frequently define a default action when no condition matches: line-oriented languages such as sed may simply print the line, and Sieve may deliver the message. Matching may be exclusive, where only the first matching statement runs, or non-exclusive, where all matching statements run. A failure to match any pattern can be treated as default behavior or caught by a catch-all statement at the end.

## Benefits and issues

Functionality only needs the abstract data type of the variables it works with, so functions and interfaces can be reused on all objects that share the same data fields, such as an object's "position". Data can be grouped into objects or entities with little consequence. Data-driven design prevents coupling data with functionality, but it has been argued to lead to poor object-oriented design when the data is more abstract, because a purely data-driven object is defined by how it is represented. Any change to that structure breaks the functions that rely on it.

Driving directions illustrate the trap. If an intersection is represented by a zip code and two street names, a city where the same two streets cross more than once produces bugs, because the data no longer uniquely identifies the intersection. Restructuring data is a common task in software engineering, done to eliminate bugs, increase efficiency, or support new features, and data-driven designs make such restructuring costly.

The languages commonly described as data-driven include AWK, BASIC, Clojure, fdm, Lua, maildrop, Oz, Perl, procmail, Raku, REBOL and other Redbol languages, sed, Sieve, Tab, and XSLT. They differ in scope: full languages such as AWK and Perl embed data-driven constructs inside a general-purpose toolkit, while narrow tools such as pcap or base Sieve restrict the user to filtering.
