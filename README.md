Sublime Coq
===========

Extensions to the Sublime Text 3 editor for use with the Coq Proof Assistant.

**Note:** Coq has a great many features, and not all of them are supported in the syntax highlighter and command palette yet. If you want something or encounter a highlighting error, just [open an issue]!

[open an issue]: https://github.com/whitequark/Sublime-Coq

Getting Started
---------------

First, open your Coq script in a window, then select `Coq: Start` in the command palette. Now you should see another pane jumping out, showing the welcome message from `coqtop`.

There are several commands available now:

* **Coq: Next Statement** (OS X: `Super+Ctrl+n`, Win/Linux: `Ctrl+Down`): Prove the current line and go to next statement.
* **Coq: Undo Statement** (OS X: `Super+Ctrl+u`, Win/Linux: `Ctrl+Up`): Undo the current proven statement and go back to the last line. Undoing `Qed.` undoes the entire proof.
* **Coq: Abort Proof** (OS X: `Super+Ctrl+p`, Win/Linux: `Alt+Backspace`): In a proof, undo every tactic and the theorem definition.
* **Coq: Run Here** (OS X: `Super+Ctrl+h`, Win/Linux: `Ctrl+Enter`): Prove or undo statements until the caret position is reached.
* **Coq: Search**, **Coq: Search Pattern**, **Coq: Search Rewrite**, **Coq: Search About**: Search proofs, patterns and rewriting theorems, with results shown as you type. Press Enter to select a name from search results and insert it at caret.
* **Coq: Stop**: (OS X: `Super+Ctrl+k`, Win/Linux: `Ctrl+Escape`): Stop `coqtop` and close the output pane.

After encountering an error, press Escape to clear it and see the current goals.

Path to `coqtop`
----------------

You might need to modify the user preference file for Sublime Coq setting `coqtop_path` to a proper value (usually by running `which coqtop` in a shell), so that the `coqtop` program can be found.

If `coqtop_path` is empty, the `PATH` environment variable will be searched for a program called `coqtop`.

Highlighting
------------

In order to get nice background highlighting for the proven parts of the file, add the following snippet to your color scheme file.

For `tmTheme` syntax:

<details><summary>dark themes</summary><p>

```xml
<dict>
  <key>name</key>
  <string>Error message</string>
  <key>scope</key>
  <string>message.error</string>
  <key>settings</key>
  <dict>
    <key>foreground</key>
    <string>#cc3333</string>
  </dict>
</dict>
<dict>
  <key>name</key>
  <string>Warning message</string>
  <key>scope</key>
  <string>message.warning</string>
  <key>settings</key>
  <dict>
    <key>foreground</key>
    <string>#ffcc00</string>
  </dict>
</dict>
<dict>
  <key>name</key>
  <string>Informational message</string>
  <key>scope</key>
  <string>message.info</string>
  <key>settings</key>
  <dict>
    <key>foreground</key>
    <string>#d5d5d5</string>
    <key>background</key>
    <string>#2b2b2b</string>
  </dict>
</dict>

<dict>
  <key>name</key>
  <string>Proven with Coq</string>
  <key>scope</key>
  <string>meta.proven.coq</string>
  <key>settings</key>
  <dict>
    <key>background</key>
    <string>#058D050D</string>
    <key>foreground</key>
    <string>#05a505</string>
  </dict>
</dict>
```
</p></details>

<details><summary>light themes</summary><p>

```xml
<dict>
  <key>name</key>
  <string>Proven with Coq</string>
  <key>scope</key>
  <string>meta.proven.coq</string>
  <key>settings</key>
  <dict>
    <key>background</key>
    <string>#002800</string>
  </dict>
</dict>
```
</p></details>

For `sublime-color-scheme` syntax:

<details><summary>dark themes</summary><p>

```json
{
    "name": "Error message",
    "scope": "message.error",
    "foreground": "#cc3333"
},
{
    "name": "Warning message",
    "scope": "message.warning",
    "foreground": "#ffcc00"
},
{
    "name": "Informational message",
    "scope": "message.info",
    "foreground": "#d5d5d5",
    "background": "#2b2b2b"
},
{
    "name": "Proven with Coq",
    "scope": "meta.proven.coq",
    "background": "#058D050D",
    "foreground": "#7fa96f"
},
```
</p></details>

<details><summary>light themes</summary><p>

```json
{
    "name": "Proven with Coq",
    "scope": "meta.proven.coq",
    "background": "#002800",
},
```
</p></details>
