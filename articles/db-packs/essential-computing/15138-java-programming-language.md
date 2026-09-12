# Java (programming language)

Java is a high-level, general-purpose, memory-safe, object-oriented programming language designed so that compiled code runs on any hardware with a Java virtual machine, a property Sun Microsystems called "write once, run anywhere" when the language debuted on May 23, 1995. James Gosling, Mike Sheridan, and Patrick Naughton began the project at Sun Microsystems in June 1991 under the name Oak, then Green, before settling on Java coffee. Java 1.0 shipped on January 23, 1996.

The portability that defines Java comes from an extra layer of translation. A Java compiler does not emit machine code for a specific processor; it emits *bytecode*, a compact instruction set for an imaginary CPU. A *Java Virtual Machine* (JVM) on each host device translates bytecode into that device's native instructions at runtime. To preserve type safety, Java forbids pointer arithmetic, so the garbage collector can relocate referenced objects without invalidating addresses. The same design choice, automatic *garbage collection*, frees the programmer from calling `free` or `delete` as in C or C++; once no live reference to an object remains, its memory becomes eligible for reclamation. A reference that points to no object raises `NullPointerException` if dereferenced.

Bytecode interpretation was historically slow, but just-in-time (JIT) compilation, introduced with Java 1.1 in 1997/1998, compiles hot bytecode paths to native code at runtime. Sun's *HotSpot* JIT became the default JVM in 2000 and remains the standard execution engine.

Java's syntax is deliberately close to C and C++ so systems programmers would find it familiar, but the language is built almost exclusively as object-oriented. Every piece of code lives inside a class, and every data item is an object except for a small set of *primitive types* (integers, floats, booleans, characters) kept as raw values for performance. Java omits features that complicate C++: no operator overloading, no multiple inheritance for classes, though a class may *implement* several *interfaces*. Types are checked at compile time.

A traditional entry point looks like this:

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}
```

Java 25 (September 2025) added a simpler form, `void main() { IO.println("Hello World!"); }`, that omits the enclosing class for small programs.

The language has accreted features steadily. Generics, added in J2SE 5.0 in September 2004, let containers hold only specified types and shift certain `ClassCastException` errors from runtime to compile time; a 2016 formal proof showed the resulting type system is technically *unsound* because generics can be subverted at runtime. Lambdas and streams arrived with Java 8 in March 2014, bringing functional-programming style.

Java is governed, not by an external standards body, but through the *Java Community Process* (JCP), a Sun-era procedure that lets outside companies propose and review API changes. Sun relicensed most of Java under GPL-2.0-only between November 2006 and May 2007. After Oracle acquired Sun in January 2010, it became steward of Java and owner of the trademark; the open-source *OpenJDK* is the official reference implementation and ships by default on most Linux distributions.

Oracle segments the platform into four editions: Java Card for smart cards, Java ME for mobile and embedded devices, Java SE for workstations, and Java EE (renamed Jakarta EE) for enterprise servers. The *Java Class Library*, organized into *packages*, supplies I/O, networking, concurrency, collections, XML processing, security, and GUI toolkits such as Swing and the newer JavaFX. Servlets, JSP, JAX-RS, and JAX-WS underpin server-side web work. Beginning with JDK 9 in September 2017, applets, programs that once ran inside web browsers, were deprecated.

Releases follow a six-month cadence, every March and September. Long-term support (LTS) versions, intended for production systems that prioritize stability, are Java 8 (March 2014), 11 (September 2018), 17 (September 2021), 21 (September 2023), and 25 (September 2025). Java 26 shipped March 17, 2026.

Android complicates the picture. Android applications are written in the Java language but run on a different virtual machine: bytecode compiled for Android is not JVM bytecode, and the standard library is a large subset of Java SE provided through Apache Harmony. The use of Java-derived APIs in Android produced the *Google LLC v. Oracle America* copyright dispute. On April 5, 2021, the United States Supreme Court ruled 6–2 that Google's use of Java APIs in Android was fair use, while deliberately avoiding a ruling on whether APIs themselves can be copyrighted.

Common criticisms target the verbosity of certain APIs, slow startup compared with natively compiled languages, the lack of unsigned integer types, quirks in floating-point arithmetic, and a history of security vulnerabilities in HotSpot.

Source: adapted from "Java (programming language)" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Java_%28programming_language%29
