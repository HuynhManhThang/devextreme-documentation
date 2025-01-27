If you need to update form data at runtime, redefine the [formData](/api-reference/10%20UI%20Components/dxForm/1%20Configuration/formData.md '/Documentation/ApiReference/UI_Components/dxForm/Configuration/#formData') object. In this case, form item values are updated automatically and the UI component is rerendered from scratch. In the following example, the [SelectBox](/api-reference/10%20UI%20Components/dxSelectBox '/Documentation/ApiReference/UI_Components/dxSelectBox/') UI component changes the **formData** object.

    <!--JavaScript-->
    var employees = [{
        name: "John Heart",
        position: "CEO",
        officeNo: "901"
    }, {
        name: "Bill Silver",
        position: "HR Manager",
        officeNo: "905"
    }];

    $(function() {
        var form = $("#formContainer").dxForm({
            formData: employees[0]
        }).dxForm("instance");

        $("#employeeSelector").dxSelectBox({
            displayExpr: "name",
            dataSource: employees,
            value: employees[0],
            onValueChanged: function(data) {
                form.option("formData", data.value);
            }
        });
    });

#include common-demobutton with {
    url: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/Form/Overview/"
}

The Form UI component provides methods that update specific **formData** fields and rerender the corresponding editors without rerendering the whole UI component. The [updateData(dataField, value)](/api-reference/10%20UI%20Components/dxForm/3%20Methods/updateData(dataField_value).md '/Documentation/ApiReference/UI_Components/dxForm/Methods/#updateDatadataField_value') method updates the value of a single field. The [updateData(data)](/api-reference/10%20UI%20Components/dxForm/3%20Methods/updateData(data).md '/Documentation/ApiReference/UI_Components/dxForm/Methods/#updateDatadata') method updates values of several fields at once. In the following code, these methods are called on a [Button](/api-reference/10%20UI%20Components/dxButton '/Documentation/ApiReference/UI_Components/dxButton/') click.

    <!--JavaScript-->
    $(function() {
        var form = $("#formContainer").dxForm({
            formData: {
                firstName: "Joe",
                lastName: "Heart",
                phone: "+1(213) 555-9392"
            }
        }).dxForm("instance");

        $("#updatePhone").dxButton({
            text: 'Update the Phone Number',
            onClick: function () {
                form.updateData("phone", "+1(333) 888-7698");
            }
        });

        $("#updateName").dxButton({
            text: 'Update the Name',
            onClick: function () {
                form.updateData({
                    firstName: "John",
                    lastName: "Doe"
                });
            }
        });
    });

With Angular, Vue or React, two-way binding to a component property is sufficient to update [formData](/api-reference/10%20UI%20Components/dxForm/1%20Configuration/formData.md '/Documentation/ApiReference/UI_Components/dxForm/Configuration/#formData') at runtime. Swapping the whole **formData** object rerenders the UI component from scratch; updating specific **formData** fields rerenders only the corresponding editors.

---
##### Angular

    <!--HTML-->
    <dx-form [(formData)]="employee"></dx-form>
    <dx-button
        text="Update the Phone Number"
        (onClick)="employee.phone = '+1(333) 888-7698'">
    </dx-button>

    <!--TypeScript-->
    import { DxFormModule, DxButtonModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        employee = {
            firstName: "Joe",
            lastName: "Heart",
            phone: "+1(213) 555-9392"
        }
    }
    @NgModule({
        imports: [
            // ...
            DxFormModule,
            DxButtonModule
        ],
        // ...
    })

##### Vue

    <!-- tab: App.vue -->
    <template>
        <div>
            <DxForm :form-data="employee" />
            <DxButton
                text="Update the Phone Number"
                @click="updatePhone" />
        </div>
    </template>
    <script>
    import 'devextreme/dist/css/dx.light.css';

    import { DxForm } from 'devextreme-vue/form';
    import { DxButton } from 'devextreme-vue/button';

    const employee = {
        firstName: 'John',
        lastName: 'Heart',
        phone: '+1(213) 555-9392'
    };

    export default {
        components: {
            DxForm, DxButton
        },
        data() {
            return {
                employee
            };
        },
        methods: {
            updatePhone(e) {
                this.employee.phone = '+1(333) 888-7698';
            }
        }
    };
    </script>

##### React

    <!-- tab: App.js -->
    import React from 'react';

    import 'devextreme/dist/css/dx.light.css';

    import { Form } from 'devextreme-react/form';
    import { Button } from 'devextreme-react/button';

    const employee = {
        firstName: 'John',
        lastName: 'Heart',
        phone: '+1(213) 555-9392'
    };

    class App extends React.Component {
        constructor() {
            super();
            this.state = {
                employee
            }
            this.updatePhone = this.updatePhone.bind(this);
        }

        render() {
            return (
                <div>
                    <Form formData={this.state.employee} />
                    <Button
                        text="Update the Phone Number"
                        onClick={this.updatePhone} />
                </div>
            );
        }

        updatePhone(e) {
            this.setState(() => {
                return { employee: {...employee, phone: '+1(333) 888-7698' } };
            });
        }
    }

    export default App;

---

#####See Also#####
- [Form - Handle the Value Change Event](/concepts/05%20UI%20Components/Form/25%20Handle%20the%20Value%20Change%20Event.md '/Documentation/Guide/UI_Components/Form/Handle_the_Value_Change_Event/')
- [Form - Generate a Data Object from Form Items](/concepts/05%20UI%20Components/Form/35%20Generate%20a%20Data%20Object%20from%20Form%20Items.md '/Documentation/Guide/UI_Components/Form/Generate_a_Data_Object_from_Form_Items/')
- [Validate the Form Data](/concepts/05%20UI%20Components/Form/01%20Getting%20Started%20with%20Form/70%20Validate%20the%20Form%20Data.md '/Documentation/Guide/UI_Components/Form/Getting_Started_with_Form/#Validate_the_Form_Data')
- [Submit the Form](/concepts/05%20UI%20Components/Form/01%20Getting%20Started%20with%20Form/80%20Submit%20the%20Form.md '/Documentation/Guide/UI_Components/Form/Getting_Started_with_Form/#Submit_the_Form')
- [Form Demos](https://js.devexpress.com/Demos/WidgetsGallery/Demo/Form/Overview)
- [Form API Reference](/api-reference/10%20UI%20Components/dxForm '/Documentation/ApiReference/UI_Components/dxForm/')

[tags]form, form data, formData, change form data, update data, update form data
