reStructured Ecosystem
======================

By `Lex Li`_

reStructuredText has evolved for decades and ever since Visual Studio Code was
born, an ecosystem is built around it to serve a variety of users. This article
provides a snapshot of the main components currently being used by more than
370,000 active users.

reStructuredText Extension for Visual Studio Code
-------------------------------------------------
This is currently the core of the ecosystem with most users. Its frequent
releases keep bringing new features and bug fixes, and also integrate with the
best and latest components of the whole ecosystem.

.. note:: Later this extension might be referred to as vscode-restructuredtext.

reStructuredText Syntax Highlighting
------------------------------------
This is an extension created by Trond Snekvik, which focuses on syntax
highlighting and section navigation.

.. note:: Later this extension might be referred to as vscode-rst.

.. important:: vscode-restructuredtext prompts new users to install vscode-rst,
   to ensure that all users receive the best in class syntax highlighting.

Esbonio Language Server
-----------------------
.. danger:: Starting from version 190.1.17 of vscode-restructuredtext, this
   component is replaced by the Esbonio extension.

Esbonio Extension for Visual Studio Code
----------------------------------------
.. danger:: Starting from version 190.1.17 of vscode-restructuredtext, this
   component is needed.

This extension is created by Alex Carney that enables reStructuredText language
services, such as

* Linting
* Build error detection
* Live preview

.. note:: Later this extension might be referred to as esbonio.

.. important:: vscode-restructuredtext prompts new users to install esbonio so
   that language services can be enabled.

.. warning:: If more code linting than esbonio is required, users can install
   individual linters such as doc8, rstcheck, and restructuredtext_lint.

Microsoft Python Extension
--------------------------
This extension is not that closely related to reStructuredText itself, but does
provide good support on selecting Python interpreters and so on.

.. important:: vscode-restructuredtext prompts new users to install
   vscode-python.
