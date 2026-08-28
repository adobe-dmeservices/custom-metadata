# Custom Metadata Panel
### Focus your attention on critical metadata in this configurable form. Mix and match standard and custom metadata fields to show the properties critical to your business.

The Custom Metadata Panel provides Enterprises and individuals with a way to focus their attention on critical metadata in one panel.

The panel is completely customizable and helps end users and DAM managers tune their metadata view for maximum accuracy and efficiency. With many form field types and available metadata presets, it expands the metadata capabilities of Creative Cloud Desktop applications without using XML or special coding.
Form fields include:
* Text and Multiple Text
* Language Alternatives for Text Fields
* Numbers and Multiple Numbers
* Tags (like Keywords) but with controlled vocabulary
* Hierarchical Tags
* Dropdown
* Multi-select Dropdown
* Date and Multi-Date
* Checkbox and Checkbox Group
* Switch and Switch Group
* Radio Buttons
* URL and Multiple URL fields that link to external web sites
* Complex structures
* Tables
* Calculation Fields
* Hidden fields
* Quicktime metadata properties for documents that support them
* Office Document metadata properties
* AEM-specific Fields
  * AEM Tags
  * AEM Smart Tags (read-only with optional push to XMP Keywords)
  * AEM AI Title (read-only with optional push to XMP Title)
  * AEM AI Description (read-only with optional push to XMP Description)
  * AEM AI Keywords (read-only with optional push to XMP Keywords)
* Read-only fields
  * Maps (uses XMP GPS fields)
  * Links (for compound documents like InDesign and Illustrator)
  * Swatches
  * Plates (inks)
  * Fonts

**Filter mode** lets you quickly filter your files in Bridge by any property in your Views!

**AEM Asset Link integration** When using Adobe Asset Link, you can view and modify asset metadata that is stored in AEM without affecting the local binary. You can also check-out linked assets from InDesign. 

