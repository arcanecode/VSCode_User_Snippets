# Enable Intellisense in VSCode for MarkDown Files

By default, intellisense for Markdown files in VSCode is Disabled. It is possible to activate a user snippet without Intellisense enabled, but honestly it's a pain in the butt. It's much easier to use snippets with intellisense turned on.

To enable intellisense for MarkDown files, open your settings.json file and add these lines:

```json
"[markdown]": {
  "editor.quickSuggestions": {
    "other": true,
    "comments": false,
    "strings": true
  },
},
```

(If you insert the above code at the very bottom of your settings.json file, then omit that final comma)

Giving credit where it is due, I found the solution to enable intellisense in this StackOverflow article:

[https://stackoverflow.com/questions/43639841/how-to-set-markdown-snippet-trigger-automatically](https://stackoverflow.com/questions/43639841/how-to-set-markdown-snippet-trigger-automatically)
