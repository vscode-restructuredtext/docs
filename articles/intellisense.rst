IntelliSense
============

This feature is enabled by default, though it is still experimental. There is
no way to disable it at this moment, as you will also lose live preview.

By `Lex Li`_

The Esbonio language server implements many useful features.

.. important:: The Esbonio language server requires the Python package
   ``esbonio`` to be installed. If it isn't installed yet, this
   extension will prompt and guide you through the installation.

Autocompletion
--------------
The language server enables autocompletion on role/directive names, file paths,
as well as parameters.

Please refer to `Esbonio documentation`_ to learn more.

Document links
--------------

.. warning:: this feature is temporarily not available.

Directives like ``image``, ``figure``, ``include``, and ``literalinclude`` now
displayed as file links. You can use those links to jump to the linked files.

Cross-referencing documents (aka ``doc`` role) are also transformed as links.

Related Resources
-----------------

- :doc:`/articles/configuration`
- :doc:`/articles/shortcuts`
- :doc:`/articles/troubleshooting`

.. _Esbonio documentation: https://swyddfa.github.io/esbonio/docs/stable/en/#language-server
