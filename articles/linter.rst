Linter
======

By `Lex Li`_

This article shows how the linter works.

doc8
----
The linter support is initially based on de facto tool called doc8, which
provides the best-in-class rules for reStructuredText files.

Based on the configuration, this extension launches doc8 in the background to
scan the source files and reports back identified issues under ``PROBLEMs`` tab
(can be opened via ``View | Problems`` menu item).

rstcheck
--------
doc8 was not actively maintained, so rstcheck was chosen as the new linter,
which became the default in release 120.0.0.

To learn more about the settings, refer to :doc:`/articles/configuration`.

Related Resources
-----------------

- :doc:`/articles/prerequisites`
- :doc:`/articles/shortcuts`
- :doc:`/articles/troubleshooting`
