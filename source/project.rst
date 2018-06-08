=========================
Using Generated Projects
=========================

Here we illustrate how to use the generated projects created by ``mkg``. 
Currently, ``mkg`` supports either flat or nested project structure. The former
is suitable for simple projects while the latter fits more complex ones. All the
projects created by ``mkg`` are ready as Git repos.

--------------------
System Requirements
--------------------

* A recent C or C++ compiler
* GNU Make

We assume the default compiler on each platform, namely

* Visual C++ on Windows; besides, optional to MinGW
* Clang on Mac
* GCC on other Unix-like systems like GNU/Linux

For Windows users, you may get a port of GNU Make at `MSYS2 <https://www.msys2.org/>`_
or `GnuWin32 <http://gnuwin32.sourceforge.net/>`_.

----------------------------------------
Flat Console Application Projects for C
----------------------------------------

Let's say that we want to create such a project *myapp*:

.. code-block:: console

   $ mkg --flat myapp
   $ cd myap

You may invoke these commands at the root of the project:

* ``make`` compiles the main application
* ``make test`` compiles the main application and run a test against it
* ``make clean`` cleans generated files such as executable and objects

------------------------------------------
Nested Console Application Projects for C
------------------------------------------

Let's say that we want to create such a project *myapp*:

.. code-block:: console

   $ mkg myapp
   $ cd myapp

You may invoke these commands at the root of the project:

* ``make`` compiles the main application
* ``make test`` compiles the main application and run a test against it
* ``make clean`` cleans generated files such as executable and objects

*myapp* owns a nested project structure like this:

.. code-block:: console

   $ tree
   .
   ├── dist
   ├── examples
   ├── include
   ├── Makefile
   ├── README.md
   ├── src
   │   ├── Makefile
   │   ├── Makefile.win
   │   └── myapp.c
   └── tests
       ├── myapp.bash
       └── myapp.vbs

* *dist* for generated executable
* *examples* for example code
* *include* for headers
* *src* for application source code
* *tests* for test programs

All these directory destinations are customizable.

------------------------------------------
Flat Console Application Projects for C++
------------------------------------------

Let's say that we want to create such a project *myapp*:

.. code-block:: console

   $ mkg -cxx --flat myapp
   $ cd myap

You may invoke these commands at the root of the project:

* ``make`` compiles the main application
* ``make test`` compiles the main application and run a test against it
* ``make clean`` cleans generated files such as executable and objects

--------------------------------------------
Nested Console Application Projects for C++
--------------------------------------------

Let's say that we want to create such a project *myapp*:

.. code-block:: console

   $ mkg -cxx myapp
   $ cd myapp

You may invoke these commands at the root of the project:

* ``make`` compiles the main application
* ``make test`` compiles the main application and run a test against it
* ``make clean`` cleans generated files such as executable and objects

*myapp* owns a nested project structure like this:

.. code-block:: console

   $ tree
   .
   ├── dist
   ├── examples
   ├── include
   ├── Makefile
   ├── README.md
   ├── src
   │   ├── Makefile
   │   ├── Makefile.win
   │   └── myapp.cpp
   └── tests
       ├── myapp.bash
       └── myapp.vbs

* *dist* for generated executable
* *examples* for example code
* *include* for headers
* *src* for application source code
* *tests* for test programs

All these directory destinations are customizable.