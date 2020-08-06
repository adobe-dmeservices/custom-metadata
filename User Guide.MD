# **User Manual for Custom Metadata Panel for Bridge**

## **Table of Contents**
- [Overview](#Overview)
	* [Adobe Bridge](#Adobe-Bridge)
	* [Metadata](#Metadata)
	* [Customizing Metadata](#Customizing-Metadata)
- [Installing Adobe Bridge](#Installing-Adobe-Bridge)
- [Adding the Custom Metadata Extension for Adobe Bridge](#Adding-the-Custom-Metadata-Extension-for-Adobe-Bridge)
- [Accessing Bridge after Adding Extensions](#Accessing-Bridge-after-Adding-Extensions)
- [Troubleshooting Common Issues](#Troubleshooting-Common-Installation-Issues)
- [Using Bridge with the Custom Metadata Panel](#Using-Bridge-with-the-Custom-Metadata-Panel)
- [Managing Metadata](#Managing-Metadata)
	* [Metadata Presets](#Metadata-Presets)
	* [Managing Conflicting Metadata Values](#Managing-Conflicting-Metadata-Values)
	* [Reverting Changes](#Reverting-Changes)
- [File Info Panel](#File-Info-Panel)
- [Using the View Editor](#Using-the-View-Editor)
	* [Assigning Dependencies](#Assigning-Dependencies)
	* [Filtering Options](#Filtering-Options)
	* [Managing Views](#Managing-Views)

### **Overview** 

#### **Adobe Bridge**
Adobe Bridge part of Adobe's [Creative Cloud](https://creativecloud.adobe.com). It is a powerful asset management tool for Creatives and Enterprises that lets users preview, select, organize, edit and publish multiple Creative assets quickly and easily. In Adobe Bridge, users can easily edit the metadata of an asset to improve the search experience for end-users, empower Enterprise workflows, and more clearly inform upstream processes that depend on metadata. The purpose of this guide is to provide an overview of how to customize metadata forms using the Custom Metadata Panel for Bridge. 
#### **Metadata**
Universally, metadata is described a set of data that gives information about other data. Adobe created a metadata specification called [XMP](https://www.adobe.com/devnet/xmp.html) that many applications (Adobe and otherwise) support. Adobe Bridge and the FileInfo Panel (found in most Adobe desktop applications) allow users to view and edit metadata in pre-defined forms, but they does not provide a method to easily customize these forms for new metadata schemas. The **Custom Metadata Panel for Bridge** extension allows a user to customize these fields to provide thorough descriptions of an asset. 
#### **Customizing Metadata**
**Custom Metadata Panel for Bridge** helps Admins and end users build, manage and share custom metadata forms for use in Bridge. The panel supports the following form types: Dates, Single- and Multi-value Text, Dropdown Menus, Constrained value fields (Tags), and a special form item to support AEM Tags. In addition, Admins and end users can focus the metadata experience via **Dependencies**, **Filters** and **Selection Groups**:
-	**Dependencies**
	-	Dependencies block entry in one field until data exists in one or more other fields. This can be used as a form of validation for end-users, ensuring that fields are assigned values in the correct order. For instance, a user might need to select a pet type before choosing a breed, or need to set an arrival date before setting a departure date.
-	**Filters**
	-	Filters reduce the possible options in one field based on the value of another field. This feature can be used as a form of information validation by narrowing the scope of options as a user moves through the form. For instance, after a user selects a pet type, the breed dropdown would remove options not related to the kind of pet.
-	**Selection Groups**
	-	Groups connect multiple options together in a multi-value field. Users choose one value that automatically selects other values that have been grouped together. For instance, in a dropdown which allows users to choose multiple US States, a dropdown called "New England" would automatically select "Maine, New Hampshire, Vermont, Massachusetts, Connecticut, Rhode Island"

### **Installing Adobe Bridge**
1.	Open the Adobe Creative Cloud desktop app and search for Adobe Bridge. 
	-	If prompted, sign in with the email you use to log in to Adobe Creative Cloud.

![Accessing Adobe Bridge from Creative Cloud Desktop](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Accessing%20Adobe%20Bridge%20in%20Creative%20Cloud%20Desktop.jpg)

2.	Click **install**. Follow the prompts and enter your computer's login credentials, if required.

![Installing Adobe Bridge](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Installing%20Adobe%20Bridge.jpg)

3.	Open Adobe Bridge. You can double-click on the icon in your Applications/Programs folder, or you can navigate back to Creative Cloud app and click the button to open Bridge. 

![Opening Adobe Bridge from Creative Cloud Desktop](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Opening%20Adobe%20Bridge%20from%20Creative%20Cloud%20Desktop.jpg)

4.	Your first launch experience includes a welcome message. Read and then click **OK**. 

![Assessing What’s New in Adobe Bridge](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Assessing%20What's%20New%20in%20Adobe%20Bridge.jpg)

### **Adding the Custom Metadata Extension for Adobe Bridge** 
1.	In Adobe Bridge, click on the Window tab and then click on **Find Extensions on Exchange…** Alternatively, you can visit the [Adobe Exchange directly](https://exchange.adobe.com/creativecloud.bridge.html).

![finding Extensions on Exchange](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Finding%20Extensions%20on%20Exchange.jpg)
2.	Search for "Custom Metadata" or scroll down and click on **Custom Metadata Panel for Bridge**.

![Accessing Custom Metadata Panel](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Accessing%20Custom%20Metadata%20Panel.jpg)

3.	Navigate to this page and click the "Free" button to install.

![Installing Custom Metadata Panel](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Installing%20Custom%20Metadata%20Panel.jpg)

4.	Accept the License Agreement by clicking **Accept and Continue**.

5.	Creative Cloud will install the extension on your computer in a few moments. You will need to relaunch Bridge to see the extension.

Using Exchange ensures that you always have the latest version of the Custom Metadata Panel installed. However, some Enterprise customers may need to download the extension outside of Exchange for managed deployment. See [Troubleshooting](#Troubleshooting-Common-Issues) below for further guidance.

### **Accessing Bridge after Adding Extensions**
1.	After the extensions are successfully downloaded and installed, open Adobe Bridge again. When you open Adobe Bridge, you will be prompted with the following message. Click **Yes** for all prompts. 

![Accessing Adobe Bridge after Adding Extensions](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Accessing%20Adobe%20Bridge%20after%20Adding%20Extensions.jpg)

2.	When complete, the following new items should appear in Window>Extensions…:
	-	Custom Metadata Panel
	-	Custom Metadata Panel – View Editor

![Extensions Options](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Extension%20Options.jpg)

### **Troubleshooting Common Installation Issues**
1.	If you have already installed the extension but the Custom Metadata Panel options are not available, please **quit Adobe Bridge** and then navigate to https://exchange.adobe.com/creativecloud.details.103752.custom-metadata-panel-for-bridge.html and click **Download / Install another way**. 

![Troubleshooting_ Step 1](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Troubleshooting_%20Step%201.jpg)

2.	Download the .zxp file and Anastasiy’s Extension manager.
	-	Obtain the .zxp file by clicking **Download Custom Metadata Panel for Bridge**
	-	Obtain the Anastasiy’s Extension manager by clicking [Download Anastasiy’s Extension Manager](https://install.anastasiy.com).

![Troubleshooting_ Step 2](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Troubleshooting_%20Step%202.jpg)

3. ***NOTE:** If you are an Enterprise Admin who needs to deploy outside of Exchange, or if you are an Enterprise user with Admin Privileges who is receiving a licensing error, visit our [Releases page on github](https://github.com/adobe-dmeservices/custom-metadata). Download the latest released .zxp from that page and [download Anastasiy’s Extension Manager](https://install.anastasiy.com) separately.*

4.	Create a folder on your desktop to hold both files. Extract the ZIP archive for Anastasiy's Extension Manager to this folder. Place the ZXP in the folder as well.

![Troubleshooting_ Step 3](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Troubleshooting_%20Step%203.jpg)

5.	Drill into the Extension Manager folder and run the Extension manager.

![Troubleshooting_ Step 4](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Troubleshooting_%20Step%204.jpg)

6.	Drag the downloaded zxp into the Extension Manager or and click **Yes** when prompted to install. You can also select **Bridge** from the **Adobe Products** column and then click the **Install** link above the Adobe Products column. Browse to the ZXP and select it to install.

![Troubleshooting_ Step 5](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Troubleshooting_%20Step%205.jpg)

7.	You’ll see this dialog when finished. Click **OK** to proceed. 

![Troubleshooting_ Step 6](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Troubleshooting_%20Step%206.jpg)

8.	Now launch Bridge again. You should see **Custom Metadata Panel** and **Custom Metadata Panel – View Editor** as new extensions. To check this, click on the **Window** tab, then click **Extensions**. 
	-	Choose **Custom Metadata Panel** to launch the extension.

![Accessing Custom Metadata Panel in Bridge](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Accessing%20Custom%20Metadata%20Panel%20in%20Bridge.jpg)

### **Using Bridge with the Custom Metadata Panel**

1.	In this manual, we use the **Essentials** Workspace in Bridge. Please change your workspace to **Essentials** by clicking on **Window -> Workspaces -> Essentials**.

![Essentials](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Essentials.jpg)

2.	Bridge has many ways to navigate a folder structure to interact with files and folders. You can search, create Collections and Smart Collections, or drill down through a folder structure on your hard drive or mounted file system. The Custom Metadata Panel works on selected files. To use the Custom Metadata Panel, bring some files into focus however you like, and then select one or more of the files. For convenience, the Favorites and Folders tabs are good starting points for navigting your hard drive.

![Locating Files](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Locating%20Files.jpg)

### **Managing Metadata**

1.	When you select an image, the Custom Metadata Panel on the left-hand side of the screen should populate with several fields. These fields are alterable via the [View Editor](#Using-the-View-Editor) and can be used to define distinct data on a specified image. 

	- ***Important Note:** While Bridge provides a set of predefined forms in the built-in Metadata Panel (seen on the right below), users can configure the Custom Metadata panel to consolidate metadata fields from several of the Bridge forms, or introduce completely new metadata schemas to Bridge. See the [View Editor](#Using-the-View-Editor) section for more details.*

![Managing Metadata](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Managing%20Metadata.jpg)

2.	Users view, modify and enter new metadata via these fields. Based on the View settings, certain fields may be read only. Others may be required before a user can submit changes. Others may require data be present in another field in order for them to activate. There are many options, which are covered in the [View Editor](#Using-the-View-Editor) section below.

	The following form field types are supported:
	-	**Text (single- and multi- value)**
		-	Text fields allow users to enter freeform text.
	-	**Date**
		-	Date fields include a date and time picker. Users can enter date and time as freeform text as well. The form will attempt to conform the freeform text to a date formatted value. Users can use relative terms such as "yesterday" and "three weeks from now," as well as "2 days ago" and "45 min from now." If the field needs to adjust the formatting, it will highlight the value in a red border, alerting the user that it has made a formatting change. When the user submits the change, the form will include a warning indicator that it has changed the formatting. The next time you view the file, the formatting will be correct.
	-	**Dropdown  (single- and multi-value)**
		-	Dropdown fields have a defined set of values. Users choose values from a dropdown menu. The form allows you to include friendly text as well as the specific value, so that users can more easily locate choices. Dropdown fields allow users to type in the field, which will reduce the choices to matching values. Users can navigate the dropdown with their arrow keys, and then hit **Enter** or **Return** when they arrive at their choice.
	-	**Constrained value fields (Tags)**
		-	Tags are similar to text fields, however their values are constrained to specific values. Users can type in the field and all matching predefined values will appear below the field, similar to a dropdown. Users can see all available tags by typing and deleting everything in the field. Users can apply multiple tags to a file.
	-	**AEM Tags**
		-	AEM Tags is a special kind of tag. Adobe Experience Manager (AEM) includes a hierarchical tagging architecture for assets, and this form mirrors its functionality. Admins must configure it using specially formatted JSON that is available to them in their AEM instance. Users can navigate the hierarchy of tags and select one or more tags. Users can also type to filter available tags. Once applied, these tags will appear in the Tags field of the Metadata Detail page for the asset, once the asset is ingested into AEM.

3.	You can now edit the values in the form. As you make changes, the form will highlight those changes with green borders or green checkmarks. When you are satisfied with the changes that you have made to the file's metadata, click **Save Changes**. If you have made changes and then are dissatisfied with these changes, then you can click **Revert**. This changes the metadata back to the previous save state.
	- ***Important Note:** If you click outside of the metadata panel before saving, then the metadata will revert to the previous saved state.*

4.	To validate changes or to view the entire XMP metadata record for a file, you can right click on an image and choose **File Info…**. You can also select the file and choose **File>File Info…** or use the keyboard shortcut **cmd/ctrl - i**.

	![File Info](Images_CEP_%20Adobe%20Bridge%20User%20Guide/File%20Info.jpg)

### **Metadata Presets**
1.	The Custom Metadata panel includes the ability to store a file's metadata as a **Metadata Preset** and apply it to other files. This is a handy tool if you have specific values you need to apply to a large set of assets. This capability is similar to Bridge's built-in Metadata Templates, which are found in the Tools menu. A key difference is that the Presets in the Custom Metadata Panel can include metadata that Bridge's Templates cannot see, as they are governed by the File Info panel.

	When you create a Metadata Preset, all of the fields with values in the current View will be added to the Preset. No other metadata will be included in the Preset. You can then apply those values to other assets.

2.	To create a Metadata Preset, select an asset, then type a name for the Preset in the Metadata Preset field at the bottom of the panel. Once finished, click the **+** button to add your Preset to the list. You may need to scroll up to see the Presets, as they are at the very bottom of the window.

	![New Metadata Preset](Images_CEP_%20Adobe%20Bridge%20User%20Guide/New_Metadata_Preset.png)

3.	To apply a Metadata Preset, select one or more assets and choose a Preset from the Metadata Preset Dropdown at the bottom of the panel. The fields that will change or get new metadata values will turn green. The Metadata Preset tool will override existing metadata in files, so check to ensure that you are not replacing important information. For safety, these new values will not be applied until you click **Save Changes**. 

	![Apply a Metadata Preset](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Apply_a_Preset.png)

### **Managing Conflicting Metadata Values**
1. A common task for asset managers is to merge metadata across many assets. The Custom Metadata Panel provides a way to merge metadata in specific fields. When you select two or more files, the Panel will alert you if there are multiple values for any given field in the selection. You can then choose one of the files' values for that field to replace all of values across the selection, or you can merge all of the values across the selection.

	For instance, if you have three files with different values for pet breed, you can decide that one of the files' breed will replace the breed for the other two files. For Tags, AEM Tags, Multi-Text and Multi-Dropdown, all files will inherit the union of all values with no duplicates. For Text fields, all files will inherit a semicolon separated list. 
	
2.	In the example below, the selection has many fields with multiple values. Each field with multiple values presents a warning flag. Those fields now have a Multiple Selection Resolution button. Click the button to see the choices.

	![Multi-Selection Resolution](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Multi-selection-resolution.png)

3.	You can preview the choices by hovering over each item in teh Multiple Value Actions dropdown.

	![Hover over a choice](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Hover_over_a_choice.png)

4.	Click an item in the list to set the value for the selection. The Field will turn green to indicate that you will make a change when you click **Save Changes**. 

### **Reverting Changes**
1.	In case you make a mistake, you can revert the last changes you made if you do not change your file selection. Once you select new assets or deselect your assets, you will not be able to revert your changes.

2. Once you commit a change by clicking **Save Changes**, the **Revert Changes** button will activate. Click it to revert the changes you just made. You must click **Save Changes** again to complete the reversal.

	![Revert Changes](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Revert_Changes.png)

###	**File Info Panel**

1. **File Info** offers forms similar to what Bridge displays in its built-in metadata forms. Common schemas are visible by clicking their names in ths list on the left hand side of the window. 

	File Info forms are extensible using the [XMP Metadata UI SDK](https://www.adobe.com/devnet/xmp.html). Any custom forms made with the UI SDK will be available everywhere File Info is available, including other Adobe Desktop applications. Custom Metadata Panel for Bridge does not use FileInfo, so any forms you make with Custom Metadata Panel will not appear in File Info, although data may appear in other form fields.
	
	You can use File Info to confirm that your metadata changes have been applied to the file. Click on **Raw Data** to view the raw XMP metadata as XML.

	![Raw Data](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Raw%20Data.jpg)

### **Using the View Editor**

1.	Metadata forms are called **Views**. Views are JSON files that can be edited manually or by using the **View Editor**. The Custom Metadata Panel for Bridge ships with an example View that includes all of the available form elements. It references some common metadata schemas and a custom metadata schema for a fictional Pet Rescue organization. You will likely want to adjust the View or create your own from scratch.

	The Custom Metadata Panel supports local and remote Views. To access the Settings, deselect all files in your Bridge window and then click the gear icon to open the Settings panel. You can also choose **Settings** from the flyout menu. 

	![Accessing View Editor](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Accessing%20Configurator.jpg)

	You can import Views from a URL using the **Network Location** field. If you use URL, then you may need to provide access credentials, based on your server settings. We recommend that View JSON be publicly available to your users to avoid any access issues. Using URL-based View definition makes it easy for an administrator to centrally manage a View for a workgroup. 
	
	***Important note:** URL-based Views may not be editied directly using the View Editor. It is possible to save the JSON locally, and then edit it.*
	
	You can also by dragging and dropping a View onto your Settings panel. You can use a server-based file location, so long as you have read access to the server folder. It is common for an Asset Manager to create one or more Views and share them with their content creators, who can drop them onto the Settings panel as needed. You can see the path to the current View at the bottom of the Settings screen.

	![Metadata View Location](Images_CEP_%20Adobe%20Bridge%20User%20Guide/PathToViewDefinition.png)

	Once you load a new View, either by Network location or by drag and drop, you will need to save the View location and reload the panel. Click **Save JSON Location** to save your new View. Click **Done** to exit Settings and load the View.

	![Save JSON Location](Images_CEP_%20Adobe%20Bridge%20User%20Guide/saveJSONLocation.png)


2.	To open the View Editor, click **Open View Editor**. 

	![Accessing View Editor 2](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Accessing%20Configurator%202.jpg)

3.	This opens the **View Editor** Panel. Once here, you can add metadata fields and/or edit existing metadata fields. 
	-	To create a new metadata field, click **Add Metadata**.
	-	To access existing metadata fields, click the **pencil icon** next to the applicable metadata field.

	![Accessing Metadata Fields](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Accessing%20Metadata%20Fields.jpg)

4.	Once you edit or create a new metadata field, you will be presented with a pop-up like the one below. You must enter values on the Basic tab before you can enter values in other tabs. *Note: some common metadata properties have specific structures. Be sure you know what kind of data your desired property will accept before making a field with the Custom Metadata Panel.* 
	-	On the **Basic** tab, you can must enter the following properties for each Field:
		-	**Field Type** Choose from one of the options described in detail below
		-	**Display Name** The name of the field you want to display in the View when a user selects a file
		-	**XMP prefix** The short name for the XMP namespace in which your property resides. For instance, the **Dublin Core** namespace has an XMP prefix of `dc`.
		-	**XMP namspace** The URI that points to the XMP namespace definition in which your property resides. For instance, the  **Dublin Core** namespace has an XMP Namespace URI of `http://purl.org/dc/elements/1.1/`
		-	**XMP property name** The name of the specific metadata property to which you want to write the value of this field. For instance, within the Dublin Core namespace, the property `subject` is used for the Keywords that have been applied to an asset by Creative Cloud applications.
		-	**Read Only** You can set a field as read only. This will prevent users from entering data into this field.

	-	Other tabs may appear, based on the field type. Specific options for each field type are outlined below.

	![Managing Metadata Fields](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Managing%20Metadata%20Fields.jpg) 

5.	In the **Field Type** Dropdown, a user can select the type of metadata field they would like to create. A user can choose one of the following Field Types:
	-	**AEM Tags** is a special case. We have pre-filled the properties for you on the Basic tab. After configuration, your tags will be available for entry in the panel. 
		-	This panel requires specially formatted JSON, which you will need to get from your AEM instance. You may need to contact your AEM administrator for assistance.
		-	For AEM 6.3 and under, this can be found at `your_AEM_URL/etc/tags.tagtree.json`
		-	For AEM 6.4+, this can be found at `your_AEM_URL/content/cq:tags.tagtree.json`
		-	Copy and paste the JSON from your browser into the **Options** panel to configure the field options.
		-	 Users will now have access to the same tags that are configured in AEM.
		-	 You can optionally use **Dependencies** to set one or more fields that must have data before a user can enter data in this field. This field will be disabled until there is a value present in the field you specify in **Dependencies**.
		-	To configure, choose one or more fields from the **Dependencies** dropdown in the **Advanced** tab. The dropdown will display all currently defined fields, so you will need to define fields before you can use them as Dependencies for other fields.

	-	**Date** fields alow users to select dates. The date picker will allow users to select a date and time from a calendar. It allows users to type values, and it will attempt to format the text as a date if necessary.
		-	You can optionally use **Dependencies** to set one or more fields that must have data before a user can enter data in this field. This field will be disabled until there is a value present in the field you specify in **Dependencies**.
		-	To configure, choose one or more fields from the **Dependencies** dropdown in the **Advanced** tab. The dropdown will display all currently defined fields, so you will need to define fields before you can use them as Dependencies for other fields.

	-	**Dropdown** fields allow users to select one value from a menu. 
		-	You can configure the values in the **Options** tab.
		-	Dropdown fields require an array of options. If you enter an array, the menu will display the values and will use those values when it writes XMP. For example,

   	    	```javascript 
			["dog", "cat", "bird"]
			```
          	You can also provide a label for each item to make it easier to read or if your users are familiar with another term for the value. Format your array to include `label` and `value` pairs for each item. The dropdown will show the `label` in the menu, but it will read and write the `value` from XMP. For example, this JSON makes a Dropdown for a field called *Pet Type* that describes the kind of pet in the photo.
			```javascript
		  	[
				{ "label": "Doggy", "value": "dog" },
				{ "label": "Kitty", "value": "cat" },
				{ "label": "Birdy", "value": "bird"}
			]
			```
          	
            #### Dependencies
			You can use **Dependencies**  in the **Advanced** tab to set one or more fields that must have data before a user can enter data in your Dropdown. Any field with Dependencies will be disabled until there is a value in each of the Dependency fields. For instance, you might want to disable the *Breed* dropdown until the *Pet Type* dropdown has a value. See **Dependencies** below for more details.
          
            #### Filter Options
			You can use **Filter Options** to specify one field whose value will be used to filter the values in your dropdown. See **Filter Options** below for more details on setting the Filter Options parent field. 
			
			Filter Options are defined by the `parent` key. You can use a single text value or an array of acceptable values, and the values must exactly match the `values`, not the `label`, from the field you choose in Filter Options.
          
            For example, if you had a Dropdown field called *Pet Type* with values "dog", "cat" and "bird", you could make a second field called "breed" that uses Pet Type to filter its options based on the value of `pet`. When the user selects "cat" as the breed, the menu defined below would show "Maine Coon" and "Other," because those have "cat" in their parent.
          
          	```javascript
			[
                { 	
					"label": "Schnauzer",
					"value": "schnauzer",
					"parent": "dog" 
				},
                {
					"label": "Maine Coon",
					"value": "maine_coon",
					"parent": "cat"
				},
                {
					"label": "Parrot",
					"value": "parrot",
					"parent": "bird"
				},
                {
					"label": "Other",
					"value": "Other",
					"parent": ["dog", "cat", "bird"]
				}
            ]
			```
			
	-	**Multi-Dropdown** fields allow users to select multiple value from a menu. It is functionally identical from a Dropdown, but it has an additional advanced configuration option: **Selection Groups**.
		-	See **Dropdown** for details on basic configuration options and Dependencies.
	
			#### Selection Groups
			You can use **Selection Groups** to connect one or more items together to make bulk selection easier. Selection Groups are defined by the `group` key, and they require an array. When a user selects an item, all items whose `group` matches the selected item's `value` will also be selected. Selection Groups are common when certain values are usually selected together, such as product families or related items.

			For example, if a user selects "All Dogs" from the dropdown defined below, the `value` will be `all dogs`. This will automatically select all of the items with the group that matches `all dogs`. Groups can contain arrays of values, so items can belong to one or more selection group

			```javascript
			[
                { 	
					"label": "All Dogs",
					"value": "all dogs",
					"parent": "dog",
					"group": ["all dogs"]
				},
				{ 	
					"label": "All Cats",
					"value": "all cats",
					"parent": "cat",
					"group": ["all cats"]
				},
				{ 	
					"label": "Schnauzer",
					"value": "schnauzer",
					"parent": "dog",
					"group": ["all dogs"]
				},
				{ 	
					"label": "Doberman Pinscher",
					"value": "doberman",
					"parent": "dog",
					"group": ["all dogs"]
				},
				{ 	
					"label": "Chinook",
					"value": "chinook",
					"parent": "dog",
					"group": ["all dogs"]
				},
                {
					"label": "Maine Coon",
					"value": "maine_coon",
					"parent": "cat",
					"group": ["all cats"]
				},
				{
					"label": "Persian",
					"value": "persian",
					"parent": "cat",
					"group": ["all cats"]
				},
                {
					"label": "Parrot",
					"value": "parrot",
					"parent": "bird",
					"group": ["all birds"]
				},
                {
					"label": "Chicadee",
					"value": "chicadee",
					"parent": "bird",
					"group": ["all birds"]
				},
				{
					"label": "Other",
					"value": "Other",
					"parent": ["dog", "cat", "bird"],
					"group": ["Other"]
				}
            ]
			```

-	**Text** fields provide a single free-form text entry for a property. 
	-	Any text can be included, and there are no configuration options.

-	**Multiple Text** fields allow users to create multiple free-form text entries for a property.
	-	These entries will be included in a bag in the XMP for the designated property.
	-	Any text can be included, and there are no configuration options.

-	**Section Divider** is used to separate metadata into logical blocks in your form. 
	-	Dividers only require a Display Name, which will be used as the divider message.

-	**Tags** fields let you constrain the values of a property while allowing entry of multiple values. This is commonly used in keywords-like scenarios where you want to limit what tags a user can apply. Tags fields will auto-complete when a user starts typing values. Tags only accepts arrays of text as its Option.
	-	Similar to a dropdown, you configure the tag values in the **Options** tab.
	-	Tags do not support `label`, `parent` or `group`. For example, the following options will constrain the field to the three possible values `dog`, `cat` and `bird`. 
	```javascript 
			["dog", "cat", "bird"]
	```

6.	As noted above, all field types (except for Section Divider) will require a user to enter metadata namespace details. Here are some helpful tips for identifying common metadata namespace details using File Info:
	-	You can find the XMP namespace and prefix in the Raw Data panel. At the top of the Raw Data, there is a list of all of the namespaces defined in the file. These will start with the tag xmlns: and will follow the pattern xmlns:`prefix`="`namespaceURI`"
	-	In the example shown below, the prefix is `dc`, and the namespace URI is `http://purl.org/dc/elements/1.1` 
	-	You can also find the XMP Property Name in the Raw Data. Property tags have the form <`prefix`:`propertyName`>
	-	In the example below, the entry for Keywords is highlighted. Keywords uses the property called `subject` in the namespace whose prefix is `dc`.
	-	It is common to add metadata to a file and then view the resulting formatting in File Info. Record the Namespace URI, Prefix and property for use in your View.

	![Raw Data Specifics](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Reading%20Metadata%20from%20File%20Info.png)

#### **Assigning Dependencies**

1.	As noted above, you have the option to assign one or more **Dependencies** to all field types. Dependencies must be met in order for the field to become active for the user. While you define the specific dependency *values* in the **Options** tab via JSON, you define the dependency *sources* in the **Advanced** tab.
	-	Navigate to the **Advanced** tab in the View Editor. Click the dropdown menu and select one or more field names (as seen in the first image below). 
	-	Once you are finished, just click out and you should see the Dependencies show up as a placeholder in the Dependencies field (as seen in the second image below).
	-	You can remove Dependencies by selecting the field again from the dropdown menu.

	![Assigning Dependencies](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Assigning%20Dependencies.jpg)

	![After Assigning Dependencies](Images_CEP_%20Adobe%20Bridge%20User%20Guide/After%20Assigning%20Dependencies.jpg)

2.	Once you set Dependencies for a field, that field will be disabled until its parent field has a value. When a field is disabled, it will appear to be greyed out and will look similar to the image below. 

	![Dependencies in Metadata Panel](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Dependencies%20in%20Metadata%20Panel.jpg)

#### **Filter Options**

1.	Some fields (**Dropdown**, **Multi-Dropdown**) will also have **Filter Options**. You can use Filter Options to specify one field whose value will be used to filter the possible values in this field. While you define the specific Filter Options *values* in the **Options** tab via JSON, you define the Filter Options *source* in the **Advanced** tab.
	-	Your current field will filter down based on the value selected in the **Filter Options Source** dropdown. You can only select one source for Filter Options.
	-	You define the specific values for filtering using the `parent` key in the JSON. See the **Dropdown configuration options** for more details on how to construct the JSON options.
	-	*Tip: Filter Options work well when coupled with Dependencies. For instance, when a user selects a pet type, this can expose the breed while also filtering the options to match the chosen pet type. This helps to focus users on allowed values while reducing errors.*

	![Setting filters](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Setting%20filters.jpg)

2.	On the **Options** tab, a user can write values of the child field and assign a filter to these values. All coding on the **Options** tab must be done in JSON format. 
	-	Assign a `label` and a `value` to each option for the custom field. 
	-	Assign a filter by assigning the value of the parent field as `parent`.

	![Assigning Filters](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Assigning%20Filters.jpg)

3.	Once you are satisfied with your changes, click **Save** to exit the metadata field. 

4. To save all of the changes that you have made in the View Editor, click **Save**. Close the window to exit the View Editor.

	![Save and Close the view editor](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Custom_Metadata_Panel_-_View_Editor.png)

5. To load your new View, click **Done**. The Custom Metadata Panel will now reload with your new View settings.

#### Managing Views
1. You can export your View as JSON to share it with coworkers or customers. In the View Editor, click **Export to JSON** to save your JSON to a local drive or a server volume.

2.	It is common for admins to create Views and share the JSON with their users via Export to JSON. You can also place the exported JSON on a web server to use the Network Location capability found in the **Settings** Tab. 

![Export view to JSON](Images_CEP_%20Adobe%20Bridge%20User%20Guide/Custom_Metadata_Panel_-_View_Editor_Export.png)