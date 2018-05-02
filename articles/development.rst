Hacking the Source Code
=======================

By `Lex Li`_

Build from source
-----------------
#. Clone the repo to a local path such as ``~/vscode-restructuredtext`` .
#. Navigate to this folder.
#. Resolve NPM dependencies via ``npm install`` .
#. Build via ``npm run compile`` .
#. Configure Sphinx following :doc:`/articles/configuration` .
#. Run VS Code from this folder via ``code .`` .
#. In this editing VS Code instance, press F5 to start a debugging instance.

.. code-block:: text

    cd ~
    git clone https://github.com/vscode-restructuredtext/vscode-restructuredtext.git
    cd ~/vscode-restructuredtext
    npm install
    npm run compile
    code .

.. note:: To configure the ``code`` command, please follow `this guide <https://code.visualstudio.com/docs/setup/setup-overview>`_ .

Publish to Marketplace
----------------------
To publish this extension, use `vsce <https://code.visualstudio.com/docs/tools/vscecli>`_ .

.. code-block:: text

    cd ~
    git clone https://github.com/vscode-restructuredtext/vscode-restructuredtext.git
    cd ~/vscode-restructuredtext
    vsce publish
