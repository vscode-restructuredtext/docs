Live Preview
============

By `Lex Li`_

This article shows how live preview.

Shorcuts
--------
The keyboard shortcuts are

* ``ctrl+shift+r`` (on Mac ``cmd+shift+r``)               Preview
* ``ctrl+k ctrl+r`` (on Mac ``cmd+k cmd+r``)              Preview to Side

.. note:: To learn all keyboard shortcuts of this extension, please refer to
   :doc:`/articles/shortcuts`.

Rendering Engines
-----------------
This extension can compile your source files in the background, and show live
preview of the current active document.

The compilation/rendering requires an engine, and currently two of them are
supported,

* DocUtils
* Sphinx

The choice decides the performance and quality of the preview page.

DocUtils Engine
---------------
DocUtils implements the basic reStructuredText syntax, and it can render
preview based on just a single page. Therefore, if this engine is used,

* The rendering speed is super fast.
* The preview page lacks of themes.
* Certain Sphinx syntax is not rendered correctly.

Sphinx
------
Sphinx implements its own syntax on top of DocUtils, and it compiles the whole
project (based on ``conf.py``) to a website. Therefore, if this engine is used,

* The rendering speed can be slow.
* The preview page contains themed elements, and matches the final result in
  web browsers.
* All Sphinx syntax and even extensions work flawlessly.

To learn more about the settings, refer to :doc:`/articles/configuration`.

Related Resources
-----------------

- :doc:`/articles/prerequisites`
- :doc:`/articles/shortcuts`
- :doc:`/articles/troubleshooting`
