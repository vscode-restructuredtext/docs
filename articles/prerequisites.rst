Prerequisites
=============
This article shows what dependencies are required by different features.

Install Python for Most Features
--------------------------------
reStructuredText is a technology created by Python community, so most of the
toolchain is built upon Python. It is very important to install Python in
advance.

#. `Download python <https://www.python.org/downloads/>`_ version 3.4 or above
   (2.x might work, but no guarantee).

#. If you are installing on Windows, ensure both the Python install directory
   and the Python scripts directory have been added to your ``PATH``
   environment variable. For example, if you install Python into the
   ``c:\python34`` directory, you can add ``c:\python34;c:\python34\scripts``
   to your ``PATH`` environment variable.

.. important:: It is recommended that you install
   `the Python extension by Microsoft <https://marketplace.visualstudio.com/items?itemName=ms-python.python>`_.
   It really makes configuring Python environment easier for users.

.. note:: Latest steps on how to install Python and Sphinx, please refer to
   `this article <https://docs.readthedocs.io/en/latest/getting_started.html#in-rst>`_.

.. important:: Python virtualenv is supported, but its setup is complex and not
   documented here yet.

Install DocUtils or Sphinx for Live Preview
-------------------------------------------
Live preview requires either DocUtils or Sphinx to be installed in advance, as
rendering engine to generate the HTML page for preview. The selection of
rendering engine and Sphinx ``conf.py`` files can be made by clicking the
status button. Please refer to :doc:`/articles/configuration` for details.

#. Install DocUtls by opening a command prompt and running the following Python
command,

   .. code-block:: text

      pip install docutils

   .. note:: If you prefer Sphinx based preview, then this step is optional.

#. Install Sphinx by opening a command prompt and running the following Python
command,

   .. code-block:: text

      pip install sphinx sphinx-autobuild

   .. note:: This operation might take a few minutes to complete.

      If you prefer DocUtils based preview, then this step is optional.

.. note:: Some Sphinx themes require their own Python packages to be installed.
          You should check the documentation of the themes you use so as to
          know which packages to install, or the preview error page contains
          the actual package name which is missing.

Install Doc8 as Linter
-----------------------
Linting support can use the doc8 engine.

#. Install ``doc8`` to enable linter support.

   .. code-block:: text

      pip install doc8

   .. note:: If you prefer not to use linter, then this step is optional.

Install RstCheck as Linter
-----------------------
Linting support can use the rstcheck engine.

#. Install ``rstcheck`` to enable linter support.

   .. code-block:: text

      pip install rstcheck

   .. note:: If you prefer not to use linter, then this step is optional.

Related Resources
-----------------

- :doc:`/articles/configuration`
- :doc:`/articles/shortcuts`
- :doc:`/articles/troubleshooting`
