Live Preview
============

By `Lex Li`_

This article shows how live preview works.

Shortcuts
---------
The keyboard shortcuts are

=========================== ================= ===============
Operation                   Windows/Linux     macOS
=========================== ================= ===============
Preview                     ``ctrl+shift+r``  ``cmd+shift+r``
Preview to Side             ``ctrl+k ctrl+r`` ``cmd+k cmd+r``
=========================== ================= ===============

.. note:: To learn all keyboard shortcuts of this extension, please refer to
   :doc:`/articles/shortcuts`.

Settings
--------
To learn more about the settings, refer to :doc:`/articles/configuration`.

Preview Mode Selection
----------------------
By triggering a preview, this extension might show a list of options,

.. image:: _static/selection.png

Once an option is chosen, this extension is going to render the preview page
accordingly.

A status bar item is also added,

.. image:: _static/reset.png

By clicking this item, the selected option is reset, and the option list is
displayed once again.

Explanation on Preview Modes
----------------------------
To show live preview pages, a mode is required to generate HTML from source
files. Currently two modes are supported,

* Esbonio
* DocUtils

Esbonio
:::::::
.. warning:: Esbonio language server must be enabled for live preview to work
   properly since release 171.0.0.

   If live preview does not work, verify if "esbonio:" is visible in the
   status bar. Read "IntelliSense" section for more details.

If you are working on a Sphinx project, then this mode is highly recommended.

Esbonio is built upon Sphinx, which implements a rich set of syntax on top of
what DocUtils offers, and it compiles the whole project (based on settings in
``conf.py``) to a complete website. Its features are,

* The rendering speed can be slow sometimes.
* The preview page contains themed elements, and matches the final result in
  web browsers.
* All Sphinx syntax and even extensions work flawlessly.

.. note:: If a large project is being worked on, it takes Esbonio a long while
   to compile the project behind the scene. Monitor "esbonio:" in status bar,
   so that you only trigger live preview when it finishes compiling.

DocUtils
::::::::
DocUtils implements the very basic reStructuredText syntax, and it can render
simple HTML pages even in worst cases. Its features are,

* The rendering speed is super fast.
* The preview page lacks of themes.
* Certain Sphinx syntax is not rendered correctly.

This mode is only used as fallback in most cases.

Related Resources
-----------------

- :doc:`/articles/prerequisites`
- :doc:`/articles/shortcuts`
- :doc:`/articles/troubleshooting`
