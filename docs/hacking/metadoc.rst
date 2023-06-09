==============================
Documentation on documentation
==============================

Documentation is now written in ReStructuredText, a lightweight and
readable markup language designed for Python.

Conventions
===========

ReStructuredText leaves much freedom in the syntax - in our help files we
try to stick to consistent conventions as in the following.

Markup for sectioning
---------------------

::

  ==============
  Document title
  ==============

  Section title
  =============

  Subsection title
  ----------------

  Sub-subsection title
  ********************

Blank and spaces
----------------

One blank line before and after every paragraph.
Two-char indent in definition lists.

Inline help parser syntax
=========================

As to the time when this documentation was last updated, the online help
parser programmed into Angband does the following:

- ignore colons (``|``)
- ignore paragraphs starting with ``..`` (including their trailing blank
  line)
- recognize link targets (``.. _something``) and be
  able to open a file to the right position using them.
- recognize "menu" links for the online help navigation. Links are given 
  with the following format (``g`` is the hotkey here):

:: 

.. menu:: [g] option.txt

Tricks
======

Sometimes it is tricky to get a thing to display in the correct way in both
the online help and the compiled RST. This is often due to the complex
interaction between backslashes and backticks in RST. In particular, in
several places we need to use in RST a syntax such as

::

``D``\isarm

If this appeared directly in the help file, then the online help parser
would display a spurious backslash character ``\`` before the ``i`` letter.
It would be quite complicated to instruct it to parse backslashes using the
full RST syntax. Instead, we adopt the following workaround: we write

::

  this is a paragraph containing the word |``D``isarm| just in the middle

and later in the file we define a substitution directive

::

.. |``D``isarm| replace:: ``D``\isarm

Magically this works, since the online help parser *skips* pipes.
