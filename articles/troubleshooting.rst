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
