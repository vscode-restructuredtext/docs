Section Builder
===============

By `Lex Li`_

Sphinx supports a few underline characters that can be used in section headers,
such as '=', '-', ':', '.', '\'', '"', '~', '^', '*', '+', and '#'.

.. note:: Though '`' and '_' are also valid in Sphinx syntax, the syntax file
   used by this extension does not work well with them. So these two are not
   supported by this feature.

The keyboard shortcuts are,

=========================== ================= ===============
Operation                   Windows/Linux     macOS
=========================== ================= ===============
Insert Adornment            ``ctrl+k ctrl+=`` ``cmd+k cmd+=``
Insert Adornment (Reversed) ``ctrl+k ctrl+-`` ``cmd+k cmd+-``
=========================== ================= ===============

.. note:: To learn all keyboard shortcuts of this extension, please refer to
   :doc:`/articles/shortcuts`.

Pressing the shortcut key would convert the current line under the cursor to
a section, by adding adornment (underlines below the title text).

Pressing the shortcut key multiple times switches among the adornment
characters.

Related Resources
-----------------

- :doc:`/articles/configuration`
- :doc:`/articles/shortcuts`
- :doc:`/articles/troubleshooting`
