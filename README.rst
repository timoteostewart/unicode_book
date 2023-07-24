About
-----

"Programming with Unicode" is a book written by Victor Stinner.

`Read the book online <https://unicodebook.readthedocs.io>`_.

Dependencies
------------

* `Sphinx <https://www.sphinx-doc.org/en/master/>`_ 7.0 or more recent:
  ``python -m pip install -U sphinx``.

* ``make html``:

  * ``sudo apt-get install dvipng`` (for pngmath)

* make pdf:

  * edit ``conf.py`` to enable ``rst2pdf.pdfbuilder`` extension: edit extensions line
  * ``sudo apt-get install rst2pdf``
  * ``sudo apt-get install python-matplotlib``
  * ``make pdf``

* ``make latex``:

  * Debian: ``sudo apt-get install texlive-latex-base texlive-lang-cyrillic``
  * Fedora: ``sudo yum install texlive-latex``
  * ``texlive-lang-cyrillic``: Cyrillic (mojibake section)
  * For make LaTeX ``./build_latex.py``


LaTeX
-----

.. code-block::

   Exception occurred:
     File "/usr/lib/python2.7/site-packages/sphinx/writers/latex.py", line 194, in __init__
       lang = babel.get_language(babel.language_code)
   AttributeError: 'ExtBabel' object has no attribute 'language_code'

   => lang = babel.get_language()
