# RadWizard CodeSnippet shortcuts for Visual Studio

## Table of contents

| Shortcut | Language| Description |
| --- | --- | --- |
| [`radwizard`](#wizard-control-with-steps) | HTML | Wizard control markup with steps control |

## Markup

### Wizard control with steps
- shortcut: radwizard
- filename: radwizard.snippet
- default destination: 'C:\Users\\{USERNAME}\Documents\Visual Studio 2015\Code Snippets\Visual Web Developer\My HTML Snippets'

<details>
<summary>Generated code (Click here to expand)</summary>

```html
<telerik:RadWizard runat="server" ID="RadWizard1">
    <WizardSteps>
        <telerik:RadWizardStep ID="WizardStep1" StepType="Start">
            Step 1
        </telerik:RadWizardStep>
        <telerik:RadWizardStep ID="WizardStep2">
            Step 2
        </telerik:RadWizardStep>
        <telerik:RadWizardStep ID="WizardStep3">
            Step 3
        </telerik:RadWizardStep>
        <telerik:RadWizardStep ID="WizardStep4" StepType="Finish">
            Finish step
        </telerik:RadWizardStep>
        <telerik:RadWizardStep ID="WizardStep5" StepType="Complete">
            Completed!
        </telerik:RadWizardStep>
    </WizardSteps>
</telerik:RadWizard>
```

</details>

