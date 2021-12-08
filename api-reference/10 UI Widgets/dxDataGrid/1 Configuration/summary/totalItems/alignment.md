---
default: undefined
acceptValues: 'center' | 'left' | 'right'
type: String
---
---
##### shortDescription
Specifies the alignment of a summary item.

---
The default alignment of a summary item depends on the [type of data](/api-reference/10%20UI%20Widgets/GridBase/1%20Configuration/columns/dataType.md '/Documentation/ApiReference/UI_Widgets/dxDataGrid/Configuration/columns/#dataType') that is held by the column that displays this item. The following table illustrates the dependency between the default alignment and the column data type.

<div class="simple-table">
<table>
  <thead>
  <tr>
    <th>dataType</th>
    <th>alignment</th>
  </tr>
  </thead>
  <tbody>
  <tr>
    <td><i>'number'</i></td>
    <td><i>'right'</i></td>
  </tr>
  <tr>
    <td><i>'boolean'</i></td>
    <td><i>'center'</i></td>
  </tr>
  <tr>
    <td><i>'string'</i></td>
    <td><i>'left'</i></td>
  </tr>
  <tr>
    <td><i>'date'</i></td>
    <td><i>'left'</i></td>
  </tr>
  <tr>
    <td><i>'datetime'</i></td>
    <td><i>'left'</i></td>
  </tr>
  <tr>
    <td><i>'guid'</i></td>
    <td><i>'left'</i></td>
  </tr>
  </tbody>
</table>
</div>

#include common-ref-enum with {
    enum: "`HorizontalAlignment`",
    values: "`Left`, `Center`, and `Right`"
}

#####See Also#####
- [Total Summary - Alignment and Location](/concepts/05%20Widgets/DataGrid/65%20Summaries/10%20Total%20Summary/10%20Alignment%20and%20Location.md '/Documentation/Guide/Widgets/DataGrid/Summaries/Total_Summary/#Alignment_and_Location')