Prerequisites
=============
This article shows what dependencies are required by different features.

Install Python for Most Features
--------------------------------
reStructuredText is a technology created by Python community, so most of the
toolchain is built upon Python. It is very important to install Python in
advance.

#. `Download Python <https://www.python.org/downloads/>`_ version 3.8 or above
   (old versions might work, but no guarantee).

   .. note:: ``pyenv`` and ``pyenv-win`` are recommended to manage multiple Python
      versions on the same machine.

   .. note:: You can refer to `Python official page <https://devguide.python.org/devcycle/#end-of-life-branches>`_
      to learn which versions should not be used.

   .. note:: Latest steps on how to install Python and Sphinx, please refer to
      `this article <https://docs.readthedocs.io/en/latest/getting_started.html#in-rst>`_.

#. Once Python is installed, make it available to this extension via either
   option,

   * Option 1: Use `the Python extension by Microsoft <https://marketplace.visualstudio.com/items?itemName=ms-python.python>`_.

     .. note:: It really makes configuring Python environment easier for users
        in this approach.

        Once you have that Python extension installed, open ``conf.py`` in
        VSCode. The Python extension shows an extra button in the status bar
        from where you can select which Python installation to use.

   * Option 2: Add Python to system path (especially on Windows).

     .. note::
      
        If you are installing on Windows, ensure both the Python install
        directory and the Python scripts directory have been added to your
        ``PATH`` environment variable.
        
        For example, if you install Python into the ``c:\python38`` directory,
        you can add ``c:\python38;c:\python38\scripts`` to your ``PATH``
        environment variable.

        However, do consider a solution like ``pyenv`` to manage multiple
        Python versions on the same machine so that you can switch easily among
        them.

   * Option 3: Use VSCode setting ``python.pythonPath`` to tell this extension
     where to locate Python.

     .. note::
        This setting is not recommended because Microsoft Python extension is
        moving away from this setting.

Virtual Environments
--------------------

Python virtual environment is partially supported,

   * ``pipenv`` users should refer to `#407 <https://github.com/vscode-restructuredtext/vscode-restructuredtext/issues/407>`_ 
   * ``venv`` users should refer to `#409 <https://github.com/vscode-restructuredtext/vscode-restructuredtext/issues/409>`_ 
   * ``conda`` users should refer to `#410 <https://github.com/vscode-restructuredtext/vscode-restructuredtext/issues/410>`_ 

.. important:: 

   Other sections of this documentation site might use commands
   such as ``pip install`` which are not virtual environment friendly.

   It is your own responsibility to replace them with virtual environment
   specific commands such as ``pipenv install`` or ``conda install``.

   You should use a solution like ``pyenv`` to manage multiple Python versions
   on the same machine so that you can switch easily among them.

Install Esbonio Language Server for Live Preview and IntelliSense
-----------------------------------------------------------------
.. danger:: Starting from version 190.1.17, this requirement is removed. You
   will be recommended to install Esbonio extension instead. To learn more
   about how to configure Esbonio, you can visit `this site <https://docs.esbon.io>`_.

Install Doc8 or RstCheck as Linter
----------------------------------
Linting support can use the ``doc8`` or ``rstcheck`` engine.

#. Install ``doc8`` to enable linter support.

   .. code-block:: text

      pip install doc8

   .. note:: If you prefer not to use ``doc8``, then this step is optional.

#. Install ``rstcheck`` to enable linter support.

   .. code-block:: text

      pip install rstcheck

   .. note:: If you prefer not to use ``rstcheck``, then this step is optional.

Related Resources
-----------------

- :doc:`/articles/configuration`
- :doc:`/articles/shortcuts`
- :doc:`/articles/troubleshooting`
