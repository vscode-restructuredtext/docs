Project History
===============

By `Lex Li`_

Microsoft introduced Visual Studio Code on April 29, 2015, and later released
it as an open source project [1]_ on November 18, 2015.

An issue was opened on Nov 18, 2015 [2]_ to add reStructuredText support to
Visual Studio Code. Lex Li responded to the issue and started to work on the
initial version of this extension, with only syntax highlighting and code
snippets ported from TextMate.

Inspired by the extension created by Thomas Townsend [3]_ , the live preview
feature was added in release 0.0.7, and fully switched to Sphinx based preview
engine in release 0.0.14.

Linter support was added in release 33.0.0, by reusing some code from Cody
Hoover's ruby-linter extension [4]_ . restructured-lint was chosen initially,
and later doc8 support was added in release 53.0.0. Recently rstcheck has been
chosen to replace doc8 in release 120.0.0.

Section builder was contributed by Adrien Di Mascio in release 44.0.0 [5]_ .

A language server project was started recently [6]_ to enable IntelliSense.
IntelliSense was included in release 47.0.0, and was disabled by default.

Tormod Landet introduced many important pieces in June/July 2018, which boost
productivity and simplified user experience [7]_ . The changes were shipped in
release 67.0.0 and above.

noisnemid added initial outline support [8]_ in release 118.0.0.

A new linter named rstcheck [9]_ was integrated in release 120.0.0 and became
the default.

Starting from release 131.0.0, the Snooty language server created by MongoDB
[10]_ was integrated. The legacy server was removed in release 137.0.0.

List editing was ported from Yu Zhang's extension [11]_ in release 143.0.0.

Table editor was ported from Tatsuya Nakamori's extension [12]_ in release
158.0.0.

Starting from release 154.0.0, this extension switched to the syntax
highlighting implemented by Trond Snekvik. Release 159.0.0 completely removed
syntax highlighiting and recommends Trond's extension [13]_ instead.

Starting from release 170.0.0, the Esbonio language server created by Alex
Carney [14]_ was integrated. The integration with Snooty was removed. As the
Esbonio project evolves quickly, this project no longer offers live preview and
IntelliSense features, but recommends the Esbonio extension to be installed
instead since release 190.1.17.

There are other contributors helping out with bug reports and pull requests.

.. rubric:: Footnotes

.. [1] https://en.wikipedia.org/wiki/Visual_Studio_Code
.. [2] https://github.com/Microsoft/vscode/issues/117
.. [3] https://github.com/tht13/RST-vscode/
.. [4] https://marketplace.visualstudio.com/items?itemName=hoovercj.ruby-linter
.. [5] https://github.com/vscode-restructuredtext/vscode-restructuredtext/pull/66
.. [6] https://github.com/lextm/restructuredtext-antlr
.. [7] https://blog.lextudio.com/important-update-on-restructuredtext-for-vscode-efa0d412422f
.. [8] https://github.com/vscode-restructuredtext/vscode-restructuredtext/pull/199
.. [9] https://github.com/myint/rstcheck
.. [10] https://github.com/vscode-restructuredtext/snooty-parser
.. [11] https://github.com/yzhang-gh/vscode-markdown
.. [12] https://github.com/TatsuyaNakamori/vscode-reStructuredText
.. [13] https://github.com/trond-snekvik/vscode-rst
.. [14] https://github.com/swyddfa/esbonio

Related Resources
-----------------

- :doc:`/articles/configuration`
- :doc:`/articles/shortcuts`
- :doc:`/articles/troubleshooting`
