---
id: dxPolarChart.Options.valueAxis.tickInterval
inherits: VizTimeInterval
---
---
##### shortDescription
Specifies an interval between axis ticks/grid lines.

---
Use this property to divide the scale by ticks in a specified interval from each other. If this property is not set, ticks are automatically arranged so that their labels do not overlap each other.

In case of a continuous or a logarithmic axis, assign a numeric value to this property.

If the axis is of the date-time type, assign one of the predefined string values or an object to this property. The object's fields specify the number of days, hours etc.

When you use a [logarithmic axis](/api-reference/10%20UI%20Components/dxPolarChart/1%20Configuration/valueAxis/type.md '/Documentation/ApiReference/UI_Components/dxPolarChart/Configuration/valueAxis/#type'), ticks are generated on a base of powers. For example, assume that the [logarithm base](/api-reference/10%20UI%20Components/dxPolarChart/1%20Configuration/valueAxis/logarithmBase.md '/Documentation/ApiReference/UI_Components/dxPolarChart/Configuration/valueAxis/#logarithmBase') is 10. Then, if the tick interval is 1, ticks are generated at 0.01, 0.1, 1, 10, 100, 1000, 10000, etc. If the tick interval is 2, ticks are generated at 0.1, 10, 1000, etc.

To set the **tickInterval** property for several axis at once, use the [commonAxisSettings](/api-reference/10%20UI%20Components/dxPolarChart/1%20Configuration/commonAxisSettings '/Documentation/ApiReference/UI_Components/dxPolarChart/Configuration/commonAxisSettings/') configuration object. To set this property for an individual axis, use the [argumentAxis](/api-reference/10%20UI%20Components/dxPolarChart/1%20Configuration/argumentAxis '/Documentation/ApiReference/UI_Components/dxPolarChart/Configuration/argumentAxis/') or **valueAxis** configuration object.
