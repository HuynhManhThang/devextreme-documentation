---
hidden: false
type: eventType
---
---
##### shortDescription
Raised after a list item is deleted from the data source.

##### param(e): Object
Information about the event.

##### field(e.component): {WidgetName}
The widget's instance.

##### field(e.element): dxElement
The widget's container. It is an [HTML Element](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement) or a [jQuery Element](https://api.jquery.com/Types/#jQuery) when you use jQuery.

##### field(e.model): Object
The model data. Available only if Knockout is used.

##### field(e.itemData): Object
The removed item's data.

##### field(e.itemElement): dxElement
The item's container. It is an [HTML Element](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement) or a [jQuery Element](https://api.jquery.com/Types/#jQuery) when you use jQuery.

##### field(e.itemIndex): Number | Object
The removed item's index. In a grouped list, the index represents an object defining the group and item indexes: { group: 0, item: 0 }.

---
Main article: [onItemDeleted](/api-reference/10%20UI%20Widgets/dxList/1%20Configuration/onItemDeleted.md '/Documentation/ApiReference/UI_Widgets/dxList/Configuration/#onItemDeleted')

#####See Also#####
- [List - Handle Deletion-Related Events](/concepts/05%20Widgets/List/35%20Item%20Deletion/10%20Events.md '/Documentation/Guide/Widgets/List/Item_Deletion/#Events')
#include common-link-handleevents