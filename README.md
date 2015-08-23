Sublime Coq
===========

Extensions to the Sublime Text 3 editor for use with the Coq Proof Assistant.

File Path
--------

You might need to modify the user preference file for Sublime-Coq, change `coqtop_path` to a proper value (usually got from `which coqtop` or similar way), so the `coqtop` program can be correctly found.

The default value will be simply `coqtop`, but during initialization, `PATH` will also be searched.


Highlighting
------------

In order to get nice background highlighting for the proven parts of the file,
add this to your theme (for light backgrounds):

```
<dict>
  <key>name</key>
  <string>Proven by Coq</string>
  <key>scope</key>
  <string>meta.coq.proven</string>
  <key>settings</key>
  <dict>
    <key>background</key>
    <string>#dcffcc</string>
  </dict>
</dict>
```

TODOs
-----
* Enrich the language spec
* Write a simple user guide
* The `undo` seems not working well sometimes


