# RadWindow CodeSnippet shortcuts for Visual Studio

## Table of contents

| Shortcut | Language| Description |
| --- | --- | --- |
| [`radwindowbtn`](#radwindow) | HTML | RadWindow control markup with show window button |

## Markup

### RadWindow 
- shortcut: radwindowbtn
- filename: radwindowbtn.snippet
- default destination: 'C:\Users\\{USERNAME}\Documents\Visual Studio 2015\Code Snippets\Visual Web Developer\My HTML Snippets'

<details>
<summary>Generated code (Click here to expand)</summary>

```html
<telerik:RadWindow runat="server" ID="RadWindow1" Width="1000" Height="1000" VisibleOnPageLoad="true"
    NavigateUrl="Default2.aspx">
</telerik:RadWindow>
<telerik:RadButton runat="server" OnClientClicked="OnClientClicked" ID="RadButton1" Text="Show Window" AutoPostBack="false" />
<script>
    function OnClientClicked(sender, args) {
        var wnd = $find("<%= RadWindow1.ClientID %>");
        wnd.show();
    }
</script>
```

</details>

