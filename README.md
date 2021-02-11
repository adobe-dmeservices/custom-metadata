# Custom Metadata Panel
## Focus your attention on critical metadata in this configurable form. Mix and match standard and custom metadata fields to show the properties critical to your business.

The Custom Metadata Panel provides Enterprises and individuals with a way to focus their attention on critical metadata in one panel.

The panel is completely customizable and helps end users and DAM managers tune their metadata view for maximum accuracy and efficiency. With 7 form field types and metadata presets, it expands the metadata capabilities of Bridge without using XML or special coding.
Form fields include:
* Text
* Multiple Text
* Tags (like Keywords)
* Dropdown
* Multi-select Dropdown
* Date Picker
* AEM Tags (special case just for Adobe Experience Manager)

Other features include a read-only entries, section dividers, a built-in form editor, form definition file import and export, and the ability to use a URL as the location for the form. This last feature is ideal for Enterprise or group applications, where a DAM Manager posts the form to a common location and all users get the latest and greatest.

Read the [User Guide](https://github.com/adobe-dmeservices/custom-metadata/wiki) for more details.

Exchange link to panel: https://exchange.adobe.com/creativecloud.details.103752.html

***Enterprise Admins can now include this and other extensions when they create Managed Packages in the Admin Console. [Read the Help Documentation here.](https://helpx.adobe.com/enterprise/using/create-nul-packages.ug.html#Managedpackages)*** Search for Custom Metadata Panel during step 7 to include it and other Extensions in your Managed Package.

***For Enterprise customers who cannot create Managed Packages to deploy Marketplace extensions, we have made it available as a Release. See the Releases link to get the latest version.***

See a video tour at https://www.youtube.com/watch?v=_IoMGJiEHss

Special thanks to Martin Gersbach for creating a [repository of useful config files for common metadata namespaces and properties](https://github.com/MuseosAbiertos/Adobe-Bridge-Custom-Metadata-JSON-Presets).

## Changes for version 1.3.0

### Added
*[See the User Guide](https://github.com/adobe-dmeservices/custom-metadata/blob/master/User%20Guide.MD) for more about these new features*
* Changed name to Custom Metadata Panel
* Added support for Photoshop and Illustrator
* Added multi-line text fields
* Allow special characters in Configurator
* Squashed some UI bugs

### Fixed
* Several bugs

## Changes for version 1.2.0

### Added
* Support for Seq and Bag arrays in Tag, Multi-Text and Multi-Dropdown fields
* Ability to reorder Multi-Text items
* Ability to edit Multi-Text items
* Improved UI for adding Multi-Text items
* New Pending change dialog
* Improved UI for showing which fields will change when user saves changes

### Fixed
* Several bugs
* Removed Configurator from the Window>Extensions menu
* Fixed Tag deletion issue in Multi-Dropdown
* Added validation when saving and exporting View templates
* Help text in Configurator window better reflects the items being edited


## Changes for version 1.1.0

### Added
*[See the User Guide](https://github.com/adobe-dmeservices/custom-metadata/blob/master/User%20Guide.MD) for more about these new features*
* Field Dependencies for all field types
* Filtering based on another field value in Dropdowns and Multi-Dropdowns
* Auto Group Selection in Multi-Dropdown
* Natural Language Date parsing for Date Field
* Multiple Values resolution workflow and menu for Bulk Selection Mode

### Fixed
* Several bugs
* Updated the About screen
