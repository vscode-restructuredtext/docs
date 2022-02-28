Live Preview
============

By `Lex Li`_

This article shows how live preview.

Shorcuts
--------
The keyboard shortcuts are

=========================== ================= ===============
Operation                   Windows/Linux     macOS
=========================== ================= ===============
Preview                     ``ctrl+shift+r``  ``cmd+shift+r``
Preview to Side             ``ctrl+k ctrl+r`` ``cmd+k cmd+r``
=========================== ================= ===============

.. note:: To learn all keyboard shortcuts of this extension, please refer to
   :doc:`/articles/shortcuts`.

Rendering Engines
-----------------
This extension can compile your source files in the background, and show live
preview of the current active document.

The compilation/rendering requires an engine, and currently two of them are
supported,

* DocUtils
* Esbonio

The choice decides the performance and quality of the preview page.

DocUtils
--------
DocUtils implements the basic reStructuredText syntax, and it can render
preview based on just a single page. Therefore, if this engine is used,

* The rendering speed is super fast.
* The preview page lacks of themes.
* Certain Sphinx syntax is not rendered correctly.

Esbonio
-------
Esbonio is built upon Sphinx, which implements its own syntax on top of
DocUtils, and it compiles the whole project (based on ``conf.py``) to a
website. Therefore, if this engine is used,

* The rendering speed can be slow.
* The preview page contains themed elements, and matches the final result in
  web browsers.
* All Sphinx syntax and even extensions work flawlessly.

To learn more about the settings, refer to :doc:`/articles/configuration`.

.. note:: If a large project is being worked on, the very first preview might
   take a long time to show, because the first call to Sphinx takes time to
   generate all HTML pages for all source files.

   The subsequent preview pages should be much quicker to show, as those calls
   to Sphinx only generate the pages that were modified.

   More information can be found in
   `this issue <https://github.com/vscode-restructuredtext/vscode-restructuredtext/issues/211>`_ .

Related Resources
-----------------

- :doc:`/articles/prerequisites`
- :doc:`/articles/shortcuts`
- :doc:`/articles/troubleshooting`
