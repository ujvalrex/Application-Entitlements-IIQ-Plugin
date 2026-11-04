# Application Entitlements

### Plugin Name: - Application Entitlements Plugin

### Plugin Version: - 1.0.0

### Supported version: - IdentityIQ 8.0 or above

### Supported browsers: - Any Chromium or Firefox browser (Internet Explorer not supported)

### Primary function: - Adds an **Entitlements** tab to the Application Configuration page so administrators can browse, search, filter, and open the entitlements of an application without leaving the page.

![Entitlements tab](docs/images/entitlements-tab.png)

## New In Version 1.0

1. Added an **Entitlements** tab on the Application Configuration page, placed right after the **Accounts** tab.
2. Added server-side pagination with First / Previous / Next / Last buttons, an editable page number, and a selectable page size (5, 10, 20, 25, 50, 75, 100 - default 25).
3. Added search (button, Enter key, and a clear **×** button) that runs on the server and resets to page 1.
4. Added an **Attribute Type** dropdown that is populated dynamically from the entitlement types that exist for the selected application (for example `memberOf` for Active Directory, or `roles` / `groups` for custom applications).
5. Added click-to-sort column headers (ID, Attribute, Display Name, Value).
6. Added a **Refresh** button and an in-table loading indicator.
7. Added click-through navigation: the **ID** links to the entitlement's edit page in a new tab, and clicking anywhere else on a row opens the standard IdentityIQ entitlement details view.
8. Added icon-based **Requestable** column (green check / red cross).

## Features

- **Entitlements tab** - Injected into the existing Application Configuration tab panel, next to **Accounts**. No other tab is modified or resized.
- **Columns** - ID, Attribute, Display Name, Value, Owner, Requestable.
- **Pagination** - Server-side. Only the requested page is fetched from IdentityIQ. Shows "Displaying X of Y".
- **Page size** - Dropdown with 5, 10, 20, 25, 50, 75, 100 items per page.
- **Search** - Matches entitlements for the current application. Supports the search button, the Enter key, and a clear button.
- **Attribute Type filter** - Dropdown listing the entitlement attribute types found for the application. Leave blank to show all types.
- **Sorting** - Click a sortable column header to toggle ascending / descending.
- **Row navigation** - Clicking a row opens the native IdentityIQ entitlement details. The ID column keeps its own hyperlink.
- **Refresh** - Reloads the current page with the current search, filter, and page size.

## Installation

- Sign in to IdentityIQ as a user with access to the Plugins page.
- Go to the **Gear icon > Plugins** and upload the plugin ZIP (**New** button, or drag and drop the file).
- Wait for the plugin to show as installed / enabled.

![Plugin installation](docs/images/installation.png)

## Configuration

- No additional configuration is required after installation.

## Verification

1. Open **Applications > Application Definition** and open any application that has entitlements in the Entitlement Catalog.
2. Confirm that an **Entitlements** tab appears right after the **Accounts** tab.
3. Open the tab and confirm that the entitlements load, the page count and "Displaying X of Y" text are correct, and the Attribute Type dropdown lists the application's entitlement types.

![Entitlements tab verification](docs/images/verification.png)

## Usage

- **Search** - type a value and press Enter or click the magnifier. Click **×** to clear the search and return to the full list.
- **Attribute Type** - choose a type to show only that kind of entitlement. Select the blank option to remove the filter.
- **Paging** - use the arrow buttons, or type a page number in the page box and press Enter to jump directly to that page.
- **Show ... items** - change how many entitlements are displayed per page.
- **Refresh** - reload the data without losing the current page, search, or filter.
- **ID link** - opens the entitlement's edit page in a new browser tab.
- **Row click** - opens the standard IdentityIQ entitlement details for that entitlement.

## Feedback

- For bugs, feature enhancement requests, issues, or questions please contact me on [LinkedIn](https://www.linkedin.com/in/infantrex) or rexajith55@gmail.com