Other features include a read-only entries, synced field values, section dividers, a built-in form editor, form definition file import and export, metadata Preset import and export, and the ability to use a URL as the location for the form. This last feature is ideal for Enterprise or group applications, where a DAM Manager posts the form to a common location and all users get the latest and greatest. For full docuentation, please see our [user guide](https://github.com/adobe-dmeservices/custom-metadata/wiki).

See the Table of Contents for help with using and configuring the panel.

Exchange link to panel: [https://exchange.adobe.com/creativecloud.details.103752.html](https://exchange.adobe.com/creativecloud.details.103752.html)

***Enterprise Admins can include this and other extensions when they create Managed Packages in the Admin Console. [Read the Adobe Help Documentation here.](https://helpx.adobe.com/enterprise/using/create-nul-packages.ug.html#Managedpackages)*** Search for Custom Metadata Panel during step 7 to include it and other Extensions in your Managed Package.

***For Enterprise customers who cannot create Managed Packages to deploy Marketplace extensions, we have made it available as a Release. See the [Releases section of this repository](https://github.com/adobe-dmeservices/custom-metadata/releases) to get the latest version.***

See a video tour at [https://youtu.be/48T_xxx_i6Y](https://youtu.be/48T_xxx_i6Y)

Special thanks to the following, who graciously created example Views that you can use when creating a new Tab:
- David Riecks, Michael Steidl and Brendan Quinn from [IPTC](https://iptc.org) for their collaboration and amazingly helpful feedback. 
- Martin Gersbach for creating a [repository of useful config files for common metadata namespaces and properties](https://github.com/MuseosAbiertos/Adobe-Bridge-Custom-Metadata-JSON-Presets).

## Changes for 2.0.27

### New: Cultural Heritage Imaging metadata example

- Added a new example View based on the Digital Object Architecture Working Group's (DOAWG) proposed minimum metadata schema for cultural heritage imaging and scanning software.
- The example is available from the examples menu when creating a new tab.
- It provides a ready-to-use starting point for capturing technical metadata used in cultural heritage digitization workflows.

### New: Paste spreadsheet data into option tables

- You can now copy a range of cells from Excel or another spreadsheet and paste it directly into an options table in the Configurator.
- Select the starting cell before pasting; tab-separated values fill columns and line breaks create rows.
- Existing rows are updated and additional rows are created automatically when the pasted range is larger than the current table.
- Quoted cells can contain tabs, line breaks, and double quotes. Comma-separated values pasted into array columns are converted into multiple values.
- Regular single-cell paste behavior is unchanged.

### Improved: Configurator and Tab Manager performance

- Dragging and reordering rows in the Configurator and Tab Manager is now smoother and more predictable.
- Corrected row placement when moving an item above or below another row, including moves to the end of a list.
- Reduced redundant updates during drag-and-drop and added a compact drag preview, improving responsiveness for larger Views.
- Option details are now prepared only when their dialog is opened, reducing work when displaying Views with large option lists.

### Improved: Remote View error reporting

- Remote View errors now identify whether the server returned an HTTP error, the response contained invalid JSON, or the remote location could not be reached.
- Error messages identify the affected View and include a **Copy Details** action for collecting the URL, status, response, or technical error information needed for troubleshooting.
- When one or more Views fail during startup, the panel now provides a clearer message and lets you copy the underlying error details.

### Fixed

- Fixed incorrect or inconsistent row ordering when dragging items in the Configurator and Tab Manager.
- Fixed unnecessary drag-state updates that could make large tables feel sluggish.
- Fixed lingering CEP context-menu and drag-preview state after an editor table is closed.

## Changes for 2.0.26

### New: Multi-select merging for Language Alternative fields

- Selecting multiple assets with different values in a Language Alternative field (such as a translated title or description) now offers a **Merge All** option that combines each language's values across the selection, in addition to the existing option to replace with a single file's value.
- Languages used by any asset in the selection are offered as editable alternates, even if they aren't part of the View's configured language list.

### New: AEM scheduled publishing dates (On Time / Off Time)

- The panel can now read and edit an AEM asset's **On Time** and **Off Time** properties — the scheduled publish and unpublish dates set in Experience Manager Assets — when a view includes them.
- These are the first Experience Manager Assets properties (beyond standard metadata) supported for editing; other advanced asset properties surfaced in a view remain read-only for now.
- Reminder: for a scheduled date to actually take effect, your AEM environment's publish and dispatcher-flush agents need scheduled publishing enabled — this is an AEM administration setting, not something the panel controls.

### New: PRISM metadata examples

Four new example views based on the W3C PRISM (Publishing Requirements for Industry Standard Metadata) specification are available from the examples menu when creating a new tab:

- PRISM Basic Metadata
- PRISM Image Metadata
- PRISM Usage Rights Metadata
- PRISM Rights Summary Metadata

### Improved: AEM checkout workflow in the Links panel

- Linked AEM assets now keep their AEM indicator (the red cloud badge) even after being checked out and synced locally, so it's always clear which linked assets live in AEM.
- Added a working **Cancel Checkout** button for AEM assets you've checked out. Since canceling discards any local changes and does not create a new version in AEM, a confirmation prompt now appears first — if you want to keep your changes as a new AEM version instead, use Check In in Adobe Asset Link.
- You can now click a linked AEM asset's name to select it in the InDesign document even if it hasn't been checked out yet, matching the existing behavior for other links.

### Improved: Quicker access to AEM asset details

- Added a button next to a selected AEM asset's file name that opens its properties page directly in Experience Manager Assets, in your default browser.
- The AEM sync button is now smaller and sits closer to the file name, matching other desktop-sized controls in the panel.

### Improved: Smoother scrolling in InDesign

- Removed a background check that ran continuously while the panel was open in InDesign, which could cause visible stutter when scrolling. InDesign's own selection-change notifications now handle this instead, so the panel stays just as responsive with less background work.

### Fixed

- A Language Alternative field with both a generic default value and a matching named-language value (for example, a description with both a default and an English translation) now displays and saves correctly as a single field, instead of appearing blank or losing the default value on save.
- Fixed a crash that could occur when editing certain Language Alternative fields, depending on the order languages appeared in the asset's data.
- Fixed a confusing tooltip that could read "Value inherited from" a language when it was actually the same language being displayed.
- Fixed a bug that prevented the multi-select merge menu from appearing on Language Alternative fields that have a configured list of languages (such as "Alt Text (Accessibility)").
- Fixed a bug where merging Language Alternative values across assets that each used a different language as their own default could produce a bogus extra entry instead of merging correctly.
- Fixed an issue where new example views (including the PRISM examples above) could fail to appear in the examples menu after a standard install.

## Changes for 2.0.25

## More reliable document detection

- The panel now more consistently recognizes the active document in Illustrator, InDesign, and Photoshop.
- Documents that were already open before the panel launched are detected correctly.
- Saving a new, previously unsaved document refreshes the panel automatically.
- Switching rapidly between documents is less likely to display metadata from the previous document.
- InDesign detection remains available for linked graphics, grouped content, placed documents, story links, AEM assets, cloud documents, and the active InDesign document.

## Safer AEM error handling

When metadata cannot be read from an AEM asset—for example, because the AEM instance is hibernating, the asset was moved, the user is signed out, or access is denied—the panel now:

- Displays a concise explanation of the general problem.
- Makes all metadata fields read-only to prevent changes based on incomplete data.
- Disables saving, presets, revert, and reapply actions until AEM metadata is available again.
- Provides a **Copy Error** button with detailed diagnostic information for support.
- Restores editing automatically after a successful AEM read or when a non-AEM asset is selected.

## Faster linked AEM assets in InDesign

- Fixed a regression that could repeatedly reload the same linked asset.
- Metadata requests are now shared across panel tabs instead of being repeated for each tab.
- Unnecessary metadata requests from the Preferences tab have been removed.
- AEM authentication and metadata requests are coordinated more efficiently.

## Improved startup reliability

- Required host scripts now finish loading before the panel begins reading metadata.
- Startup failures display a clear message instead of leaving the panel partially functional.
- Selection handling is more reliable after reopening the panel or restarting a host application.
- Bridge selection handling no longer interferes with event handlers installed by other Bridge scripts or extensions.

## Better support diagnostics

- The About screen now displays the version of the startup script currently loaded by the host application.
- This makes it easier to identify an outdated or missing startup script when troubleshooting document-selection problems.
- Error reports retain detailed file, location, and stack information when available, while normal notifications remain concise.



## Changes for 2.0.24

### AEM metadata is available regardless of checkout location

- A configured AEM instance is now always the metadata source for linked AEM assets.
- Metadata can be read from and written to AEM when an asset is checked out in another environment and no local copy exists.
- Checkout state now controls only whether metadata can also be synchronized to a local WIP copy.
- The experimental **Use AEM as the source of truth** preference was removed because this behavior is now the default.
- The **AEM Asset metadata unavailable** screen is shown only when the panel cannot access AEM and no usable local copy exists.
- The unavailable-state guidance now directs users to check their Asset Link connection or create a local copy by checking out the asset.
- The Links component now shows asset previews for linked AEM Assets.
- The Links report now shows the URL for linked AEM Assets.

### Windows AEM path handling

- Windows placeholder paths are normalized from backslashes to canonical AEM DAM paths.
- A valid `aems://` URI is used when an InDesign local path does not contain `/content/dam`.
- Local WIP paths are joined using the separator style of the configured checkout directory.
- Canonical DAM paths are used consistently for AEM requests, checkout lookup, caching, and local-copy discovery.

### InDesign selection handling

- Selecting a normal page object no longer causes the panel to treat every link on the page or spread as selected.
- Parent graphic lookup is limited to actual InDesign graphic-frame types: Rectangle, Oval, and Polygon.
- Direct links, linked graphics, grouped content, placed documents, and story links continue to be supported.

### Detailed error reporting

- Added a shared CEP error formatter that retains the error name, message, file, line, column, code, and stack when available.
- Added matching ExtendScript formatting for InDesign selection events and host-side XMP operations.
- Replaced raw string and numeric throws in affected production paths with `Error` objects so caller locations are retained.
- Clipboard error actions now format native `Error` objects instead of producing empty objects, `null`, or incomplete messages.
- AEM read failures now display an **Unable to read AEM metadata** notification with a **Copy error** action.
- ExtendScript's `.source` property is intentionally omitted so diagnostic reports do not include source-file contents.

### First-run stability

- Removed proof-of-concept Views from the default configuration when their template files are not guaranteed to be present.
- Existing settings created by version 2.0.22 are repaired on load by removing the three obsolete POC tabs and persisting the cleaned configuration.
- Only the exact legacy `{default}` View paths are removed; similarly named user-created Views remain untouched.
- New users no longer receive a missing-View error when the panel creates its initial settings file.

## Changes for 2.0.22

### AEM Assets & AEM Tags
- **AEM is now the source of truth** for linked AEM Asset metadata, regardless of local check-out status — with a "Fetch from AEM" refresh across InDesign links and Photoshop/Illustrator/InDesign active docs.
- **New AEM Tags configurator** connects directly to your AEM instance (via Adobe Asset Link) to browse and select tag namespaces, with a manual-JSON fallback for users without Asset Link.
- **View and promote AI-generated metadata** — new fields display AEM's AI/CV-generated Smart Tags, title, and description, and let you promote them into standard XMP properties (`dc:subject`, `dc:title`, `dc:description`).
- Supported in InDesign, Photoshop (Intel), Illustrator, and Bridge.

### New Hierarchical Tags Field
- Constrained-vocabulary tag field with a tree-browser UI, for multi-value hierarchical taxonomies (e.g. IPTC Media Topics).
- New example Views included: IPTC Media Topics (flat and hierarchical) and IPTC Genre.

### Language Alternative Support
- New **"Store as Lang-Alt (default only)"** option lets Dropdown, Number, Date, Checkbox, Switch, Radio Group, and URL fields correctly read/write XMP properties that are defined as Language Alternatives, without exposing per-language editing.

### Fixes
- Filter Options and Dependencies now work correctly for fields nested inside a Structure.
- Copying a property into another View (or duplicating one within the same View) no longer breaks its Dependencies or Filter Options relationships.
- Fixed a bug that could display unsupported properties incorrectly in Lightroom Classic.


## Changes for 2.0.21
### New Field Types (read-only, Bridge/InDesign/Photoshop/Illustrator/Premiere Pro only)

#### Map
Read Only. Displays an interactive map using the file's EXIF GPS coordinates (`exif:GPSLatitude`, `exif:GPSLongitude`, `exif:GPSAltitude`). The map is rendered via Leaflet/OpenStreetMap and shows a pin at the captured location. Configurable map height.

#### Swatches & Plates
Read Only. Reads the color swatches and ink plates embedded in the file (InDesign, Illustrator). Swatches are displayed as color chips with their names. Selected swatches can be exported to an `.ase` file. Plates shows the underlying ink separations.

#### History
Read Only. Displays the modification history of the file from XMP history metadata (`xmpMM:History`). Shows each history entry with its action, timestamp, and software agent.

#### Links
Read Only. Displays the linked items embedded in the file (InDesign, Illustrator). Each link shows its path, status, and modification date. Links can be opened in the file system and a links report can be exported.

#### Fonts
Read Only. Displays the fonts used in the file. Each font entry shows the font name, type, and whether it is embedded. A fonts report can be exported.

---

### New Feature: Filter Mode

Views can now include a Search field that filters all visible fields by their current values. This allows users to quickly find properties by value within a large View.

---

### New Number Field Options

#### EXIF Rational Format (`rational`)
Number and MultiNumber fields can be configured with `rational: true`. When enabled:
- XMP stores values as EXIF rational strings (e.g. `169/1`, `12/5`)
- The field displays the equivalent decimal (e.g. `169`, `2.4`)
- On write, decimal input is converted back to a rational string using GCD simplification
- Useful for `exif:GPSAltitude`, `exif:FNumber`, `exif:FocalLength`, and similar EXIF properties

#### Rational Decimal Precision (`rationalPrecision`)
Optional companion to `rational`. When set (0–10), limits the decimal display to that many places (e.g. `168.1234` → `168.12` with precision 2). Leave blank to show all digits.

#### Display Unit (`unit`)
All Number, MultiNumber, and Table Number columns can have an optional unit label (e.g. `m`, `°`, `fps`):
- Appears inline with the value when the field is idle (`168 m`)
- Hides when the field is focused for editing (only the number is shown)
- Display-only — not stored in metadata

---

### What's New Panel

- **Layout**: Heading, carousel, and pip navigation now use a proper flex column layout filling `100vh`. The page no longer scrolls vertically.
- **Scrollable description**: Only the text description area scrolls; the screenshot image stays fixed above it.
- **Pip navigation**: Replaced `StepList` (a wizard-style component that rendered connector dashes between each step) with simple circular dot indicators. Dots are 8px, with 8px gap, opacity-based active/inactive states, and click-to-navigate.


## Changes for 2.0.20
### Lightroom Classic Update

  This release improves the multi-text field in Lightroom Classic. It now shows all of the current values in a scrollable list. Users can select items for reordering, updating and deleting. 

### Hierarchical Keywords support

Custom Metadata now supports hierarchical keywords in Bridge and Lightroom Classic. Users can create hierarchical values using the pipe character `|` to separate levels in the hierarchy.
  
---

  ### Bug Fixes

  - **Lightroom Loading Loop** — If you select a View that has no Fields that Lightroom supports, the panel no longer goes into an inescapable loading loop.

  ### Improvements

  - **Crash hardening** — Trapping more rare error conditions.

## Changes for 2.0.19
### Lightroom Classic Support

  This release introduces a complete Lightroom Classic plugin that brings Custom Metadata Panel's view-based metadata editing to Lightroom's Library module.

  **How it works.** The plugin reads your existing CMP view templates directly from the shared settings file — the same JSON you configure in Bridge or Photoshop. At Lightroom startup, it registers all custom fields from all your views into Lightroom's metadata schema. From the Library menu, **Library > Custom Metadata > Edit Custom Metadata…** opens a dynamically generated editing dialog built from your active view template. Because the template is reloaded fresh on every open, any changes made in the CMP Configurator appear immediately in Lightroom without restarting.

  **XMP read/write.** Lightroom Classic does not provide full programmatic XMP access, so the plugin ships with a companion command-line tool (`xmp-cli`) for both Mac and Windows, built on Adobe's official XMP Toolkit SDK. When saving metadata, the plugin writes through the CLI to embed XMP directly in the photo file and also writes a `.xmp` sidecar alongside it. On read, it follows a fallback chain: sidecar on disk → embedded XMP in the file → Lightroom's cached xmpPacket. On Windows, the CLI runs as a persistent background daemon during the Lightroom session to avoid a console window flashing on every metadata operation.

  **Field type coverage.** Nearly all CMP field types render natively in the dialog: text, number, URL (with an Open button), date/time picker, checkbox, switch, radio group, dropdown, tags, multi-select, checkbox group, multi-text, language alternatives, structure, and calculated/read-only fields. Fields that are inherently unsupported in Lightroom — Camera Metadata (QuickTime atoms), Office Metadata, AEM Tags, and Premiere Pro Clip metadata — are skipped. Structures with array types (bag/seq) are fully editable with item navigation and add/remove controls.

  **Multi-photo editing.** Selecting multiple photos and opening the dialog shows the common value for each field. Fields with differing values across the selection are left blank; saving writes only the fields the user explicitly edits.

  **Metadata panel integration.** A "Custom Metadata CEP" entry appears in the Library module's Metadata panel dropdown, showing all registered custom fields alongside standard Lightroom fields (filename, folder, title, caption).
  
---

  ### Bug Fixes

  - **Locked folder detection** — Files in non-writable folders are now detected and treated as read-only, rather than surfacing an obscure XMP error (code 1000).
  - **Premiere Pro / InDesign "file locked" error** — Resolved an issue where saving metadata in Premiere Pro and InDesign could falsely report the file as locked.
  - **UI warning for `https://` XMP URIs** — Added a visible warning when a View is configured with an `https://` URI, which is not supported by the XMP SDK.

  ### Improvements

  - **Crash hardening** — Null guards and proper error propagation added across the ExtendScript host and CEP JavaScript layers to address a range of edge cases that could silently fail or crash the panel.
  - **Cleaner error messages** — XMP errors no longer include the full ExtendScript source listing; only the file name and line number are reported.
  - **Settings page layout** — Preferences footer is now properly anchored with a two-column layout (checkboxes left, action buttons right-aligned), fixing a layout anomaly in Premiere Pro.

## Changes for 2.0.17
**Quality of life improvements including:**
- Close and Save buttons to Tab and View editors. These are contextually aware and will prompt the user if they have unsaved changes
- Redesigned the Tab and View editor tables to include contextual copy, paste and delete
- Preferences layout improvements. Info window now scrolls and bottom buttons/checkboxes are always visible
- Updated font scaling methods
- some bug fixes
![https://raw.githubusercontent.com/adobe-dmeservices/custom-metadata/refs/heads/master/Images_CEP_%20Adobe%20Bridge%20User%20Guide/close_and_save.gif](https://raw.githubusercontent.com/adobe-dmeservices/custom-metadata/refs/heads/master/Images_CEP_%20Adobe%20Bridge%20User%20Guide/close_and_save.gif)

## Changes for 2.0.15
- **Office Document and Quicktime Metadata Support in InDesign**
 - **Office and media file Integration**: Automatically detect Office and media files linked in InDesign layouts
 - **Linked Text Frame Detection**: Select text frames with linked Word documents to view/edit metadata
- **Linked Table Detection**: Select tables with linked Excel spreadsheets to view/edit metadata  
 - **Seamless Workflow**: Read and edit metadata directly from InDesign without switching to Bridge

### Office Document Support in Bridge
- **Word, PowerPoint & Excel Integration**: Automatically detect Office files in Bridge selections
- **Full metadata access**: Read and write all pre-defined and custom Office metadata properties


- ## Changes for Version 2.0.14

### Enhanced Quicktime Metadata Support
- **Dependencies and Sync to Another Field**: You can now configure Dependencies and Sync to another field options for Quicktime Metadata fields, providing the same powerful workflow automation available for XMP fields.

### Improved Calculation Field Editor
- **New Calculation Editor**: Introduced a completely redesigned calculation editor that makes it easier to build and manage complex formulas:
  - Visual field picker for easy variable insertion
  - Function library with categorized functions (Math, Text, Date/Time, Logic, Aggregation)
  - Syntax highlighting and error detection
  - Real-time formula preview
  - Support for cursor positioning and editing
- **Quicktime Metadata Support**: Calculation fields can now reference Quicktime metadata properties, enabling calculations that combine XMP and Quicktime data.

### Time Zone Support for Date Fields
- **Date Field Time Zones**: Added comprehensive time zone support for Date and Multi-Date fields:
  - View and edit the GMT offset for each date value
  - Automatic conversion to user's local timezone (optional)
  - Preserves original time zone information
  - Compatible with ISO 8601 date format

## Bug Fixes

### InDesign Unicode Character Support (Critical)
**Problem**: Property names containing spaces (encoded as `ↂ0020` unicode markers) failed to save when editing InDesign document metadata directly, despite working correctly in Bridge and for InDesign linked assets.

## Changes for Version 2.0.13

### Introduces Quicktime Metadata Field Type

This release introduces a major new field type: **Quicktime Metadata**. This field type allows users to read and write embedded camera metadata directly in video files (MP4/MOV) without requiring XMP namespace configuration.

#### Key Features

* **16 Supported QuickTime Atoms** for comprehensive metadata coverage:
  * **Camera & Technical**: Image Rating (`urat`), Manufacturer (`manu`), Camera Model (`modl`), Encoding Tool (`©too`)
  * **Production Credits**: Director (`©dir`), Producer (`©prd`), Writer (`©wrt`), Artist (`©art`)
  * **Content & Description**: Title (`©nam`), Description (`©des`), Comment (`©cmt`), Keywords (`keyw`), Copyright (`©cpy`)
  * **Media Library (iTunes-style)**: Album (`©alb`), Genre (`©gen`), Year (`©day`)

* **Interactive Star Rating Display** for the Image Rating field
  * 5-star rating component (0-5 scale maps to 0-100 internally)
  * Users can click to set ratings interactively

* **Optional XMP Synchronization** - Write to both QuickTime atoms AND corresponding XMP properties
  * User-controlled on a per-property basis via "Sync with XMP" checkbox
  * Automatic mapping to standard XMP properties (e.g., `urat` → `xmp:Rating`, `manu` → `tiff:Make`, `©nam` → `dc:title`)
  * Supports all 16 QuickTime atoms with appropriate XMP equivalents
  * Handles special cases: alt-lang properties, array types, and value conversions (e.g., rating 0-100 scale converts to 0-5 scale)
  * Configurator displays which XMP property will be synced for each atom

* **Camera Metadata Example View** included with organized sections:
  * Camera & Technical information
  * Production Credits
  * Content & Description
  * Media Library (iTunes-style)

### Improved Property Name Handling

* **Space Support in Property Names** - Makes Acrobat custom properties easier to use
  * Spaces automatically convert to `ↂ0020` unicode character internally
  * Seamless bidirectional conversion for user-friendly editing
  * Type property names naturally with spaces (e.g., "My Custom Property")
  * Stored correctly as `Myↂ0020Customↂ0020Property` for XMP compliance

* **Enhanced Prefix Validation** - Prevents invalid prefixes
  * Spaces are now blocked in XMP prefix field
  * Clear error messages guide users to XMP-compliant naming

### Technical Notes

* Quicktime Metadata fields work with MP4 and MOV files that use the QuickTime container format
* The panel safely handles files without existing `udta` atoms by creating the necessary structure
* All metadata operations preserve video playback integrity by updating internal file pointers
* Compatible with Bridge, and works alongside existing XMP metadata fields

### Fixed

* Improved unicode character support for property names (spaces and `ↂ` character)
* Enhanced validation messages for property names and prefixes
* Better error handling for unsupported file types
![Quicktime Metadata](https://raw.githubusercontent.com/adobe-dmeservices/custom-metadata/refs/heads/master/Images_CEP_%20Adobe%20Bridge%20User%20Guide/Quicktime.gif)
---

This release significantly expands the panel's capabilities for video professionals, camera operators, and media asset managers who need to work with embedded camera metadata in their video files. The optional XMP sync feature ensures maximum compatibility with other Adobe applications and DAM systems.

## Changes for 2.0.12
This release improved linked item support for Custom Metadata in InDesign. InDesign documents often include linked Library items, Cloud Documents, and even AEM Assets. While Custom Metadata can directly inspect metadata from traditionally linked assets, Cloud objects don't have the same properties available. To make it easier to inspect metadata for these items, we have introduced round trip workflows.

### Linked Library Items
When you select a linked Library item, its original application may be available to view and edit metadata. If so, Custom metadata will display the option to view metadata in the originating application.

### Linked Cloud Documents
InDesign supports placing Photoshop and InDesign Cloud documents. Custom Metadata will now allow you to open linked Photoshop Cloud Documents directly from Custom Metadata. You will need to open linked Cloud InDesign documents from the Home screen.

### Linked AEM Assets
When a local copy of a linked AEM Asset is not available to InDesign, Custom Metadata will now present a button to open the asset's Properties page in AEM. You can then view both XMP and AEM metadata. If you check out the linked asset from Asset Link in InDesign, then Custom Metadata will have a local copy and can display the asset's XMP metadata directly.

![InDesign](https://raw.githubusercontent.com/adobe-dmeservices/custom-metadata/refs/heads/master/Images_CEP_%20Adobe%20Bridge%20User%20Guide/linked_cloud_library.gif)

## Changes for 2.0.11
### UI text resize and Asset Link support for InDesign
Users can now resize the text in Custom Metadata Panel screens. This control is available from the flyout menu and also from the context menu (right-click). Preferences are also available from the context menu. ***NOTE: You must enable System Contextual Menus in Settings to see the menu***

Users can also view and edit XMP metadata for checked out linked AEM Assets when using AEM Asset Link. Check out is required to access XMP, because check out downloads the full binary to your computer. When you are done editing metadata, you can check the asset back in to send the changes back to AEM.

![InDesign](https://raw.githubusercontent.com/adobe-dmeservices/custom-metadata/refs/heads/master/Images_CEP_%20Adobe%20Bridge%20User%20Guide/resizeview.gif)

## Changes for 2.0.9 & 2.0.10
### Improved InDesign support
This clarifies whether a linked asset's XMP metadata can be viewed or edited. Since InDesign does not provide a way to read or write the full XMP packet to and from Library items and linked Cloud Documents, we now tell you that in the UI. We also don't yet support editing metadata for linked AEM Asset Link assets, but we are working on that and should have a solution shortly.

![InDesign](https://raw.githubusercontent.com/adobe-dmeservices/custom-metadata/refs/heads/master/Images_CEP_%20Adobe%20Bridge%20User%20Guide/InDesign.gif)

## Changes for 2.0.8
### InDesign support
This release brings Custom Metadata to InDesign. You can view and edit XMP metadata for the active InDesign document and also any linked assets that support XMP. InDesign Cloud Documents and multiple selections are also supported.

This release also fixes some irregularities with multiple selections that may have resulted in unexpected values being written to the form when choosing "Merge Values." It also allows merging of Text fields that are Language Alternatives with no defined alternative languages, such as Description in Dublin Core.
![InDesign](https://raw.githubusercontent.com/adobe-dmeservices/custom-metadata/refs/heads/master/Images_CEP_%20Adobe%20Bridge%20User%20Guide/InDesign.gif)

## Changes for 2.0.7
### Preset import and export
This release adds the ability to import and export Metadata Presets from the Settings menu. When an imported preset already exists (by name), the user can choose to replace or merge the presets. When merging, the new preset values replace the existing values, but any existing values not in the new preset will remain.

We also added documentation links in the Flyout menu for XMP, IPTC Photo & Video, PLUS, AVM

It also improves error handling and makes messages more informative and consistent.

## Changes for 2.0.6
### Introduces the Calculation Field
[Watch a video for the 2.0.5 and 2.0.6 features](https://youtu.be/r3iqeYmCtTM)

Calc fields allow you to combine values from other fields in your view. The field will be read only for the user, but it will change based on the values of the referenced fields. The result can be either a string or a number, and the result will be stored in the XMP.

When calculating a number, it is a best practice to refer to Number fields, however if you need to use special values such as π or e, users can enter those directly.

Enter your calculated value as text. You can reference other fields in your view by using the field's XMP prefix and property name in curly braces, separated by `:`. For example, if you have a field with the XMP property name `myField`with the prefix `myPrefix` and you want to add it to another field, you would enter `{myPrefix:myField}` in the calculation field to use it in a calculation.

For example, assume you have a form that tracks pets with a custom namespace of prefix `pet`. If the user enters "dog" for the type of pet, and "dachsund" for the breed, then a calculated field with calculated value of "The {pet:petType} is a {pet:breed}." will be stored in XMP as "The dog is a dachsund."

When calculating a number, it is a best practice to refer to Number fields in your calculated value. Operations include +, -, *, /, ^, !, ln, log, and root. You can use parentheses to ensure calculation precedence. You can use the following trigonometric functions: sin, cos, tan, asin, acos, atan, sinh, cosh, tanh, asinh, acosh, atanh. Constants include e, π or pi. You can use the Combination (C) and Permutation (P) operators, such as 2P2 => 12 and 4C2 => 6. You can also use Sigma or ∑ to calculate sums. for example Sigma(1,100,n) results 5050

Users can use the constants π, pi, or e in calculations. Imaginary numbers are not supported.
![calculation](https://github.com/user-attachments/assets/ffa362ed-83f7-4283-944d-c0b2243cd4bd)

We also added a button on the Settings page to reset Custom Metadata to its default state. This will not remove presets, but it will remove any Tabs. The prior Settings file will be backed up in the Settings folder, which now can be revealed via the flyout menu. Additionally, Custom Metadata will warn you if you open the Settings panel when you have unsaved changes.

This release also updates the AVM preset to version 1.1, which includes Tags for `Subject:Category`. It also updates the PLUS preset to include URL fields and to align shared fields with IPTC.

This release also fixes the following bugs:
- Tags do not render correctly in some circumstances
- Presets may not apply to assets properly in some circumstances

## Changes for Version 2.0.5
### Introduces the Table Field and a new editing paradigm for Field Options
This release introduces a new Field: Tables. Tables display correlated properties in a tabular format, with each column representing a property and each row representing a correlated value across all properties. 

- Columns can be Text, Number or Dropdown Fields.
- Rows can be reordered by the user
- Tables can have row legends, for cases where the order of the items in each property corresponds to a specific kind of value. For instance, if item[0] represents the X coordinate of a position and item[1] represents the Y coordinate of a position, then you can have a legend for row 1 "X Coordinate" and a legend for row 2 "Y Coordinate"
- You can limit the minimum and maximum number of rows in a Table's value
- You can use Tables in Presets

We also redesigned the Options editor to remove the JSON Field and replace it with a table-based form for easier editing.

We also added IPTC and PLUS tabs to the first launch experience, and added a button to create new Tabs from the example Views. We also introduced a preset for the Astronomy Visualization Metadata Standard (AVM). We believe these will make it easier for users to get started with Custom Metadata.

## Changes for Version 2.0.4
This fixes an issue where options were not filtering properly. 

We also added the following new features:
- You can now automatically set a field value on a filtered field when the options reduce to one value
- Text fields will now automatically become multi-text when the existing value is an array

## Changes for Version 2.0.3
Bug fixes.

## Changes for Version 2.0.2
This release addresses multiple user-reported issues and adds much-requested features. We are updating the public documentation and refreshing videos, but we have updated the in-app help text. Additionally, the What's New screen contains some helpful copy and short videos. While not comprehensive, here's a list of additions, improvements, and bug fixes.
#### Field updates
- Added URL and multi-URL form fields
- Added Multi-Number form field
- Added Hidden Fields
- Added Custom Tooltips
- Added Custom Placeholder Text
- Added additional Time and Date formatting controls for Date and MultiDate fields
- You can now Sync values between fields
- Added Language Alternative support for Structures
- Improved Language Alternative configuration
- Improved Language Alternative display to include asset-defined langs
- Fixed issue which prevented update to structure contents
#### Additional Features
- You can now  Copy and Paste properties between Views when editing Views
- Added support for relative path names for Views in Settings.json
- Added click to select JSON file
- Added portability for Presets between Views
- Improved feedback when there are no Fields to display
- Moved Presets to the bottom of the Metadata View window so it's always visible
- Added clickable link to Section and SubSection headers
- Includes updated IPTC metadata starter Views (thanks, IPTC!!!)

#### Bug fixes
- Fixed field update issue when the image selection changed in Bridge
- Fixed issue which prevented Presets from working with Structures
- Added support for displaying Alt Langs with single values when the View expects an array
- Fixed a bug in Dropdowns that prevented users from selection options when using labels in the option array
- Fixed a longstanding bug in Tags which prevented the use of label-value objects
- Squashed other bugs

#### To do: 
- Update in-app help documentation for new tools and features
- Update public documentation
- Create updated quick start and feature videos

## Changes for Version 2.0.1
* Added PLUS License Data Format example View

## Changes for version 2.0.0
* Added new field types:
  * Numbers
* Changed Multiline text to automatically expand when the text is longer than 3 lines
* Added **Complex Structure** object support
  * You can now create XMP Structures, which can contain other XMP properties as well as Structures
  * The PLUS Metadata Example is a great reference for Structures
* [See the documentation for more details](https://github.com/adobe-dmeservices/custom-metadata/wiki/). 

### Fixed
* A few bugs

## Changes for version 1.7.0
* Added new field types:
  * Switches and Switch Groups
  * Radio Buttons
  * Checkboxes and Checkbox Groups
  * Multiple Date fields
  * Subdivision Divider
* Added Autocomplete for XMP Namespace and Prefix definitions
* Added **Duplicate field** button in View Editor
* [See the documentation for more details](https://github.com/adobe-dmeservices/custom-metadata/wiki/). 

### Fixed
* A few bugs

## Changes for version 1.6.0
* Added support for Premiere Pro Clip metadata within Premiere Pro. Users can read and update Clip metadata and optionally sync those values to XMP properties. [See the documentation for more details](https://github.com/adobe-dmeservices/custom-metadata/wiki/Custom-Metadata-Panel-in-Premiere-Pro). 
* Added a set of reference namespace definitions that you can access from the panel [or from our documentation](https://github.com/adobe-dmeservices/custom-metadata/wiki/Metadata-Definitions). These have been updated to include Premiere Pro specific metadata properties.

### Fixed
* A few bugs

## Changes for version 1.5.0

### Added
*[See the User Guide](https://github.com/adobe-dmeservices/custom-metadata/wiki) for more about these new features*
* Added Tabbed Interface for Metadata Forms
  * Support for independent tabs, each with its own view
* New Settings panel with separate controls for
  * Tab Manager
  * View Editor
  * Visibility of What's New screen
* What's New screen
  * Carousel with animations and text to highlight new features
* Metadata Examples for new Forms
  * Presets for popular Metadata schemas
  * Special thanks to Martin Gersbach and Greg Reser of GLAM for creating a [repository of useful config files for common metadata namespaces and properties](https://github.com/MuseosAbiertos/Adobe-Bridge-Custom-Metadata-JSON-Presets). 

## Changes for version 1.4.0

### Added
*[See the User Guide](https://github.com/adobe-dmeservices/custom-metadata/wiki) for more about these new features*
* Changed name from *Custom Metadata* from *Custom Metadata Panel*
* Added support for Language Alternative properties
  * Ability to set AltLang value type for Text Fields
  * Added Configurator Option for Alternative Language
  * Updated Default View to contain AltLang Examples
* Added a link to documentation in the Flyout menu
* Added support for self-entered values for Multiple Dropdown and Tags
* Squashed some UI bugs

### Fixed
* Inconsistent behavior when writing metadata to media files (Bridge specific)
  * This is caused by a bug in Bridge. We have implemented a workaround while the Bridge team resolves the bug. 
* Several bugs

## Changes for version 1.3.0

### Added
*[See the User Guide](https://github.com/adobe-dmeservices/custom-metadata/wiki) for more about these new features*
* Changed name to Custom Metadata Panel
* Added support for Photoshop and Illustrator
* Added multi-line text fields
* Allow special characters in Configurator
* Squashed some UI bugs

### Fixed
* Several bugs

## Changes for version 1.2.0

### Added
*[See the User Guide](https://github.com/adobe-dmeservices/custom-metadata/wiki) for more about these new features*
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
*[See the User Guide](https://github.com/adobe-dmeservices/custom-metadata/wiki) for more about these new features*
* Field Dependencies for all field types
* Filtering based on another field value in Dropdowns and Multi-Dropdowns
* Auto Group Selection in Multi-Dropdown
* Natural Language Date parsing for Date Field
* Multiple Values resolution workflow and menu for Bulk Selection Mode

### Fixed
* Several bugs
* Updated the About screen
