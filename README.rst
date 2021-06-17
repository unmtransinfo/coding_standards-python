=======================
Python Coding Standards
=======================
The reason for coding standards is simple: standards maximize productivity.  Not just individual productivity but the productivity
of the community. Code written to standards is easier to write, understand, deploy, and reuse.  Writing to standards saves you time
both by avoiding pitfalls and also by enabling use of powerful software techniques.  Better programmers than you have fallen into
those pitfalls and written their way out of problems that would otherwise waste your time, so you stand on their shoulders. Programmers
(and scientists who program) are more valuable to collaborators, students, and future employers if that they follow good software engineering
practices.

Technical Debt
--------------
When you're writing code, it's good to be aware of the concept of `technical debt`.  Simply put, technical debt is a cost of doing things
quickly that someone has to pay for later when they run, rewrite, or reuse your code.  Computational biologists know there are minefields
of technical debt laying around that we collectively pay the price for every time we read a FASTA file.  Technical debt isn't an absolute;
you can't decide `I will now eliminate all technical debt from my code` because time is finite and you can't rewrite every library or
convert every badly-thought-out file into a debt-free format.  Deadlines loom sometimes, and you simply have to get code out.  But when
you're at the start of your career, especially, you should minimize the technical debt all that you can because nobody expects you to be
highly productive at first.  

Why Not a Notebook?
-------------------
Data scientists use Jupyter notebooks extensively.  Notebooks show off your code.  They run server-side so the data marshalling
is done in advance and, once configured, let you do exploratory analysis quickly.  But if you need stable, reproducible code that
can be shared with others, notebooks suck.  Notebooks blow up nearly every tool of software engineering: modularity, repositories, IDE,
testing, versioning.  If you want to write a long-running app, if you want to use a package not contained in the server, if you want
to share anything, you're going to be starting from scratch.  You'll be more productive if you make a package from the start.

The Standards
-------------
Since technical debt is not an absolute, there will be times you may knowingly break every standard laid down here.  People
will still cheer you on if that results in something good that arrives just in time.  But taking the time to learn how to use these
standards early on will save you time later.

1. **Use a repository.**  The repository guarantees that you'll be able to find it later, when you've forgotten the details. With it comes a lot of great services for free, like testing, packaging, code quality assessment, dependency updating, and documentation publishing.
2. **Write code to be a python package.**  Making a package increases your productivity by increasing code reuse.  Start by searching potential package names against PYPI for collisions.  You should pick a name that is short, lower-case, and memorable.  Avoid underscores, they create messes later. 
3. **Follow PEP8.**  There are sometimes legitimate reasons not to follow the rules that everybody agrees upon, but they're rare.
4. **Use static typing.** Using python's type hints lets you can take advantage of packages such as FastAPI and Typer.  This means python 3.8 or later.
5. **Write tests.** Dependencies update every day and the only way you will know that your code isn't broken is if you wrote tests.  Using pytest isn't difficult, and if you write tests for each function you write, testing quickly becomes natural.  With GitHub Actions, every commit can get tested, documented, and published.
6. **Use a template.** Templates save you lots of time writing boilerplate, plugs you code into services, and gets the branding right. The `UNM Translational cookiecutter <https://github.com/unmtransinfo/cookiecutter-unmtransinfo-python>`_ template is there for you to use.
