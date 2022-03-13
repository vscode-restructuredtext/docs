Editor Enhancement
==================

By `Lex Li`_

This article shows how this extension enhances the editor.

Section Builder
---------------
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

Table Editor
------------
As an experiment, table editor has been ported from Tatsuya Nakamori's
extension, which provides the following functionalities,

* Create empty table from simple text such as 3x4.
* Create formatted table from comma separated text.
* Add/delete table row/column

You can refer to this `article <https://tatsuyanakamori.github.io/vscode-reStructuredText/en/sec02_functions/table.html#creating-a-table>`_
for more information.

.. note:: To avoid conflicts with IntelliSense, the ported table editor uses a
   different approach to trigger empty table creation,

   #. Start in a new line in the editor.
   #. Type text such as 3x4.
   #. Select the text and right click.
   #. Choose the menu item "Create a grid of tables".

Related Resources
-----------------

- :doc:`/articles/configuration`
- :doc:`/articles/shortcuts`
- :doc:`/articles/troubleshooting`
