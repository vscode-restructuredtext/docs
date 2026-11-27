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

Linter processes run from the document's directory, so tool configuration such
as ``pyproject.toml`` or ``doc8.ini`` is discovered next to the document.

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

.. attention:: Upgrade or install recommendations for linter tools can be
   disabled via ``restructuredtext.linter.installRecommendation.disabled``.

.. attention:: Old settings below are obsolete since release 178.0.0,

   * ``restructuredtext.linter.disabled``
   * ``restructuredtext.linter.name``
   * ``restructuredtext.linter.executablePath``
   * ``restructuredtext.linter.extraArgs``

Lint onType or onSave or not at all
:::::::::::::::::::::::::::::::::::
By default the linter runs as you type but can be changed to linting as you
save. Note that linting on save is most useful when auto-save is on. Use the
setting below to change the behavior with the values onType, onSave, and off,

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

Formatter
---------
Formatting is based on ``rstformat``. It can format the whole document or the
current selection. On desktop it requires Python 3.11 or above and
``rstformat`` installed as described in :doc:`/articles/prerequisites`; in
Visual Studio Code for the Web it is bundled.

Use the ``Format Document`` or ``Format Selection`` command, or the default
``Shift+Alt+F`` (Windows/Linux) / ``Shift+Option+F`` (macOS) shortcut.

Formatter Settings
::::::::::::::::::
The following settings control formatting,

.. code-block:: json

    {
        "restructuredtext.formatter.normalizeSectionUnderlines": true,
        "restructuredtext.formatter.normalizeSectionSpacing": true,
        "restructuredtext.formatter.trimTrailingWhitespace": true,
        "restructuredtext.formatter.maxConsecutiveBlankLines": 2
    }

``normalizeSectionUnderlines`` adjusts section underline and overline widths to
the title text. ``normalizeSectionSpacing`` inserts a blank line before and
after section titles when needed. ``trimTrailingWhitespace`` removes trailing
spaces and tabs. ``maxConsecutiveBlankLines`` limits how many consecutive
blank lines are preserved.

Visual Studio Code for the Web
------------------------------
Since release 190.4.14, linting and formatting are available in Visual Studio
Code for the Web through a Python runtime bundled with this extension. Local
Python installations, linter executable paths, and ``pip install`` commands do
not apply in that environment; bundled tools are updated together with the
extension.

Security
--------
This extension runs a few third-party command-line tools found from the
locations determined by settings such as
``restructuredtext.linter.doc8.executablePath``. Configuring them in workspace
settings allows users to conveniently select a different set of tools based on
a project's needs, but also allows attackers to run arbitrary binaries on your
machine if they convince you to open a random repository. The extension
declares that it is not supported in untrusted workspaces, so Visual Studio
Code disables it in Restricted Mode. To use workspace or folder-level tool
paths, trust the workspace through Visual Studio Code's Workspace Trust
interface.

Related Resources
-----------------

- :doc:`/articles/prerequisites`
- :doc:`/articles/shortcuts`
- :doc:`/articles/troubleshooting`
