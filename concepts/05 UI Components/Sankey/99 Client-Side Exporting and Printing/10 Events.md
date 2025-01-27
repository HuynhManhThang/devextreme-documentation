DevExtreme data visualization UI components raise the following exporting-related events:

- [exporting](/api-reference/10%20UI%20Components/BaseWidget/4%20Events/exporting.md '/Documentation/ApiReference/UI_Components/dxSankey/Events/#exporting')  
Allows you to request export details or prevent exporting.

- [exported](/api-reference/10%20UI%20Components/BaseWidget/4%20Events/exported.md '/Documentation/ApiReference/UI_Components/dxSankey/Events/#exported')  
Allows you to notify an end user when exporting is completed.

- [fileSaving](/api-reference/10%20UI%20Components/BaseWidget/4%20Events/fileSaving.md '/Documentation/ApiReference/UI_Components/dxSankey/Events/#fileSaving')        
Allows you to access exported data in the <a href="https://en.wikipedia.org/wiki/Binary_large_object" target="_blank">BLOB</a> format and/or prevent it from being saved on the user's device.

You can handle these events with functions. If the handling functions are not going to be changed at runtime, assign them to the [onExporting](/api-reference/10%20UI%20Components/BaseWidget/1%20Configuration/onExporting.md '/Documentation/ApiReference/UI_Components/dxSankey/Configuration/#onExporting'), [onExported](/api-reference/10%20UI%20Components/BaseWidget/1%20Configuration/onExported.md '/Documentation/ApiReference/UI_Components/dxSankey/Configuration/#onExported') and [onFileSaving](/api-reference/10%20UI%20Components/BaseWidget/1%20Configuration/onFileSaving.md '/Documentation/ApiReference/UI_Components/dxSankey/Configuration/#onFileSaving') properties when you configure the UI component.

---
##### jQuery

    <!--JavaScript-->$(function() {
        $("#sankeyContainer").dxSankey({
            // ...
            onExporting: function(e) {
                // Handler of the "exporting" event
            },
            onExported: function(e) {
                // Handler of the "exported" event
            },
            onFileSaving: function(e) {
                // Handler of the "fileSaving" event
            }
        });
    });


##### Angular

    <!--HTML--><dx-sankey ...
        (onExporting)="onExporting($event)"
        (onExported)="onExported($event)"
        (onFileSaving)="onFileSaving($event)">
    </dx-sankey>

    <!--TypeScript-->
    import { DxSankeyModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        onExporting(e) {
            // Handler of the "exporting" event
        };
        onExported(e) {
            // Handler of the "exported" event
        };
        onFileSaving(e) {
            // Handler of the "fileSaving" event
        }
    }
    @NgModule({
        imports: [
            // ...
            DxSankeyModule
        ],
        // ...
    })

##### Vue

    <!-- tab: App.vue -->
    <template> 
        <DxSankey
            @exporting="onExporting"
            @exported="onExported"
            @file-saving="onFileSaving"
        />
    </template>

    <script>
    import DxSankey from 'devextreme-vue/sankey';

    export default {
        components: {
            DxSankey
        },
        methods: {
            onExporting(e) {
                // Handler of the "exporting" event
            };
            onExported(e) {
                // Handler of the "exported" event
            };
            onFileSaving(e) {
                // Handler of the "fileSaving" event
            }
        }
    }
    </script>

##### React

    <!-- tab: App.js -->
    import React from 'react';
    import Sankey from 'devextreme-react/sankey';

    class App extends React.Component {
        render() {
            return (
                <Sankey
                    onExporting={this.onExporting}
                    onExported={this.onExported}
                    onFileSaving={this.onFileSaving}
                />
            )
        }
        onExporting(e) {
            // Handler of the "exporting" event
        };
        onExported(e) {
            // Handler of the "exported" event
        };
        onFileSaving(e) {
            // Handler of the "fileSaving" event
        }
    }

    export default App;

---

---

##### jQuery

Otherwise (or if you need several handlers for a single event), subscribe to the exporting-related events using the [on(eventName, eventHandler)](/api-reference/10%20UI%20Components/Component/3%20Methods/on(eventName_eventHandler).md '/Documentation/ApiReference/UI_Components/dxSankey/Methods/#oneventName_eventHandler') method.

    <!--JavaScript-->
    var exportedHandler1 = function(e) {
        // First handler of the "exported" event
    };

    var exportedHandler2 = function(e) {
        // Second handler of the "exported" event
    };

    $("#sankeyContainer").dxSankey("instance")
        .on("exported", exportedHandler1)
        .on("exported", exportedHandler2);

---

#####See Also#####
#include common-link-handleevents
