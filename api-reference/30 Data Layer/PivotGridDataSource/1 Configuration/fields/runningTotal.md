---
id: PivotGridDataSource.Options.fields.runningTotal
type: Enums.PivotGridRunningTotalMode
default: undefined
---
---
##### shortDescription
Specifies whether to calculate the running total by rows or by columns.

---
For example, a pivot grid row contains the following summary values:

    [ 3, 3, 3, 3, 3 ]

If the **runningTotal** property is set to *"row"*, each value in this row is added to the previous value:

    [ 3, 6, 9, 12, 15 ]

This also applies to columns if the **runningTotal** property is set to *"column"*.

#include common-demobutton with {
    url: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/Pivot_Grid/RunningTotals/"
}

#####See Also#####
- **fields[]**.[allowCrossGroupCalculation](/api-reference/30%20Data%20Layer/PivotGridDataSource/1%20Configuration/fields/allowCrossGroupCalculation.md '/Documentation/ApiReference/Data_Layer/PivotGridDataSource/Configuration/fields/#allowCrossGroupCalculation')