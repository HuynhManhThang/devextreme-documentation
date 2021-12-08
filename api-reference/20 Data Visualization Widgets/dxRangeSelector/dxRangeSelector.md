---
module: viz/range_selector
export: default
inherits: ..\BaseWidget\BaseWidget.md
---
---
##### widgettree
dataSource: [{
    arg: "1",
    val: 1
}, {
    arg: "2",
    val: 2
}, {
    arg: "3",
    val: 3
}, {
    arg: "4",
    val: 4
}, {
    arg: "5",
    val: 5
}, {
    arg: "6",
    val: 6
}, {
    arg: "7",
    val: 7
}, {
    arg: "8",
    val: 8
}]

##### lib
dx.viz.js, dx.viz-web.js, dx.all.js

##### shortDescription
The **RangeSelector** is a widget that allows a user to select a range of values on a scale.

---
This widget represents a scale (numeric or date-time) and two sliders. A user selects the required range by moving the sliders.

<img style="margin:0px auto;display:block" src="/Content/images/doc/18_1/ChartJS/RangeSelector_new.gif" alt="RangeSelector" />

#include common-ref-roottopic-introduction

---
#####[**jQuery**](/concepts/00%20Getting%20Started/10%20Widget%20Basics%20-%20jQuery/01%20Create%20and%20Configure%20a%20Widget.md '/Documentation/Guide/Getting_Started/Widget_Basics_-_jQuery/Create_and_Configure_a_Widget/')  

    <!--JavaScript-->$(function() {
        $("#rangeSelector").dxRangeSelector({
            scale: {
                startValue: new Date(2011, 0, 1),
                endValue: new Date(2011, 5, 1),
                tickInterval: { days: 7 }
            }
        });
    });

    <!--HTML--><div id="rangeSelector"></div>

#####[**Angular**](/concepts/00%20Getting%20Started/15%20Widget%20Basics%20-%20Angular/01%20Create%20and%20Configure%20a%20Widget.md '/Documentation/Guide/Getting_Started/Widget_Basics_-_Angular/Create_and_Configure_a_Widget/')  

    <!--HTML-->
    <dx-range-selector>
        <dxo-scale
            [startValue]="startDate"
            [endValue]="endDate">
            <dxo-tick-interval [days]="7"></dxo-tick-interval>
        </dxo-scale>
    </dx-range-selector>

    <!--TypeScript-->
    import { DxRangeSelectorModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        startDate = new Date(2011, 0, 1);
        endDate = new Date(2011, 5, 1);
    }
    @NgModule({
        imports: [
            // ...
            DxRangeSelectorModule
        ],
        // ...
    })

#####[**AngularJS**](/concepts/00%20Getting%20Started/20%20Widget%20Basics%20-%20AngularJS/01%20Create%20and%20Configure%20a%20Widget.md '/Documentation/Guide/Getting_Started/Widget_Basics_-_AngularJS/Create_and_Configure_a_Widget/')  

    <!--HTML--><div ng-controller="DemoController">
        <div dx-range-selector="{
            scale: {
                startValue: startDate,
                endValue: endDate,
                tickInterval: { days: 7 }
            }
        }"></div>
    </div>

    <!--JavaScript-->angular.module('DemoApp', ['dx'])
        .controller("DemoController", function ($scope) {
            $scope.startDate = new Date(2011, 0, 1);
            $scope.endDate = new Date(2011, 5, 1);
        });

#####[**Knockout**](/concepts/00%20Getting%20Started/25%20Widget%20Basics%20-%20Knockout/01%20Create%20and%20Configure%20a%20Widget.md '/Documentation/Guide/Getting_Started/Widget_Basics_-_Knockout/Create_and_Configure_a_Widget/')  

    <!--HTML-->
    <div data-bind="dxRangeSelector: {
        scale: {
            startValue: new Date(2011, 0, 1),
            endValue: new Date(2011, 5, 1),
            tickInterval: { days: 7 }
        }
    }"></div>

#####[**ASP.NET MVC Controls**](/Documentation/Guide/ASP.NET_MVC_Controls/Fundamentals/#Creating_a_Widget)
    
    <!--Razor C#-->@(Html.DevExtreme().RangeSelector()
        .ID("rangeSelector")
        .Scale(scale => scale
            .StartValue(new DateTime(2011, 1, 1))
            .EndValue(new DateTime(2011, 6, 1))
            .TickInterval(ti => ti.Days(7))
        )
    )

    <!--Razor VB-->@(Html.DevExtreme().RangeSelector() _
        .ID("rangeSelector") _
        .Scale(Sub(scale)
            scale.StartValue(New DateTime(2011, 1, 1)) _
                    .EndValue(New DateTime(2011, 6, 1)) _
                    .TickInterval(Sub(ti) ti.Days(7))
        End Sub)
    )

---

 

A chart can be displayed in the [background](/api-reference/20%20Data%20Visualization%20Widgets/dxRangeSelector/1%20Configuration/background '/Documentation/ApiReference/Data_Visualization_Widgets/dxRangeSelector/Configuration/background/') of the **RangeSelector** widget. This allows end users to select the required range in a chart series. You can also integrate the **RangeSelector** widget with a stand-alone [Chart](/api-reference/20%20Data%20Visualization%20Widgets/dxChart '/Documentation/ApiReference/Data_Visualization_Widgets/dxChart/') widget to emulate chart [zooming and scrolling](/concepts/05%20Widgets/zz%20Common/10%20Data%20Visualization%20Widgets/90%20Charts%20-%20End-User%20Interaction/6%20Zooming%20and%20Scrolling/01%20Using%20dxRangeSelector.md '/Documentation/Guide/Widgets/Common/Data_Visualization_Widgets/Charts_-_End-User_Interaction/Zooming_and_Scrolling/#Using_dxRangeSelector').

#include common-demobutton with {
    url: "https://js.devexpress.com/Demos/WidgetsGallery/#demo/formsandmulti-purposerangeselectorrangeselectornumericscale/"
}
<a href="http://www.youtube.com/watch?v=0x_VmMwxigA&index=52&list=PL8h4jt35t1wjGvgflbHEH_e3b23AA30-z" class="button orange small fix-width-155" target="_blank">Watch Video</a>

#####See Also#####
- [RangeSelector - Visual Elements](/concepts/05%20Widgets/RangeSelector/10%20Visual%20Elements '/Documentation/Guide/Widgets/RangeSelector/Visual_Elements/')
- [RangeSelector - Range Changing](/concepts/05%20Widgets/RangeSelector/20%20Range%20Changing '/Documentation/Guide/Widgets/RangeSelector/Range_Changing/')