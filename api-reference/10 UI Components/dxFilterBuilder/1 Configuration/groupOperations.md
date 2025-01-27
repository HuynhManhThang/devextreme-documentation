---
id: dxFilterBuilder.Options.groupOperations
type: Array<Enums.GroupOperation>
default: ['and', 'or', 'notAnd', 'notOr']
---
---
##### shortDescription
Specifies a set of available group operations.

---
The group operations are:

- *"and"*       
- *"notAnd"*        
 Returns a reverted result of an *"and"* operation: `["!", [[condition1], "and", [condition2]]]`.
- *"or"*        
- *"notOr"*     
 Returns a reverted result of an *"or"* operation: `["!", [[condition1], "or", [condition2]]]`.

#include common-demobutton with {
    url: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/FilterBuilder/Customization/"
}

#####See Also#####
- [maxGroupLevel](/api-reference/10%20UI%20Components/dxFilterBuilder/1%20Configuration/maxGroupLevel.md '/Documentation/ApiReference/UI_Components/dxFilterBuilder/Configuration/#maxGroupLevel')
- [groupOperationDescriptions](/api-reference/10%20UI%20Components/dxFilterBuilder/1%20Configuration/groupOperationDescriptions '/Documentation/ApiReference/UI_Components/dxFilterBuilder/Configuration/groupOperationDescriptions/')