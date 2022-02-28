.. linpeiman documentation master file, created by
   sphinx-quickstart on Sat Dec 19 17:51:25 2015.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. _index:

reStructuredText Extension for Visual Studio Code
=================================================
This extension enables reStructuredText related features in Visual Studio Code,

* Code Snippets
* Live Preview
* Editor Enhancement
* Linter
* IntelliSense

.. note:: To get Syntax Highlighting, please also install `this extension <https://marketplace.visualstudio.com/items?itemName=trond-snekvik.simple-rst>`_
   by Trond Snekvik.

.. image:: _static/main.gif
   :alt: screenshot

Getting Started
---------------
Install it from `Visual Studio Code Marketplace <https://marketplace.visualstudio.com/items?itemName=lextudio.restructuredtext>`_ .

#. Upgrade to Visual Studio Code 1.20.0 or above.
#. Switch to the Extensions view by clicking the fifth icon in the left most
   bar.
#. Type "restructuredtext" in the search box and hit Enter key.
#. Click "Install" button to install "reStructuredText" extension.

You can go through the follow articles to better understand the various
features,

.. toctree::
    :titlesonly:

    articles/index
    Support Services <https://support.lextudio.com>

Frequent Asked Questions can be found `here <https://github.com/vscode-restructuredtext/vscode-restructuredtext/issues?q=is%3Aissue+label%3A%22faq+candidate%22+>`_.

License
-------
This extension is licensed under the MIT License. 

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
