.. documentation master file, created by
   sphinx-quickstart on Sat Dec 19 17:51:25 2015.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. _index:

reStructuredText Ecosystem in Visual Studio Code
================================================
Visual Studio Code is a modern code editor for developers and more. To enable very good editing experience for a programming language, the following features are critical and necessary,

* Syntax Highlighting
* Code Snippets
* Editor Enhancement
* Linter
* IntelliSense
* Live Preview

In recent years, different extension authors have collaborated to make sure reStructuredText language is well supported in VS Code.

The start is the reStructuredText extension by LeXtudio Inc., which provides the basic features and also prompts to install all other neccessary ones, such as `this extension <https://marketplace.visualstudio.com/items?itemName=trond-snekvik.simple-rst>`_ by Trond Snekvik that provides syntax highlighting.

.. image:: _static/main.gif
   :alt: screenshot

Getting Started
---------------
Install the stable version from `Visual Studio Code Marketplace <https://marketplace.visualstudio.com/items?itemName=lextudio.restructuredtext>`_ .

#. Upgrade to Visual Studio Code 1.43.0 or above.
#. Switch to the Extensions view by clicking the fifth icon in the left most
   bar.
#. Type "restructuredtext" in the search box and hit Enter key.
#. Click "Install" button to install "reStructuredText" extension.

.. note:: If you want to stay on the edge, you can install Visual Studio Code
   Insider and then install the prerelease version of this extension.

You can go through the follow articles to better understand the various
features,

.. toctree::
   :titlesonly:

   Visit Docs Home <https://docs.lextudio.com>
   articles/index
   Support Services <https://docs.lextudio.com/support>
   privacy

Frequent Asked Questions can be found `here <https://github.com/vscode-restructuredtext/vscode-restructuredtext/issues?q=is%3Aissue+label%3A%22faq+candidate%22+>`_.

License
-------
The reStructuredText extension is licensed under the MIT License.

Please see :doc:`/articles/thirdparties` for details on the third-party files
that we include with releases of this project.

Acknowledgements
----------------

Logo
^^^^
The project logo comes from `Legendora Icon <http://raindropmemory.deviantart.com/art/Legendora-Icon-Set-118999011>`_
by `Teekatas Suwannakrua <http://raindropmemory.deviantart.com/>`_.

Linter
^^^^^^
The linter support is based on `Cody Hoover's ruby-linter <https://marketplace.visualstudio.com/items?itemName=hoovercj.ruby-linter>`_.

Live Preview
^^^^^^^^^^^^
The initial idea was brought from `Thomas Haakon Townsend's ReStructured Text Previewer <https://marketplace.visualstudio.com/items?itemName=tht13.rst-vscode>`_,
but soon after moving fully to Sphinx, this extension becomes its own beast.

IntelliSense
^^^^^^^^^^^^
The IntelliSense support is provided by the `Esbonio Language Server <https://github.com/swyddfa/esbonio>`_.
