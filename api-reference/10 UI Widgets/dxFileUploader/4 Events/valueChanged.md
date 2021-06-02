---
id: dxFileUploader.valueChanged
type: eventType
---
---
##### shortDescription
Raised when one or several files are added to or removed from the selection.

##### param(e): Object
Information about the event.

##### field(e.component): {WidgetName}
The widget's instance.

##### field(e.element): dxElement
#include common-ref-elementparam with { element: "widget" }

##### field(e.event): event
#include common-ref-eventparam

##### field(e.jQueryEvent).deprecated
Use 'event' instead.

##### field(e.jQueryEvent): jQuery.Event
The jQuery event that caused the handler execution. Deprecated in favor of the **event** field.

##### field(e.model): Object
The model data. Available only if Knockout is used.

##### field(e.previousValue): Array<File>
Previously selected files.

##### field(e.value): Array<File>
Newly selected files.

---
Main article: [onValueChanged](/api-reference/10%20UI%20Widgets/dxFileUploader/1%20Configuration/onValueChanged.md '/Documentation/ApiReference/UI_Widgets/dxFileUploader/Configuration/#onValueChanged')

#####See Also#####
#include common-link-handleevents