# The LDL programming language

# Introducation

## Why a new language?

This repository is for the LDL programming language, which does not exist yet.
I am planning for the design and implementation and all the results will be
here.

I have tried a lot of programming languages and I think they all have something
undesired. First I want to describe my ideal language:

1. It should be compiled, no-gc, source cross-platform, and suitable for system
   programming.
2. It should have a static type system and a decent module system.
3. It should be basically an OO language with standalone function support.
4. It should NOT have language features encouraging excessive meta-programming.
5. It should support unicode and i18n in the language level.
6. It should have a pragmatic standard library for application development.
7. It should be easy to write a new program, without a lot of boilerplate or
   initial setup.
8. It should have a decent light weight IDE as a part of the langauge
   implementation.

The thought of creating this new language came from my using MQL (the MetaQuotes
Language). It is a propriety langauge and basically a simplified version of C++.
I used the language extensively and tried to write a standard library in it. In
the process I found that the language is quite limited, however, I can go pretty
far with the existing features. I am confident that I know all the MQL features,
which is a fealing that I do not have when using C++. With every new feature,
the library can be greatly enhanced. And the MQL language contains a single
executable IDE (MetaEditor) with the compiler buildin. The IDE has a
syntax-highlighting and auto-complete editor, with support for debugging,
profiling, and version control. If you want to create a new program, you just
fire up the IDE (or Editor), write your program, hit compile, and run. No need
to create a project, nor setup include paths and library paths, nor use any
build tool. It is extremely easy to start working.

Probably you can write Python this way (IDLE) but it is interpreted and does not
have a static type system. Nim is compiled and boasts a Python like experience,
but it is not main stream and has problems with library support and stablity.
And I hate the bash like syntax.

JVM languages need the huge JRE (or JDK) to run and good luck configuring maven
or gradle or downloading a even larger IDE. To me, Java has a decent feature set
so that it can implement most things without too much effort. It is necessary to
keep the language simple and easy to understand. Scala or Haskell like languages
is too theorectical and most people can not understand the program without an
involved thinking process.

C++ is unnecessarily powerful and they are continuingly adding new features to
the language while the standard library is still not practical for writing any
useful applications. It does not even have a standard way to handle unicode. It
is encouraging people using template meta-programming which to me is just a lame
technique to code generation. They are abusing something not intended to be a
turing complete functional programming language. And they call this "modern C++"
as opposed to the good old OO C++. Setting up a C++ project is even harder, and
you have to learn Makefile or CMake or some other peculiar build systems (like
autotools). I think Fortran is better in that it has a module system and you do
not need to handle include files. D is meant to be a C++ without the backward
compatibity concern. So D is also too complicated. D is also Garbage Collected
which puts off many people. They are pushing the "Better C" mode recently and
strive to be GC free in the standard library. The trend is clear in D, that
people want an efficient and simple language rather than a complex and
"powerful" one.

Rust is polular and promising these days, but I found the life time semantics
and syntax quite confusing. And all the new languages learn the ruby way to
include a version manager and a package manager, so you can install several
compilers and libraries in parallel. To me this is just a sign of bad design
because you can not keep the language compatible with previous versions and the
library ecosystem is a mess. They use an online package manager which is too
slow to download anything and you have no explicit way to download and install
them manually.

Maybe there are alternatives, but overall I do not find any language that
satisfies the requirements I mentioned. I want a pragmatic, simple, or even
boring language that is familar to C/C++/Java guys, suitable for both system and
applicaton programming. I want people to create various libraries to enhance the
ecosystem rather than discussing language features.
