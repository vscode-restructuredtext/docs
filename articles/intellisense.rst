IntelliSense
============
This feature is disabled by default, as it is still experimental.

By `Lex Li`_

Settings
--------
To enable it at directory level, a new file ``.vscode/settings.json`` needs to
be created under the root directory shown in your Explorer tab in Visual
Studio Code.

Its default content is as below,

.. code-block:: json

    {
        "restructuredtext.languageServer.disabled": true
    }

To enable IntelliSense, change the value to ``false``,

.. code-block:: json

    {
        "restructuredtext.languageServer.disabled": false
    }

You need to restart Visual Studio Code for this change to take effect.

.. note:: You can also enable it at machine level, by making this change in
   ``Preferences -> Settings``.

Once configured properly, suggestions would be provided when pressing ``/``
after lines such as ``- :doc:`` to help input file path much quicker.
