---
id: dxDataGrid.Options.summary.totalItems.customizeText
---
---
##### shortDescription
Customizes the text to be displayed in the summary item.

##### param(itemInfo): Object
The summary item's data.

##### field(itemInfo.value): String | Number | Date
The summary item's value as it was calculated.

##### field(itemInfo.valueText): String
The summary item's [formatted](/api-reference/10%20UI%20Components/dxDataGrid/1%20Configuration/summary/totalItems/valueFormat.md '/Documentation/ApiReference/UI_Components/dxDataGrid/Configuration/summary/totalItems/#valueFormat') value.

##### return: String
The text for the summary item to display.

---
This property accepts a function that must return the text to be displayed in the summary item. When you implement this function, you can access the summary item value using the fields of object passed to the function as its argument. 

#include common-demobutton with {
    url: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/DataGrid/GridSummaries/"
}

#####See Also#####
- [Format Text and Value](/concepts/05%20UI%20Components/DataGrid/65%20Summaries/40%20Format%20Text%20and%20Value.md '/Documentation/Guide/UI_Components/DataGrid/Summaries/Format_Text_and_Value/')