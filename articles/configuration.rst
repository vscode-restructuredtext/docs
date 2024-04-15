Configuration
=============

By `Lex Li`_

This article shows how to configure the extension.

Sample Project
--------------
Before digging further into the configuration, please create a sample project
first.

.. code-block:: text

    mkdir sphinxtest
    cd sphinxtest
    sphinx-quickstart
    code .

The test project has the following contents, like ``makefile``, ``conf.py``,
and build folder.

Now this project is opened in Visual Studio Code.

.. important:: You also need to install prerequisites. Please refer to
   :doc:`/articles/prerequisites` for details.

.. important:: If Microsoft Python extension is installed, please first open
   ``conf.py`` of your project. The Python extension should ask you to specify
   the Python interpreter to use (in case the machine has multiple interpreters
   installed). Your preference is saved by the Python extension, and is then
   consumed by this extension.

   If you didn't make a choice, this extension might not be able to use the
   Python interpreter you expected.

   For information, please refer to :doc:`/articles/prerequisites`.

Live Preview
------------
.. danger:: Starting from version 190.1.17, this feature is removed. You will
   be recommended to install Esbonio extension instead. To learn more about how
   to configure Esbonio, you can visit `this site <https://docs.esbon.io>`_.

Linter
------
The linter support is based on ``rstcheck``, ``doc8``, and ``rst-lint``.

Linting is automatically enabled if the linters are installed. The linters
scan the opened files and highlight those lines with issues detected. The
PROBLEMS tab should also show all issues detected for easy navigation.

Executable Path
:::::::::::::::
To override automatic detection of linter modules, the following settings can
be used,

.. code-block:: json

    {
        "restructuredtext.linter.doc8.executablePath": "PathToExecutable",
        "restructuredtext.linter.rstcheck.executablePath": "PathToExecutable",
        "restructuredtext.linter.rst-lint.executablePath": "PathToExecutable"
    }

.. note:: The values should be absolute paths.

.. attention:: Linters can be disabled via the new setting,
   ``restructuredtext.linter.disabledLinters``.

.. attention:: Old settings below are obsolete since release 178.0.0,

   * ``restructuredtext.linter.disabled``
   * ``restructuredtext.linter.name``
   * ``restructuredtext.linter.executablePath``
   * ``restructuredtext.linter.extraArgs``

Lint onType or onSave or not at all
:::::::::::::::::::::::::::::::::::
By default the linter will lint on the fly but can be changed to linting as
you save. Note that linting on save is most useful when auto-save is on. Use
the setting below if to change the behavior with the values onType, onSave,
and off,

.. code-block:: json

    {
        "restructuredtext.linter.run": "onType"
    }

Linter rstchck Settings
:::::::::::::::::::::::
To be added.

Linter doc8 Settings
::::::::::::::::::::
You can configure ``doc8`` `using an ini file <https://github.com/openstack/doc8#ini-file-usage>`_.
Specify the location of the ini file in ``settings.json`` as extra args.

.. code-block:: json

    {
      "restructuredtext.linter.doc8.extraArgs": [
        "--config",
        "${workspaceFolder}/doc8.ini"
      ]
    }

.. note:: This should be an absolute path.

Security
--------
This extension runs a few third-party command-line tools found from the
locations determined by the settings such as
``restructuredtext.linter.doc8.executablePath``. Configuring them in workspace
settings allows users to conveniently select a different set of tools based on
project's need, but also allows attackers to run arbitrary binaries on your
machine if they successfully convince you to open a random repository. In order
to reduce the security risk, the extension reads those settings from user
settings by default. If the repository can be trusted and workspace settings
must be used, you can mark the workspace as a trusted workspace using the
"reStructuredText: Toggle Workspace Trust Flag" command.

Related Resources
-----------------

- :doc:`/articles/prerequisites`
- :doc:`/articles/shortcuts`
- :doc:`/articles/troubleshooting`
