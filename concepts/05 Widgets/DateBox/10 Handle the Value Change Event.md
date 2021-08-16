If instead of picking a value, an end user types it into the **DateBox**, this value applies when the <a href="https://developer.mozilla.org/en/docs/Web/Events/change" target="_blank">change</a> event is raised. If you need the value to be applied on another event, set the [valueChangeEvent](/api-reference/10%20UI%20Widgets/dxTextEditor/1%20Configuration/valueChangeEvent.md '/Documentation/ApiReference/UI_Widgets/dxDateBox/Configuration/#valueChangeEvent') option.

---
##### jQuery

    <!--JavaScript-->
    $(function() {
        $("#dateBoxContainer").dxDateBox({
            value: new Date(),
            type: "date",
            valueChangeEvent: "keyup"
        });
    });

##### Angular

    <!--HTML-->
    <dx-date-box
        [(value)]="date"
        type="date"
        valueChangeEvent="keyup">
    </dx-date-box>

    <!--TypeScript-->
    import { DxDateBoxModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        date: Date = new Date()
    }
    @NgModule({
        imports: [
            // ...
            DxDateBoxModule
        ],
        // ...
    })

---

To process a new **DateBox** value, you need to handle the value change event. If the handling function is not going to be changed during the lifetime of the widget, assign it to the [onValueChanged](/api-reference/10%20UI%20Widgets/Editor/1%20Configuration/onValueChanged.md '/Documentation/ApiReference/UI_Widgets/dxDateBox/Configuration/#onValueChanged') option when you configure the widget.

---
##### jQuery

    <!--JavaScript-->
    $(function() {
        $("#dateBoxContainer").dxDateBox({
            // ...
            onValueChanged: function (e) {
                var previousValue = e.previousValue;
                var newValue = e.value;
                // Event handling commands go here
            }
        });
    });

##### Angular

    <!--HTML-->
    <dx-date-box ...
        (onValueChanged)="dateBox_valueChanged($event)">
    </dx-date-box>

    <!--TypeScript-->
    import { DxDateBoxModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        dateBox_valueChanged (e) {
            let previousValue = e.previousValue;
            let newValue = e.value;
            // Event handling commands go here
        }
    }
    @NgModule({
        imports: [
            // ...
            DxDateBoxModule
        ],
        // ...
    })

---

If you are going to change event handlers at runtime, or if you need to attach several handlers to the value change event, subscribe to this event using the [on(eventName, eventHandler)](/api-reference/10%20UI%20Widgets/EventsMixin/3%20Methods/on(eventName_eventHandler).md '/Documentation/ApiReference/UI_Widgets/dxDateBox/Methods/#oneventName_eventHandler') method. This approach is more typical of jQuery.

    <!--JavaScript-->
    var valueChangedHandler1 = function (e) {
        var previousValue = e.previousValue;
        var newValue = e.value;
        // First handler of the "valueChanged" event
    };

    var valueChangedHandler2 = function (e) {
        var previousValue = e.previousValue;
        var newValue = e.value;
        // Second handler of the "valueChanged" event
    };

    $("#dateBoxContainer").dxDateBox("instance")
        .on("valueChanged", valueChangedHandler1)
        .on("valueChanged", valueChangedHandler2);

#####See Also#####
#include common-link-handleevents
- [DateBox - Control the Behavior](/concepts/05%20Widgets/DateBox/05%20Control%20the%20Behavior.md '/Documentation/Guide/Widgets/DateBox/Control_the_Behavior')
- [DateBox - Specify Value Range](/concepts/05%20Widgets/DateBox/15%20Specify%20Value%20Range.md '/Documentation/Guide/Widgets/DateBox/Specify_Value_Range')
- [DateBox Demos](https://js.devexpress.com/Demos/WidgetsGallery/#demo/editors-date_box-overview)
- [DateBox API Reference](/api-reference/10%20UI%20Widgets/dxDateBox '/Documentation/ApiReference/UI_Widgets/dxDateBox/')

[tags]date box, dateBox, editor, get value, set value, change value, valueChangeEvent, valueChanged