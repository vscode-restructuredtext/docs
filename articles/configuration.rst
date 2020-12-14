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
   the Python build to use (in case your machine has multiple Python builds
   installed). Your preference is saved to ``.vscode/settings.json`` file, and
   is then used by this extension.

   If you didn't make a choice, this extension might not be able to use the
   Python build you expected.

Live Preview
------------
The keyboard shortcuts are

* ``ctrl+shift+r`` (on Mac ``cmd+shift+r``)               Preview
* ``ctrl+k ctrl+r`` (on Mac ``cmd+k cmd+r``)              Preview to Side

.. note:: To learn all keyboard shortcuts of this extension, please refer to
   :doc:`/articles/shortcuts`.

By triggering a preview, this extension might show a list of options,

.. image:: _static/selection.png

Once an option is chosen, this extension is going to render the preview page
accordingly.

A status bar item is also added,

.. image:: _static/reset.png

By clicking this item, the selected option is reset, and the option list is
displayed once again.

You might tune the following three settings when the extension cannot locate
the generated HTML pages.

First, a new file ``.vscode/settings.json`` needs to be created under the root
directory shown in your Explorer tab in Visual Studio Code.

Its default content is as below,

.. code-block:: json

    {
        "restructuredtext.builtDocumentationPath" : "${workspaceRoot}/_build/html",
        "restructuredtext.confPath"               : "${workspaceRoot}",
        "restructuredtext.updateOnTextChanged"    : "true",
        "restructuredtext.updateDelay"            : 300,
        "restructuredtext.sphinxBuildPath"        : null
    }

.. note:: All settings are set to the default values.

A file with customized values might look as below,

.. code-block:: json

    {
        "restructuredtext.builtDocumentationPath" : "${workspaceRoot}/build/html",
        "restructuredtext.confPath"               : "${workspaceRoot}/source",
        "restructuredtext.updateOnTextChanged"    : "false",
        "restructuredtext.updateDelay"            : 1000,
        "restructuredtext.sphinxBuildPath"        : "C:\\Users\\lextm\\AppData\\Local\\Programs\\Python\\Python36\\Scripts\\sphinx-build.exe"
    }

Conf.py Path
::::::::::::
.. important:: For release 68.0.0 and above, this option is maintained
   automatically by the extension in most cases, so you don't need to modify it
   unless really neccessary.

   The meaning of this setting also changes. Now it stores the active preview
   option for the workspace/folder.

   * If it is ``""``, then docutils is used to render the preview page.
   * If it is a valid folder, then ``conf.py`` from that folder is used by
     Sphinx to render the preview page.
   * If it is not set, then this extension shows a list of options before
     generating a preview page.

   It is not recommended to use docutils, as it does not work on Sphinx
   specific features, and the preview pages can look differently.

This extension relies on Sphinx ``conf.py`` to generate preview pages.

Usually when a Sphinx project is opened, ``conf.py`` is located at the root in
Explorer folder, and that's the default value ``${workspaceRoot}`` of
``restructuredtext.confPath``.

If you have ``conf.py`` at another location, then ``restructuredtext.confPath``
should point to the proper path, such as
``${workspaceRoot}/source``.

.. note:: This should be an absolute path.

.. important:: For release 68.0.0 and above, the ``conf.py`` file must be
   located within the root folder.

Sphinx Build Path (25.0 and above)
::::::::::::::::::::::::::::::::::
The value for ``restructuredtext.sphinxBuildPath`` above depends on your Python
installation.

On Windows Python can be installed to all possible locations and does not
appear in ``PATH`` environment variable. Then you must set this value to the
proper ``sphinx-build.exe`` file path.

.. note:: This should be an absolute path.
   If you don't set this setting, but ``python.pythonPath``, then this extension
   will then pick up that setting instead. Also ``python.pythonPath`` should be
   an absolute path.

Linter
------
The linter support is based on ``rstcheck`` and ``doc8``.

Linting is automatically enabled if the linter ``rstcheck`` or ``doc8`` is
installed. The linter scans the opened files and highlights those lines with
issues detected. The PROBLEMS tab should also show all issues detected for easy
navigation.

.. note:: A warning is displayed if ``rstcheck`` or ``doc8`` cannot be found.

Executable Path
:::::::::::::::
It expects ``rstcheck`` or ``doc8`` Python module to be installed and already
added to the system path. If it is installed but not added to system path, add
the path to your preferences as seen below,

.. code-block:: json

    {
        "restructuredtext.linter.executablePath": "PathToExecutable"
    }

.. note:: This should be an absolute path.
   If you don't set this setting, but set ``python.pythonPath`` separately,
   then this extension will then pick up that setting instead. Also
   ``python.pythonPath`` should be an absolute path.

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
      "restructuredtext.linter.extraArgs": [
        "--config",
        "${workspaceFolder}/doc8.ini"
      ]
    }

.. note:: This should be an absolute path.

IntelliSense
------------
This feature is disabled by default, as it is still experimental.

To enable it at directory level, a new file ``.vscode/settings.json`` needs to
be created under the root directory shown in your Explorer tab in Visual
Studio Code.

Its default content is as below,

.. code-block:: json

    {
        "restructuredtext.languageServer.disabled": true
    }

To enable IntelliSense, change the value to ``false``,

.. code-block:: json

    {
        "restructuredtext.languageServer.disabled": false
    }

You need to restart Visual Studio Code for this change to take effect.

.. important:: The Snooty language server requires the Python package `snooty`
   to be installed. If it isn't installed yet, this extension will prompt and
   guide you through the installation.

.. note:: You can also enable it at machine level, by making this change in
   ``Preferences -> Settings``.

Once configured properly, certain language server features will be activated.

* The legacy language server provides file path suggestions when pressing ``/``
after lines such as ``- :doc:`` to help speed up input file references.
* The Snooty language server implements a different set of features.

Related Resources
-----------------

- :doc:`/articles/prerequisites`
- :doc:`/articles/shortcuts`
- :doc:`/articles/troubleshooting`
