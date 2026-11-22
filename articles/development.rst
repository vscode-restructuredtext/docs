Hacking the Source Code
=======================

By `Lex Li`_

Build from source
-----------------
#. Clone the repo to a local path such as ``/Users/someuser/vscode-restructuredtext``.
#. Navigate to this folder.
#. Resolve Node.js dependencies via ``npm ci`` .
#. Build via ``npm run compile`` .
#. Configure Sphinx following :doc:`/articles/configuration` .
#. Run VS Code from this folder via ``code .`` .
#. In this editing VS Code instance, press F5 to start a debugging instance.

.. code-block:: text

    cd /Users/someuser
    git clone https://github.com/vscode-restructuredtext/vscode-restructuredtext.git
    cd vscode-restructuredtext
    npm ci
    npm run compile
    code .

.. note:: To configure the ``code`` command, please follow `this guide <https://code.visualstudio.com/docs/setup/setup-overview>`_ .

You can now open a test folder in this debugging instance.

Tests
-----
The following commands are available,

============================== =============================================
Command                        Description
============================== =============================================
``npm run typecheck``          Type checks the extension and tests.
``npm run test:unit``          Runs unit tests without starting VS Code.
``npm run test-node``          Runs desktop integration tests in VS Code.
``npm run test-node-linters``  Runs the linter version matrix.
``npm run test-web``           Runs integration tests in VS Code for the Web.
============================== =============================================

.. note:: ``test-node`` downloads a VS Code build on first use.
   ``test-node-linters`` prepares the virtual environments under
   ``.venv-linter-tests``. ``test-web`` uses Playwright Chromium and stores
   its downloads under ``.vscode-test-web``.

.. note:: Since release 190.4.14, the web build bundles Pyodide and the
   supported Python tools. ``npm run compile`` downloads the required Pyodide
   package wheels and verifies them against the Pyodide lock file before they
   are packaged.

Debugging with Esbonio
----------------------
.. danger:: Starting from version 190.1.17, this feature is removed. You will
   be recommended to install Esbonio extension instead. To learn more about how
   to configure Esbonio, you can visit `this site <https://docs.esbon.io>`_.

Publish to Marketplace
----------------------
To publish this extension, use `vsce <https://code.visualstudio.com/docs/tools/vscecli>`_ .

.. note:: Create the release tag before packaging. The build reads the version
   from ``git describe`` before producing the VSIX.

.. code-block:: text

    cd /Users/someuser
    git clone https://github.com/vscode-restructuredtext/vscode-restructuredtext.git
    cd vscode-restructuredtext
    npm ci
    npx vsce package
    npx vsce publish

Related Resources
-----------------

- :doc:`/articles/configuration`
- :doc:`/articles/shortcuts`
- :doc:`/articles/troubleshooting`
