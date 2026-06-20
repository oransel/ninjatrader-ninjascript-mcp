# WorkspaceOptions

Source: https://developer.ninjatrader.com/docs/desktop/workspaceoptions

---

# WorkspaceOptions


## [Definition](https://developer.ninjatrader.com/docs/desktop/workspaceoptions#definition)


Sets required workspace options.
![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


- The WorkspaceOptions class includes logic for opening, closing, saving, and restoring workspaces, checking windows are off screen, and setting basic properties such as the workspace name and current status.
- A WorkspaceOptions property must simply be declared within your NTWindow, as in the example below. All of its contained logic is taken care of automatically.


## [Examples](https://developer.ninjatrader.com/docs/desktop/workspaceoptions#examples)


```csharp
// IWorkspacePersistence member

public WorkspaceOptions WorkspaceOptions { get; set; }
```

![note image](/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FNote.57c6078c.svg&w=64&q=75)

## Note


**Tip**: For a complete, working example of this class in use, please download the [AddOn Framework NinjaScript Basic Example](http://ninjatrader.com/support/helpGuides/AddOn_Framework_NinjaScript_Basic.zip) to your desktop.
