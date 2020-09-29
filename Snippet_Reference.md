# Snippet Reference

Here is an example of a user snippet I created for PowerShell.

```json
  "PowerShell File Header": {
		"prefix": "pshead",
		"body": [
"<#-------------------------------------------------------------------------------------------------",
"  Data Fabricator - $TM_FILENAME",
"  Author: Robert C. Cain | @ArcaneCode | arcane@arcanetc.com",
"		       http://arcanecode.me",
"",
"  This code is Copyright (c) $CURRENT_YEAR Robert C. Cain. All rights reserved.",
"",
"  The code herein is for demonstration purposes. No warranty or guarantee",
"  is implied or expressly granted.",
"",
"  This module may not be reproduced in whole or in part without the express",
"  written consent of the author. ",
"-----------------------------------------------------------------------------------------------#>",
""
		],
    "description": "File Header for PowerShell Headers"
  }
```

The first line is the formal name of the snippet ("PowerShell File Header")

The ```prefix``` is what you type in to trigger the use of the snippet.

The ```body``` is the text that will be inserted. Note that you can indent the body text under the body tag if you wish. I usually do, but github didn't format it correctly for the code sample so I removed the indentions for this example.

The ```description``` is descriptive text that appears beside the prefix when intellisense is activated.

Note that when you have multiple snippets, there must be a comma after the closing ```}``` except for the very last snippet in your file.

Here is a sample of what the previous snippet created:

```powershell
<#-------------------------------------------------------------------------------------------------
  Data Fabricator - Execute-Tests.ps1
  Author: Robert C. Cain | @ArcaneCode | arcane@arcanetc.com
           http://arcanecode.me

  This code is Copyright (c) 2020 Robert C. Cain. All rights reserved.

  The code herein is for demonstration purposes. No warranty or guarantee
  is implied or expressly granted.

  This module may not be reproduced in whole or in part without the express
  written consent of the author. 
-----------------------------------------------------------------------------------------------#>
```

Note how the variables correctly inserted the file name, as well as the year for the copyright date.

## Escape characters

Embedded double quotes use \"

Dollar signs $ are escaped with \\\\$   (Two backslashes)

Escape a \ with two backslashes \\\\

```$0``` is where it will place the cursor after inserting the snippet, such as this example:

```json
		"body": [
			"#------------------------------------------------------------------------------------------------",
			"#  $0"
			"#------------------------------------------------------------------------------------------------",
			""
		],
```

You can also use ```$1```, ```$2```... and will be able to use the TAB key to jump between these immediately after a snippet is inserted.

## Variables

Snippets also supports variables, such as the $TM_FILENAME or $CURRENT_YEAR in the top example, Here is a list.

    TM_SELECTED_TEXT The currently selected text or the empty string
    TM_CURRENT_LINE The contents of the current line
    TM_CURRENT_WORD The contents of the word under cursor or the empty string
    TM_LINE_INDEX The zero-index based line number
    TM_LINE_NUMBER The one-index based line number
    TM_FILENAME The filename of the current document
    TM_FILENAME_BASE The filename of the current document without its extensions
    TM_DIRECTORY The directory of the current document
    TM_FILEPATH The full file path of the current document
    CLIPBOARD The contents of your clipboard
    WORKSPACE_NAME The name of the opened workspace or folder

For inserting the current date and time:

    CURRENT_YEAR The current year
    CURRENT_YEAR_SHORT The current year's last two digits
    CURRENT_MONTH The month as two digits (example '02')
    CURRENT_MONTH_NAME The full name of the month (example 'July')
    CURRENT_MONTH_NAME_SHORT The short name of the month (example 'Jul')
    CURRENT_DATE The day of the month
    CURRENT_DAY_NAME The name of day (example 'Monday')
    CURRENT_DAY_NAME_SHORT The short name of the day (example 'Mon')
    CURRENT_HOUR The current hour in 24-hour clock format
    CURRENT_MINUTE The current minute
    CURRENT_SECOND The current second
    CURRENT_SECONDS_UNIX The number of seconds since the Unix epoch

For inserting line or block comments, honoring the current language:

    BLOCK_COMMENT_START Example output: in PHP /* or in HTML <!--
    BLOCK_COMMENT_END Example output: in PHP */ or in HTML -->
    LINE_COMMENT Example output: in PHP //

## For more information, please see the Visual Studio Code documentation at:

[https://code.visualstudio.com/docs/editor/userdefinedsnippets](https://code.visualstudio.com/docs/editor/userdefinedsnippets )

## MarkDown Snippets

Note that by default, intellisense is not enabled in MarkDown files within VSCode, making them harder to use. See the article [Enable_Intellisense_In_MarkDown.md](Enable_Intellisense_In_MarkDown.md) in this repository for instructions on how to enable it.

---

## Author Information

### Author

Robert C. Cain | [@ArcaneCode](https://twitter.com/arcanecode) | arcanecode@gmail.com

### Websites

About Me: [http://arcanecode.me](http://arcanecode.me)

Blog: [http://arcanecode.com](http://arcanecode.com)

Github: [http://arcanerepo.com](http://arcanerepo.com)

LinkedIn: [http://arcanecode.in](http://arcanecode.in)

### Copyright Notice

This document is Copyright (c) 2020 Robert C. Cain. All rights reserved.

The code samples herein is for demonstration purposes. No warranty or guarantee is implied or expressly granted.

This document may not be reproduced in whole or in part without the express written consent of the author and/or Pluralsight. Information within can be used within your own projects.
