.. linpeiman documentation master file, created by
   sphinx-quickstart on Sat Dec 19 17:51:25 2015.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. _index:

reStructuredText Extension for Visual Studio Code
=================================================

What is reStructuredText?
-------------------------
Below is the definition quoted from `the Docutils homepage <http://docutils.sourceforge.net/rst.html>`_ .

"reStructuredText is an easy-to-read, what-you-see-is-what-you-get plaintext
markup syntax and parser system. It is useful for in-line program
documentation (such as Python docstrings), for quickly creating simple web
pages, and for standalone documents. reStructuredText is designed for
extensibility for specific application domains. The reStructuredText parser is
a component of Docutils. reStructuredText is a revision and reinterpretation
of the StructuredText and Setext lightweight markup systems."

"The primary goal of reStructuredText is to define and implement a markup
syntax for use in Python docstrings and other documentation domains, that is
readable and simple, yet powerful enough for non-trivial use. The intended
purpose of the markup is the conversion of reStructuredText documents into
useful structured data formats."

.. image:: _static/rst.png

.. note:: Though Markdown has now become almost the standard of documentation markup,
   reStructuredText still has its own terrirtories.

   You can find a lot of information about reStructuredText from Docutils.

What is Sphinx?
---------------
Below is the definition quoted from `the Sphinx homepage <http://www.sphinx-doc.org/en/master/>`_ .

"Sphinx is a tool that makes it easy to create intelligent and beautiful
documentation, written by Georg Brandl and licensed under the BSD license."

"It was originally created for the Python documentation, and it has excellent
facilities for the documentation of software projects in a range of languages.
Of course, this site is also created from reStructuredText sources using
Sphinx! The following features should be highlighted:"

* **Output formats:** HTML (including Windows HTML Help), LaTeX (for printable
  PDF versions), ePub, Texinfo, manual pages, plain text
* **Extensive cross-references:** semantic markup and automatic links for
  functions, classes, citations, glossary terms and similar pieces of
  information
* **Hierarchical structure:** easy definition of a document tree, with
  automatic links to siblings, parents and children
* **Automatic indices:** general index as well as a language-specific module
  indices
* **Code handling:** automatic highlighting using the Pygments highlighter
* **Extensions:** automatic testing of code snippets, inclusion of docstrings
  from Python modules (API docs), and more
* **Contributed extensions:** more than 50 extensions contributed by users in
  a second repository; most of them installable from PyPI

"Sphinx uses reStructuredText as its markup language, and many of its strengths
come from the power and straightforwardness of reStructuredText and its
parsing and translating suite, the Docutils."

.. note:: Documentation hosting sites such as `ReadTheDocs <https://readthedocs.org/>`_ help make Sphinx popular.

What is Visual Studio Code?
---------------------------
`Visual Studio Code <https://code.visualstudio.com/>`_ is a free and open source code editor from Microsoft.

According to various surveys such as `Stack Overflow Developer Survey <https://insights.stackoverflow.com/survey/2018/#development-environments-and-tools>`_ ,
Visual Studio Code is now the most popular editor around the world.

OK, what is this extension?
---------------------------
This extension enables reStructuredText related features in Visual Studio Code,

* Syntax highlighting
* Code Snippets
* Live Preview
* Section Builder
* Linter
* IntelliSense

.. image:: _static/vscode.png

Get started
-----------
Install it from `Visual Studio Code Marketplace <https://marketplace.visualstudio.com/items?itemName=lextudio.restructuredtext>`_ and we are ready to go.

#. Upgrade to Visual Studio Code 1.20.0 or above.
#. Switch to the Extensions view by clicking the fifth icon in the left most
   bar.
#. Type "restructuredtext" in the search box and hit Enter key.
#. Click "Install" button to install "reStructuredText" extension.

Configuration system is documented in :doc:`/articles/configuration`.

Frequent Asked Questions can be found `here <https://github.com/vscode-restructuredtext/vscode-restructuredtext/issues?q=is%3Aissue+label%3A%22faq+candidate%22+>`_ .

Contributing to the code
------------------------
Check out :doc:`/articles/development` for more details on how to contribute
to this extension!

Check the `dashboard on work items <https://waffle.io/vscode-restructuredtext/vscode-restructuredtext>`_ .

License
-------
This extension is licensed under the MIT License. Please see
:doc:`/articles/thirdparties` for details on the third-party files that we
include with releases of this project.

Acknowledgements
----------------
Logo
^^^^
The project logo comes from `Legendora Icon <http://raindropmemory.deviantart.com/art/Legendora-Icon-Set-118999011>`_
by `Teekatas Suwannakrua <http://raindropmemory.deviantart.com/>`_ .

Linter
^^^^^^
The linter support is based on `Cody Hoover's ruby-linter <https://marketplace.visualstudio.com/items?itemName=hoovercj.ruby-linter>`_ .

Live Preview
^^^^^^^^^^^^
The initial idea was brought from `Thomas Haakon Townsend's ReStructured Text Previewer <https://marketplace.visualstudio.com/items?itemName=tht13.rst-vscode>`_ ,
but soon after moving fully to Sphinx, this extension becomes its own beast.

IntelliSense
^^^^^^^^^^^^
The IntelliSense support is provided by the new `reStructuredText Language Server <https://github.com/lextm/restructuredtext-antlr>`_ .
