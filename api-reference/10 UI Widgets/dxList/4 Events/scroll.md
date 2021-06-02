---
id: dxList.scroll
type: eventType
---
---
##### shortDescription
Raised on each scroll gesture.

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

##### field(e.reachedBottom): Boolean
Indicates whether the container's bottom boundary is reached.

##### field(e.reachedLeft): Boolean
Indicates whether the container's left boundary is reached.

##### field(e.reachedRight): Boolean
Indicates whether the container's right boundary is reached.

##### field(e.reachedTop): Boolean
Indicates whether the container's top boundary is reached.

##### field(e.scrollOffset): Object
The current scroll offset in the following format { top: topOffset, left: leftOffset }.

---
Main article: [onScroll](/api-reference/10%20UI%20Widgets/dxList/1%20Configuration/onScroll.md '/Documentation/ApiReference/UI_Widgets/dxList/Configuration/#onScroll')

#####See Also#####
- [List - Handle Scrolling-Related Events](/concepts/05%20Widgets/List/20%20Scrolling/10%20Events.md '/Documentation/Guide/Widgets/List/Scrolling/#Events')
#include common-link-handleevents