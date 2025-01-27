---
id: dxPivotGrid.Options.scrolling.mode
type: Enums.ScrollMode
default: 'standard'
---
---
##### shortDescription
Specifies the scrolling mode.

---
There are two different scrolling modes.

- **Standard Mode**        
    In a standard scrolling mode, the grid loads the entire summary data at once. This operation may affect grid performance as the loaded data may contain many summary values.

- **Virtual Mode**        
    In a virtual scrolling mode, the grid loads a summary value at runtime when it gets into a field of vision. Once a summary cell is out of the field of vision, it is removed from the grid. This behavior allows an end-user to scroll through large amounts of grid records without noticeable lags.      

#include common-demobutton-named with {
    url: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/PivotGrid/VirtualScrolling/",
    name: "Virtual Scrolling"
}
#include common-demobutton-named with {
    url: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/PivotGrid/RemoteVirtualScrolling/",
    name: "Remote Virtual Scrolling"
}