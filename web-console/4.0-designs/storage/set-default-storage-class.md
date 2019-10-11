# Storage

## Create Storage Class

![Storage class page with create button](img/create-storage-class.png)
- Users with appropriate privileges can click to create a new Storage Class.

![create storage class form](img/storage-class-form.png)
- They are presented with a form that enables them to define the name, description, type of storage, reclaim policy, and provisioner for this storage class.

![create storage class form](img/storage-class-parameters.png)
- The `What should I enter here?` link should preferably direct the user to a list of parameters for the selected provisioner, but if that is not possible, linking to the Kubernetes documentation is acceptable.

![create storage class form](img/storage-class-parameters-2.png)
- Parameter rows can be added by clicking the `Add Parameter` button and removed with the minus button.
- Rows are not draggable.

![dynamic parameter fields](img/storage-class-generated-fields.png)
- If it is feasible, selecting a provisioner should dynamically create fields for parameters rather than requiring that users specify them. In this case, additional parameters could still be added as needed.

## Attach Storage

![deployment detail page with add storage item](img/add-storage.png)
-  Deployment pages will contain a new `Add Volume` option within the actions dropdown.

![form for adding storage](img/add-storage-create.png)
- The user can either add existing storage or choose to `Create Storage` from within the dropdown.

![form for adding and creating storage](img/create-storage-form.png)
- Selecting `Create Storage` exposes fields for Storage Class, Name, Access Mode, Size, and the label selector checkbox.
- Only access modes that are compatible should be available to select in this form.

## Set Default Storage Class
- Users with appropriate privileges can set a Default Storage Class.
- THERE ARE TWO WAY USER CAN SET A DEFAULT STORAGE CLASS:

#### OPTION-1: Kebab menu option:

1. Login to OpenShift > Admin > Storage (menu) > Storage classes (sub-menu)
2. User can see list of ‘Storage classes' [list view] & there will be a label that indicates `default` storage class

3. Click on the kebab menu > select `Set as Default Storage Class`

![Set a Default Storage Class using kebab menu](img/stroage-opt1-start-1.png)

4. Pop-up opens with confirmation message.
5. User clicks on 'Confirm' button to make the change

![Popup menu with confirmation](img/stroage-opt1-popup-confirm-1.png)

6. Successfully modified ‘Default Storage class” [list view]
![Modified default storage class](img/stroage-opt1-done.png)
NOTE: If user clicks on the kebab menu of the existing 'default storage class' then the `Set as Default Storage Class` will be disabled
![Popup menu with confirmation](img/stroage-opt1-start-1-disable.png
  )

#### OPTION-2: Change the ‘default’ option from storage class detail page:

1. Login to OpenShift > Admin > Storage (menu) > Storage classes (sub-menu)
2. Click on a storage class name link and view details of the storage

![Set a Default Storage Class using edit ](img/stroage-opt2-start.png)

3. SC details are shown as below
4. Click on 'pencil icon' near the ‘default class status’

![Set a Default Storage Class using pencil icon](img/stroage-opt2-details.png)

5. Pop-up opens with a list of ‘SC’ and message shown below:
![Popup menu to select a different Default Storage Class](img/stroage-opt2-popup-select.png)

** Message:
Current default storage class will be changed to false when you
choose a different storage class from the list below.**

6. User can choose any SC as a default storage class and click on ‘Save’ button to confirm the change.
![Popup menu with confirmation](img/stroage-opt2-popup-confirm.png)

7. Successfully modified ‘Default Storage class” [list view]
![Set a Default Storage Class using kebab menu](img/stroage-opt2-done.png)
