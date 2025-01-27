---
id: dxTextBox.Options.mode
type: Enums.TextBoxType
default: 'text'
---
---
##### shortDescription
The "mode" attribute value of the actual HTML input element representing the text box.

---
The value of this property affects the set of keyboard buttons shown on the mobile device when the UI component gets focus. In addition, the following mode values add visual features to the UI component:

 - "search" - the text box contains the "X" button, which clears the text box contents
 - "password" - the text box shows a password character instead of the actual characters typed

#include common-demobutton with {
    url: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/TextBox/Overview/"
}