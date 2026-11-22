Troubleshooting Guide
=====================

By `Lex Li`_

If any error happens, please follow the steps below to locate the possible
causes.

Reboot The Computer
-------------------

In some cases (though rarely), Visual Studio Code background processes can be
left behind. These background processes are involved in tasks such as
rendering HTML preview.

Find The Logs
-------------
#. Use "View -> Output" menu item to open Visual Studio Code OUTPUT panel.
#. On the dropdown list in the upper right area of the OUTPUT panel that says
   "Search" by default, choose "reStructuredText" or "Esbonio Language Server"
   from the list to switch to reStructuredText logging pages.

The logs show many hidden information, such as

* What compiler command line is used by this extension to execute a Python task
* Which HTML file is being used as preview.

They should indicate what might be wrong.

Python Version
--------------
If the output says ``Python X.Y is not supported``, install Python 3.11 or
above, select it with the Python extension, and reload the Visual Studio Code
window. Linting and formatting are disabled while an unsupported interpreter is
selected.

Visual Studio Code for the Web
------------------------------
In Visual Studio Code for the Web, the first formatting or linting request
loads the bundled Python runtime. A status bar message indicates when the
runtime is being loaded. Local Python installations and linter executable paths
are not used there.

Linter Configuration
--------------------
Linter processes run from the document's directory. If a linter configuration
file such as ``pyproject.toml`` or ``doc8.ini`` is not applied, verify that it
is next to the document or in a parent directory of it.

Use Developer Tools
-------------------
In rare cases you need to use ``Help | Toggle Developer Tools`` menu item to
enable Visual Studio Code's hidden Console tab. Then when you reproduce a
certain issue, you can see relevant errors recorded.

Related Resources
-----------------

- :doc:`/articles/configuration`
- :doc:`/articles/shortcuts`
- :doc:`/articles/prerequisites`
