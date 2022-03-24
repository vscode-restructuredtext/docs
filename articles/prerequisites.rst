Prerequisites
=============
This article shows what dependencies are required by different features.

Install Python for Most Features
--------------------------------
reStructuredText is a technology created by Python community, so most of the
toolchain is built upon Python. It is very important to install Python in
advance.

#. `Download python <https://www.python.org/downloads/>`_ version 3.6 or above
   (old versions might work, but no guarantee).

   .. note:: You can refer to `Python official page <https://devguide.python.org/devcycle/#end-of-life-branches>`_
      to learn which versions should not be used.

   .. note:: Latest steps on how to install Python and Sphinx, please refer to
      `this article <https://docs.readthedocs.io/en/latest/getting_started.html#in-rst>`_.

#. Once Python is installed, make it available to this extension via either
   option,

   * Option 1: Add Python to system path (especially on Windows).

     .. note:: If you are installing on Windows, ensure both the Python install
        directory and the Python scripts directory have been added to your
        ``PATH`` environment variable. For example, if you install Python into
        the ``c:\python36`` directory, you can add
        ``c:\python36;c:\python36\scripts`` to your ``PATH`` environment
        variable.

   * Option 2: Use `the Python extension by Microsoft <https://marketplace.visualstudio.com/items?itemName=ms-python.python>`_.

     .. note:: It really makes configuring Python environment easier for users
        in this approach.

        Once you have that Python extension installed, open ``conf.py`` in
        VSCode. The Python extension shows an extra button in the status bar
        from where you can select which Python installation to use.

   * Option 3: Use VSCode setting ``python.pythonPath`` to tell this extension
     where to locate Python.

.. important:: Python virtualenv is partially supported, but its setup is
   complex and not documented here yet. Many issues are expected.

Install Esbonio Language Server for Live Preview and IntelliSense
-----------------------------------------------------------------

Esbonio language server provides both IntelliSense and live preview
functionalities, so it must be installed in advance, as
rendering engine to generate the HTML page for preview.

..note:: In case you really want to avoid Esbonio and Sphinx for live preview,
  you can select DocUtils. Please refer to :doc:`/articles/configuration` for
  details.

#. Install Esbonio by opening a command prompt and running the following Python
   command,

   .. code-block:: text

      pip install esbonio

   .. note:: This operation might take a few minutes to complete.

      If you prefer DocUtils based preview, then this step is optional.

   .. note:: Some Sphinx themes require their own Python packages to be
      installed. You should check the documentation of the themes you use so as
      to know which packages to install, or the preview error page contains the
      actual package name which is missing.

#. Install DocUtils by opening a command prompt and running the following Python
   command,

   .. code-block:: text

      pip install docutils

   .. note:: If you prefer Esbonio based preview, then this step is optional.

Install Doc8 or RstCheck as Linter
----------------------------------
Linting support can use the doc8 or rstcheck engine.

#. Install ``doc8`` to enable linter support.

   .. code-block:: text

      pip install doc8

   .. note:: If you prefer not to use doc8, then this step is optional.

#. Install ``rstcheck`` to enable linter support.

   .. code-block:: text

      pip install rstcheck

   .. note:: If you prefer not to use rstcheck, then this step is optional.

Related Resources
-----------------

- :doc:`/articles/configuration`
- :doc:`/articles/shortcuts`
- :doc:`/articles/troubleshooting`
