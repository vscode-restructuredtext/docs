Linter
======

By `Lex Li`_

This article shows how the linter works.

Overview
--------
This extension can detect and launch various linters in the background to scan
the source files and report back common issues under ``PROBLEMS`` tab (which
can be opened via ``View | Problems`` menu item).

Settings
--------
To learn more about the settings, refer to :doc:`/articles/configuration`.

Supported Linters
-----------------
Three linters are currently supported,

rst-lint
::::::::
This linter provides essential rules. To install it,

.. code-block:: bash

   pip install restructuredtext_lint

doc8
::::
This linter provides enhanced rules. To install it,

.. code-block:: bash

   pip install doc8

.. note:: doc8 supersedes rst-lint, so rst-lint is disabled if doc8 is enabled.

rstcheck
::::::::
This linter provides enhanced rules. To install it,

.. code-block:: bash

   pip install rstcheck

Related Resources
-----------------

- :doc:`/articles/prerequisites`
- :doc:`/articles/shortcuts`
- :doc:`/articles/troubleshooting`
