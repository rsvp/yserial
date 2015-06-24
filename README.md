# README for yserial

[![Join the chat at https://gitter.im/rsvp/yserial](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/rsvp/yserial?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

TL;DR single module file: **yserial = serialization + persistance** 

In a few lines of Python code, compress and annotate Python objects into
SQLite; then later retrieve them chronologically by keywords without any SQL.
Highly useful NoSQL "standard" module for a database to store schema-less
data.

It is based on *key/value* where the conceptual key is

     filename + table_name + primary_key + timestamp + notes

and the value is any reasonable object.  We generally mean Python objects, but
we include support for files (binary, image, etc.) and URL content (e.g.
webpages). Python objects are strings, dictionaries, lists, tuples, classes,
and instances. Objects are inserted into a hierarchy: database file, table
within that database, row within table. Moreover, each object is annotated for
reference by "notes" and automatically timestamped.

You are spared from explicitly spelling out many of the difficult protocol
details: cursor/connection, SQL/DB-API implementation, serialization,
compression, search algorithm, etc. -- for these are optimized to interact with
speed, security, and concurrency -- yet handled transparently.  And our module
is faster than comparable approaches under PostgreSQL. 

We highly recommend SQLite because it requires neither separate installation
nor a server process; also, it uses single normal files (easy to backup or
send), not an elaborate filesystem. Moreover, in comparison to similar
applications with MySQL or PostgreSQL, SQLite is extremely fast and suits most
purposes wonderfully. [The computing center at Harvard's math department
asserts that yserial *"provides a very reliable NoSQL interface for SQLite,"* 
see http://www.math.harvard.edu/computing/sqlite ]

The means for insertion, organization by annotation, and finally retrieval are
designed to be **simple to use**. The notes effectively label the objects
placed into the database. We can then later query the database, for example,
by regex (regular expression) searching on notes, and placing the qualified
objects in a dictionary. The keys of this dictionary correspond to the unique
primary keys used in the database. We can thus use Python code to process the
contents of this qualified dictionary, in effect, a data subset. If the objects
in that dictionary are themselves dictionaries we are essentially dealing with
schema-less data.

Other useful methods are available:

- insert any external file (via *infile*). This is handy for working with
  thousands of image files.
- insert anything on the web by URL (via *inweb*).
- insert in batches by generator (via *ingenerator*). This can be used to
  rapidly store a series of computationally intense results for quick
  retrieval at a later time.


## Installation: simply a single file

The latest development version of the module is
[y_serial_dev.py](https://github.com/rsvp/yserial/blob/master/y_serial_dev.py), 
whereas recent stable versions can be found under the
[release](https://git.io/yserial-release) directory.  **There are no dependencies, 
other than standard issue Python modules.**

```sh
     $ curl -kLO  https://git.io/y_serial_dev.py
```

REQUIREMENT: Python version 2.x where x is 5 or greater.  Copy or symlink the
y_serial module to where your Python can find it.  


## Documentation

The module includes the tutorial documentation within itself. And the source 
code contains verbose comments for developers. Our
[wiki](https://github.com/rsvp/yserial/wiki) has some useful tips.

But first checkout the **ten-minute HOWTO tutorial** at 
http://nbviewer.ipython.org/urls/git.io/yserial-HOWTO.ipynb


## Contributing to yserial repository

Details are covered in [CONTRIBUTING.md](https://git.io/yserial-pr) (which
should appear when making a pull request). All feedback is welcome. 

For real-time discussions, please go to the #yserial IRC channel on freenode:

- IRC <irc://irc.freenode.net/#yserial>


## Testing

Tests are contained within the module itself. 
The default database file db0 assigned in class Base presumes 
Linux top directory /tmp (change to suit your system) -- 
yserial is designed to operate *cross-platform* including Windows.

```py
     import y_serial_dev as y_serial
     y_serial.tester()
     #        ^for the principal class Main
     #        testfarm is for the beta version, not yet in Main.
     #   Flip the DEBUG variable for verbose results. 
```


## Memorable current links

- https://git.io/yserial points to the GitHub yserial repository.
- https://git.io/yserial-dev points to development module code page.
- https://git.io/y_serial points to the latest module file directly.


## Brief development history

- 2009-09-06  The *y_serial* code was open sourced as of v018.
- 2009--2010  Development at SourceForge http://sourceforge.net/projects/yserial 
- 2010-12-09  Repository moved to Bitbucket https://bitbucket.org/rsvp/yserial
- 2010-08-21  Released stable `y_serial_v060.py` 
- 2015-04-19  Converted GitHub repo from Mercurial-hg mirror to purely git.
- Further details in [CHANGELOG.md](https://git.io/yserial-log)

***Thanks so much to all who participated in this project over these long
years.  We truly appreciate your wonderful collaboration in developing our
code.***
[Acknowledgements](https://github.com/rsvp/yserial/wiki/Acknowledgements)

- *Adriano* @rsvp, yserial lead developer, http://rsvp.github.com


[//]: # ( COMMENTS )
[//]: # ( vim: set fileencoding=utf-8 ff=unix tw=78 ai syn=markdown : )
