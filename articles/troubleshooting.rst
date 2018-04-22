Troubleshooting Guide
=====================

By `Lex Li`_

If any error happens, please follow the steps below to locate the possible
causes.

Find The Logs
-------------
#. Use "View -> Output" menu item to open Visual Studio Code OUTPUT panel.
#. On the dropdown list in the upper right area of the OUTPUT panel that says
   "Search" by default, choose "reStructuredText" from the list to switch to
   reStructuredText logging page.

The logs show what compiler command line is used by this extension and which
HTML is being previewed. They should indicate what might be wrong.

Locate The Conf.py Folder
-------------------------
#. Open Integrated Terminal in Visual Studio Code code by clicking "View |
   Integrated Terminal".
#. If you have ``.vscode/settings.json`` in the workspace, find the value of
   ``restructuredtext.confPath`` setting. Assume its value is ``src``, execute
   ``cd src`` at terminal to switch to the folder.

Test The Generated HTML files
-----------------------------
When the make process succeeds, the generated HTML pages should present in
``${workspaceRoot}/_build/html``.

If you cannot find this folder or the extension indicates it cannot find
certain HTML page, then the make process might generate them at another
location. You have to set ``restructuredtext.builtDocumentationPath``.

.. note:: This should be an absolute path.
