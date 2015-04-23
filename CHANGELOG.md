# CHANGELOG (in reverse chronological order)

     - Users may consult the ```y_serial_dev.py``` module itself for detailed
       documentation.  That single file is the latest and all you need for
       execution, see HOWTO http://yserial.sourceforge.net


## 2015-04-22  Release of y_serial v0.70.0 at GitHub

It's been five years since the last release -- v060 was rock-solid stable.
For the latest release, we can certify that it works under Python 2.7.8 and
IPython 2.3.0. We changed the default database db0 for the development version
to work under /tmp, and the encoding of the source code is now officially
utf-8. Nice to see that our work has been useful in IPython notebooks and 
clusters.


## 2015-04-19  GitHub becomes our development site

Over the last five years, there has been a dramatic shift to **git** as a
primary tool for version control, and to **GitHub** as a community development
site -- thus we have decided to drop Mercurial-hg for version control.

The *yserial* repository at GitHub formerly was a hg mirror, but henceforth it
will become the primary development site. (The hg-git extension, maintained by
durin42, was used to create the mirror.) Mercurial is obviously not supported
at GitHub, but our repository is easy to clone using a generic hg command.  

     - Annotated TAGS will adopt the following semantic versioning form:
       vN.mm.b where N= major, mm= minor, b= bugfix numbers, e.g. v0.60.1


## 2010-11-05  Version control using Mercurial-hg 

The development style using Mercurial version control is discussed in the
docs/02-hg-dev-stable-branch.html [deleted as of 2015-04-19].  There are two
branches in the repo: default and stable. The default branch is for non-bug
development, while the stable branch is for bug fixes.

Recorded TAGS will generally take the semantic versioning form:  vNmm.b
where N= major, mm= minor, b= bugfix numbers, e.g. v060.1


## 2010-12-09  Repository moved to Bitbucket.org

Our primary development repository has shifted from SourceForge to
**Bitbucket**, please see https://bitbucket.org/rsvp/yserial

We will continue to use Mercurial-hg for version control, however, 
using the hg-git extension we will maintain a mirror at GitHub.


## 2010-08-21  Release y_serial_v060.py SHA256 signature 

92313b2e60afea86fa0812637e271e61e619aaa699e60ab4f061abfb61cd4adb


## 2009 to 2010 at SourceForge.net

Development site during this period was **SourceForge**, please see
http://sourceforge.net/projects/yserial/ 

Coding began there with v018 on 2009-09-06.


## Welcome message

Thanks very much for participating in this project. We appreciate your
collaboration in developing our code.

     - Adriano, yserial lead developer, http://rsvp.github.com


___
vim: set fileencoding=utf-8 ff=unix tw=78 ai syn=markdown : 
