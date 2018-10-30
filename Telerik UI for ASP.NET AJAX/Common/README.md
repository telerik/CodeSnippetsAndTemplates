# Common CodeSnippet shortcuts for Visual Studio

## Table of contents

| Shortcut | Language| Description |
| --- | --- | --- |
| [`pageload`](#ajax-pageload) | JS | Markup for the Sys.Application.add_load() |
| [`handlertelerik`](#telerik-client-events-handler) | JS | Markup for a sample Telerik client-side event handler |
| [`find`](#find) | JS | Markup for the $find() |
| [`startupscriptregister`](#scriptmanager-registerstartupscript) | C# | Syntax for [executing code from server](https://docs.telerik.com/devtools/aspnet-ajax/controls/window/troubleshooting/executing-javascript-code-from-server#when-using-aspnet-ajax) |

## Markup

### AJAX pageLoad
- shortcut: pageload
- filename: pageloadSnippet.snippet
- default destination: 'C:\Users\\{USERNAME}\Documents\Visual Studio 2015\Code Snippets\JavaScript\My Code Snippets'

<details>
<summary>Generated code (Click here to expand)</summary>

```js
function pageLoadHandler() {
        $selected$ $end$
        // Sys.Application.remove_load(pageLoadHandler);  
    } 
  Sys.Application.add_load(pageLoadHandler);
```

</details>

### Telerik client events handler
- shortcut: handlertelerik
- filename: eventhandler.snippet
- default destination: 'C:\Users\\{USERNAME}\Documents\Visual Studio 2015\Code Snippets\JavaScript\My Code Snippets'

<details>
<summary>Generated code (Click here to expand)</summary>

```js
function (sender, args) {

}
```

</details>


### $find()
- shortcut: find
- filename: findControl.snippet
- default destination: 'C:\Users\\{USERNAME}\Documents\Visual Studio 2015\Code Snippets\JavaScript\My Code Snippets'

<details>
<summary>Generated code (Click here to expand)</summary>

```js
$find("<%= RadControl1.ClientID %>");
```

</details>

## Code-behind - C#

### ScriptManager RegisterStartupScript
- shortcut: startupscriptregister
- filename: RegisterStartupScript.snippet
- default destination: 'C:\Users\\{USERNAME}\Documents\Visual Studio 2015\Code Snippets\Visual C#\My Code Snippets'

<details>
<summary>Generated code (Click here to expand)</summary>

```cs
string scriptstring = "window.frameElement.radWindow.Close();";
ScriptManager.RegisterStartupScript(Page, Page.GetType(), "closewindow", scriptstring, true);
```

</details>
