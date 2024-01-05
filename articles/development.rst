Hacking the Source Code
=======================

By `Lex Li`_

Build from source
-----------------
#. Clone the repo to a local path such as ``/Users/someuser/vscode-restructuredtext``.
#. Navigate to this folder.
#. Resolve Node.js dependencies via ``yarn install`` .
#. Build via ``yarn compile`` .
#. Configure Sphinx following :doc:`/articles/configuration` .
#. Run VS Code from this folder via ``code .`` .
#. In this editing VS Code instance, press F5 to start a debugging instance.

.. code-block:: text

    cd /Users/someuser
    git clone https://github.com/vscode-restructuredtext/vscode-restructuredtext.git
    cd vscode-restructuredtext
    yarn install
    yarn compile
    code .

.. note:: To configure the ``code`` command, please follow `this guide <https://code.visualstudio.com/docs/setup/setup-overview>`_ .

You can now open a test folder in this debugging instance.

Debugging with Esbonio
----------------------
.. danger:: Starting from version 190.1.17, this feature is removed. You will
   be recommended to install Esbonio extension instead. To learn more about how
   to configure Esbonio, you can visit `this site <https://docs.esbon.io>`_.

To debug the language server, clone its source code from GitHub,

.. code-block:: shell

    cd /Users/someuser
    git clone https://github.com/swyddfa/esbonio.git

and then edit the settings of the test folder to include Esbonio source folder,

.. code-block:: json

    {
        "esbonio.server.sourceFolder": "/Users/someuser/esbonio/lib/esbonio",
        "esbonio.server.debugLaunch": false
    }

Now restart the VSCode instance being debugged, so that the extension picks up
this change and prepares the debugging environment by removing installed
esbonio package and loading esbonio from the source with debugpy enabled for
debugging.

.. note:: If everything is configured properly, you should see `debugpy is at port
   5678. Connect and debug.`

.. note:: If you want to debug initialization, then change `esbonio.server.debugLaunch`
   to `true`.

Then launch another VSCode instance and open esbonio source folder in it.

Make sure its `launch.json` contains the following profile,

.. code-block:: json

    {
        "configurations": [
            {
                "name": "Python: Remote Attach",
                "type": "python",
                "request": "attach",
                "connect": {
                    "host": "localhost",
                    "port": 5678
                },
                "pathMappings": [
                    {
                        "localRoot": "${workspaceFolder}/lib/esbonio",
                        "remoteRoot": "."
                    }
                ]
            }
        ]
    }

Start debugging with `Python: Remote Attach` profile and this VSCode instance
will attach to the language server via port 5678. All debugging features like
break points should work.

Publish to Marketplace
----------------------
To publish this extension, use `vsce <https://code.visualstudio.com/docs/tools/vscecli>`_ .

.. code-block:: text

    cd /Users/someuser
    git clone https://github.com/vscode-restructuredtext/vscode-restructuredtext.git
    cd vscode-restructuredtext
    vsce publish

Related Resources
-----------------

- :doc:`/articles/configuration`
- :doc:`/articles/shortcuts`
- :doc:`/articles/troubleshooting`
