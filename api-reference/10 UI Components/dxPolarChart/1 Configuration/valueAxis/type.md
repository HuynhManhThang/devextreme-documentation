---
id: dxPolarChart.Options.valueAxis.type
---
---
##### shortDescription
Specifies the required type of the value axis.

---
The 'discrete' type is set when string values are specified in the data source of the chart's series. The discrete value axis is divided by the values (called _categories_) that are specified in a series' data source. The categories order can be specified by the [categories](/api-reference/10%20UI%20Components/dxPolarChart/1%20Configuration/valueAxis/categories.md '/Documentation/ApiReference/UI_Components/dxPolarChart/Configuration/valueAxis/#categories') property if the order used in the data source is not appropriate.

The 'continuous' type is set when numeric or date-time values are specified in the series data source. The continuous axis is divided automatically.

The 'logarithmic' type can be set when numeric values are specified in the series data source. The logarithmic axis is useful when you visualize a dataset of rapidly-growing values. Each axis tick represents a particular value that is raised to the next power in turn. This particular value is specified by the [logarithmBase](/api-reference/10%20UI%20Components/dxPolarChart/1%20Configuration/argumentAxis/logarithmBase.md '/Documentation/ApiReference/UI_Components/dxPolarChart/Configuration/argumentAxis/#logarithmBase') property. For example, if you set this property to 5, the following ticks will be generated: 5<sup>0</sup>, 5<sup>1</sup>, 5<sup>2</sup>, 5<sup>3</sup>, etc.

On continuous and logarithmic axes, ticks and grid lines are generated automatically. In addition, you can set a custom tick interval (the [tickInterval](/api-reference/10%20UI%20Components/dxPolarChart/1%20Configuration/valueAxis/tickInterval '/Documentation/ApiReference/UI_Components/dxPolarChart/Configuration/valueAxis/tickInterval/') or [axisDivisionFactor](/api-reference/10%20UI%20Components/dxPolarChart/1%20Configuration/valueAxis/axisDivisionFactor.md '/Documentation/ApiReference/UI_Components/dxPolarChart/Configuration/valueAxis/#axisDivisionFactor') properties).

[note] If you require a discrete axis when numeric or date-time values are specified in the data source, set the **type** property to 'discrete' explicitly.
