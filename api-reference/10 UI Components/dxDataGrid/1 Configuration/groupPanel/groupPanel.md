---
id: dxDataGrid.Options.groupPanel
type: ui/data_grid:GroupPanel
inheritsType: ui/data_grid:GroupPanel
---
---
##### shortDescription
Configures the [group panel](/concepts/05%20UI%20Components/DataGrid/45%20Grouping/10%20User%20Interaction/10%20Group%20Data.md '/Documentation/Guide/UI_Components/DataGrid/Grouping/#User_Interaction/Group_Data').

---
Data in DataGrid can be grouped by one column or by several. Once a column is used for grouping, it is added to the group panel.

By default, the group panel is hidden. To make it visible, set the **groupPanel**.[visible](/api-reference/10%20UI%20Components/dxDataGrid/1%20Configuration/groupPanel/visible.md '/Documentation/ApiReference/UI_Components/dxDataGrid/Configuration/groupPanel/#visible') property to **true**. Alternatively, the visibility of the group panel can depend on the device's screen size. To accomplish this behavior, set the **visible** property to *"auto"*.

In case you need to show the group panel, but make it irresponsive, assign **false** to the **groupPanel**.[allowColumnDragging](/api-reference/10%20UI%20Components/dxDataGrid/1%20Configuration/groupPanel/allowColumnDragging.md '/Documentation/ApiReference/UI_Components/dxDataGrid/Configuration/groupPanel/#allowColumnDragging') property. This is useful, for instance, when grid records are grouped initially and when the user needs to know about that grouping, but must not be able to change it.

#include common-demobutton-named with {
    url: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/DataGrid/RecordGrouping/",
    name: "Record Grouping"
}
#include common-demobutton-named with {
    url: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/DataGrid/RemoteGrouping/",
    name: "Remote Grouping"
}

#####See Also#####
- [Grouping](/concepts/05%20UI%20Components/DataGrid/45%20Grouping '/Documentation/Guide/UI_Components/DataGrid/Grouping/')
- **grouping**.[contextMenuEnabled](/api-reference/10%20UI%20Components/dxDataGrid/1%20Configuration/grouping/contextMenuEnabled.md '/Documentation/ApiReference/UI_Components/dxDataGrid/Configuration/grouping/#contextMenuEnabled') - enables the user to group data using the context menu.
- **columns[]**.[allowGrouping](/api-reference/_hidden/dxDataGridColumn/allowGrouping.md '/Documentation/ApiReference/UI_Components/dxDataGrid/Configuration/columns/#allowGrouping') - disallows grouping for an individual column.