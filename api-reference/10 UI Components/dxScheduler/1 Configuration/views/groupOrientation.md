---
id: dxScheduler.Options.views.groupOrientation
type: Enums.Orientation
---
---
##### shortDescription
Arranges resource headers vertically (in a column) or horizontally (in a row).

---
This property's default value depends on the view [type](/api-reference/10%20UI%20Components/dxScheduler/1%20Configuration/views/type.md '/Documentation/ApiReference/UI_Components/dxScheduler/Configuration/views/#type'). The following list illustrates the dependency:

- *"horizontal"*        
For the **day**, **month**, **week**, and **workWeek** view types.

- *"vertical"*          
For the **timelineDay**, **timelineMonth**, **timelineWeek**, and **timelineWorkWeek** view types. For the **agenda**, resource headers are always organized vertically.

#include common-demobutton with {
    url: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/Scheduler/GroupOrientation/"
}

#####See Also#####
- [Group Appointments by Resources](/concepts/05%20UI%20Components/Scheduler/040%20Resources/030%20Group%20Appointments%20by%20Resources.md '/Documentation/Guide/UI_Components/Scheduler/Resources/Group_Appointments_by_Resources/')