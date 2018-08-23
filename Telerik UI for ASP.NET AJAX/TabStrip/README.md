# RadTabStrip CodeSnippet shortcuts for Visual Studio

## Table of contents

| Shortcut | Language| Description |
| --- | --- | --- |
| [`radtabstripmp`](#tabstrip-control-with-multipage) | HTML | TabStrip control markup with related MultiPage control |

## Markup

### TabStrip control with MultiPage
- shortcut: radtabstripmp
- filename: radtabstripmp.snippet
- default destination: 'C:\Users\\{USERNAME}\Documents\Visual Studio 2015\Code Snippets\Visual Web Developer\My HTML Snippets'

<details>
<summary>Generated code (Click here to expand)</summary>

```html
<telerik:RadTabStrip runat="server" ID="RadTabStrip1" MultiPageID="RadMultiPage1">
    <Tabs>
        <telerik:RadTab Text="Tab 1"></telerik:RadTab>
        <telerik:RadTab Text="Tab 2"></telerik:RadTab>
        <telerik:RadTab Text="Tab 3"></telerik:RadTab>
    </Tabs>
</telerik:RadTabStrip>
<telerik:RadMultiPage runat="server" ID="RadMultiPage1" SelectedIndex="0">
    <telerik:RadPageView ID="RadPageView1" runat="server">
        Page 1
    </telerik:RadPageView>
    <telerik:RadPageView ID="RadPageView2" runat="server">
        Page 2
    </telerik:RadPageView>
    <telerik:RadPageView ID="RadPageView3" runat="server">
        Page 3
    </telerik:RadPageView>
</telerik:RadMultiPage>
```

</details>

