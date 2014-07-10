Perl-Tk-Wizard — `Tk::Wizard` — Wizard GUI Framework
====================================================

DESCRIPTION
-----------

In the context of this Perl namespace, a Wizard is defined as a graphical
user interface (GUI) that presents information, and possibly performs
tasks, step-by-step via a series of different pages.  Pages (or
'screens', or 'Wizard frames') may be chosen logically depending upon
user input.

The `Tk::Wizard` module automates a large part of the creation of a
wizard program to collect information and then perform some complex
tasks based upon it.

The wizard feel is largly based upon the Microsoft(TM,etc) wizard style:
the default is similar to that found in Microsoft Windows 95; a more
Windows 2000-like feel is also supported (see the "-style" entry in
"WIDGET-SPECIFIC OPTIONS".)  Subclassing the module to provide different
look-and-feel is highly encouraged: please see "NOTES ON SUB-CLASSING
`Tk::Wizard`".

Important Changes To Previous Versions
--------------------------------------

* `Tk::Wizard` Version 2.084, distribution 2.143,
  allows Wizard::addPage to accept same args as Wizard::blank_frame:
  see t/055_Pages.t

* `Tk::Wizard` Version 2.131 moved some methods to new modules to keep
  in line with the original ethos as outlined in the POD.
  This should have no practical effect until verseion 3.00 but
  please read the documentation for the "import" method for
  further details.

* As of `Tk::Wizard` version 2.044 (distribution version 2.111),
  the -width and -height arguments to blank_frame() are applied
  to the /content area only/, not to the entire Wizard window.
  Look-up the Martin Thurn's `Tk::Wizard::Sizer` module
  to semi-automatically recalculate what you should pass in the
  `-width` and `-height` arguments.

INSTALLATION
------------

This module can be installed in the normal perl way, such as one of:

    perl -MCPAN -e "install Tk::Wizard"
    cpan Tk::Wizard
    cpanm Tk::Wizard

    perl Makefile.PL && make all test && make install

If you are on Windows you might have to use `nmake` instead of make -
or you could try:

    ppm install `Tk::Wizard`

If you set environment variable `TEST_INTERACTIVE` to any non-zero
value, most of the tests will pause and you will have to click the
"Next" button several times to get through them.

AUTHOR
------
Lee Goddard (lgoddard@cpan.org)

LAST UPDATED
------------
2010. This file: 2014.

MANY THANKS TO
--------------
Daniel T Hable
Martin Thurn (mthurn@cpan.org)
