# Map Management

Inside a workspace, the **Maps** tab displays a list of all maps created for that workspace. Each map entry shows the map's **name**, **description**, and **visibility** (*Public* or *Private*).

![Map List](../assets/images/workspace/map-management-list.png)

## Creating a Map

To create a new map in the workspace, click the **plus** icon at the top right of the map list and select **Map** from the options. This opens the map creation form, where you fill in the following fields:

* **Title:** The map title, in all required languages.
* **Description** *(optional)*: A description of the map.
* **Visibility:** Choose whether the map is *Public* or *Private*.

!!! note

    Public maps are shown on the front page to all users without requiring a login. For the end-user view of a map, see the [GET SDI Portal Manual](https://geospatialenablingtechnologies.github.io/get.sdi.v.6.0.0-manual/).

![Create Map Form](../assets/images/workspace/map-management-create-form.png)

## Map Actions

Each map in the list provides a set of available actions:

| Icon | Action | Description |
| :---: | :--- | :--- |
| ![Edit icon](../assets/icons/pencil.png) | **[Edit](#edit)** | Modify the map's details. |
| ![Settings icon](../assets/icons/settings.png) | **[Settings](#settings)** | Configure the map's settings. |
| ![Map events icon](../assets/icons/mouse-pointer-click.png) | **[Map Events](#map-events)** | Configure the map's events. |
| ![Excerpt print icon](../assets/icons/printer.png) | **[Excerpt Print Configuration](#excerpt-print-configuration)** | Configure the map's excerpt print output. |
| ![Preview icon](../assets/icons/eye.png) | **[Preview](#preview)** | Preview the map. |
| ![Delete icon](../assets/icons/trash-2.png) | **[Delete](#delete)** | Permanently remove the map from the workspace. |

### Edit

The **Edit** action opens the edit map form, where you can change the map's **Name** and **Description** (in all required languages) and its **Visibility** (*Public* or *Private*).

![Edit Map Form](../assets/images/workspace/map-management-edit-form.png)

### Settings

The **Settings** action opens the **Map Editor**, an extended version of the Map Viewer. Because the two share the same interface, the tools are documented in the end-user manual rather than repeated here:

* [Map Viewer overview](https://geospatialenablingtechnologies.github.io/get.sdi.v.6.0.0-manual/map/)
* [Sidebar](https://geospatialenablingtechnologies.github.io/get.sdi.v.6.0.0-manual/map/sidebar/)
* [Toolbar](https://geospatialenablingtechnologies.github.io/get.sdi.v.6.0.0-manual/map/toolbar/)
* [Attribute Table](https://geospatialenablingtechnologies.github.io/get.sdi.v.6.0.0-manual/map/attribute-table/)
* [Right Click](https://geospatialenablingtechnologies.github.io/get.sdi.v.6.0.0-manual/map/right-click/)
* [Export and Import](https://geospatialenablingtechnologies.github.io/get.sdi.v.6.0.0-manual/map/export-import/)

The key difference is a **Save** icon next to the map [export and import configuration](https://geospatialenablingtechnologies.github.io/get.sdi.v.6.0.0-manual/map/export-import/) buttons, which lets administrators save the current map configuration.

!!! note

    The saved configuration is the one every user sees when they load the map, whether from the front page or the administration page.

![Map Editor](../assets/images/workspace/map-management-settings-editor.png)
 
### Map Events

The **Map Events** action configures the [right-click map events](https://geospatialenablingtechnologies.github.io/get.sdi.v.6.0.0-manual/map/right-click/) available on the map. Clicking it opens the map events drawer, which lists all events configured for the map, each showing its **name** and the **GeoServer layer** it corresponds to.

The order of the events in this list is the order they appear in the right-click menu on the map. You can reorder them by dragging them within the list.

![Map Events Drawer](../assets/images/workspace/map-management-events-drawer.png)

#### Creating a Map Event

To create a map event, click the **Add Event** button at the top right of the list. This opens the Add Event form.

1. Enter the event's **Title** in all required languages.
2. Configure the GeoServer source using one of two tabs, **Registered** or **Custom URL**, then select a layer.
3. Choose the event's layout: **List** or **Collapse**.

##### Registered

The **Registered** tab lets you select from the available registered [GeoServers](geoserver-management.md) and then choose one of its layers.

!!! note

    For registered GeoServers, layer access is role-based — you only see the layers permitted by the GeoServer assigned to your account and your role on that GeoServer.

![Add Event Registered Tab](../assets/images/workspace/map-management-events-registered.png)

##### Custom URL

The **Custom URL** tab lets you type the URL of a GeoServer (ending in `/geoserver`) and select one of its publicly available layers.

![Add Event Custom URL Tab](../assets/images/workspace/map-management-events-custom-url.png)

##### List Layout

In the **List** layout, you organize the event's information into one or more **categories**.

For each category:

1. Enter the **category title** in all required languages.
2. Select which items to display by moving them from the left **items list** to the right **items list**. Items are the attributes of the chosen layer.

The selected items appear as a list at the bottom of the form, where you can drag them to set the order in which they appear within the category.

![Map Event List Layout](../assets/images/workspace/map-management-events-list.png)

##### Collapse Layout

In the **Collapse** layout, you group the event's information by field. Select the **field to group by**, then select the **columns** to display as items.

![Map Event Collapse Layout](../assets/images/workspace/map-management-events-collapse.png)

##### Configuring an Item

In both the **List** and **Collapse** layouts, the selected items are added, reordered, and configured the same way. Clicking an item expands its configuration form, where you can add a **Label** for the item in all required languages and choose a **display format** from the following options:

| Category | Available formats |
| :--- | :--- |
| **Currency** | Euro, Dollar, Pound, Euro (ISO code), Euro (full text), Euro (no decimals), Euro (3 decimals) |
| **Number** | Float, Float (1 decimal), Float (2 decimals), Float (3 decimals), Integer, Percentage, Percentage (1 decimal), Percentage (2 decimals), Compact short, Compact long |
| **Unit** | Square meters, Square kilometers, Hectares, Meters, Kilometers, Kilograms, Degrees Celsius |
| **Date** | Short, Long, Full |
| **Relative time** | Minutes, Hours, Days, Weeks, Months, Years |
| **Other** | Text, Text list, Link, Link list, Image, Image list, PDF, PDF list, Layer, Layer list |

![Map Event Item Configuration](../assets/images/workspace/map-management-events-item.png)

#### Map Event Actions

Each entry in the map events drawer provides the following actions:

| Icon | Action | Description |
| :---: | :--- | :--- |
| ![Edit icon](../assets/icons/pencil.png) | **[Edit](#edit-event)** | Modify the map event's configuration. |
| ![Delete icon](../assets/icons/trash-2.png) | **[Delete](#delete-event)** | Permanently remove the map event from the map. |

##### Edit Map Event

The **Edit** action reopens the event form, where you can change the event's **Title**, **GeoServer** source and layer, **layout**, and item configuration.

![Edit Map Event Form](../assets/images/workspace/map-management-events-edit-form.png)

##### Delete Map Event

Clicking the **Delete** action permanently removes the map event from the map.

### Excerpt Print Configuration

TBD

### Delete Map

Clicking the **Delete** action permanently removes the map from the workspace.