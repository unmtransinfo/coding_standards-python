=======================
Python Coding Standards
=======================

The reason for coding standards is simple: maximize productivity, not just individual productivity but especially our joint productivity.
Code written to standards is easier to write, understand, deploy, and reuse.  A lot of other developers' time went into making tools
that will help you be productive, but to use them it helps to follow some basic rules.  

Repositories are also documents with very long lifetimes that anybody can see.  Programmers (and scientists who program) are
more valuable to collaborators, students, and future employers if their repositories show that they follow good programming pratices.

Technical Debt
--------------
When you're writing code, it's good to be aware of the concept of `technical debt`.  Simply put, technical debt is a cost of doing things
quickly that someone has to pay for later when they run, rewrite, or reuse your code.  Computational biologists know there are minefields
of technical debt laying around that we collectively pay the price for every time we read a FASTA file.  Technical debt isn't an absolute;
you can't decide `I will now eliminate all technical debt from my code` because time is finite and you can't rewrite every library or
convert every badly-thought-out file into a debt-free format.  Deadlines loom sometimes, and you simply have to get code out.  But when
you're at the start of your career, especially, you should minimize the technical debt all that you can because nobody expects you to be
highly productive at first.  

If technical debt is not an absolute, this means that there are times you may knowingly break every standard laid down here.  People
will still cheer you on if that results in something good that arrives just in time.  But taking the time to learn how to use these
standards early on will save you time later.

The Rules
---------
1. Use a repository and use it well.  Look at the time when you start writing code.  If you're still working on it an hour later,
  then it deserves to be in a repository.  When you're developing against that repository, use the branch-develop-merge pattern.
2. Write your code to be a python package.  That means start by searching potential names against PYPI for collisions.  You should
  pick a name that is short, lower-case, avoids underscores if at all possible, and not hierarchical unless you're prepared for
  the consequences.  
3. Follow PEP8 except where you have good reasons not to.
4. Use static typing routinely, so that you can take advantage of packages such as FastAPI and Typer.  This means python 3.8 or later.
5. Write tests using pytest.  If you do it for each function you write at the time you write them, you'll find this becomes natural.
6. Use the UNM Translational cookiecutter package to save yourself lots of boilerplate and enable modern services.
