Section Builder
===============

By `Lex Li`_

Sphinx supports a few underline characters that can be used in section headers,
such as '=', '-', ':', '.', '\'', '"', '~', '^', '*', '+', and '#'.

.. note:: Though '`' and '_' are also valid in Sphinx syntax, the syntax file
   used by this extension does not work well with them. So these two are not
   supported by this feature.

The most common shortcut to use is ``ctrl+k ctrl+=`` (on Mac ``cmd+k cmd+=``).

Pressing the shortcut key would convert the current line under the cursor to
a section, by adding adornment (underlines below the title text).

Pressing the shortcut key multiple times switches among the adornment
characters.

.. important:: Starting from 78.0.0, you might also use ``ctrl+k ctrl+-`` (on
   Mac ``cmd+k cmd+-``). The difference is that this command choose characters
   in the reverse order.
