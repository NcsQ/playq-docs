---
sidebar_position: 2
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Overview

The `selectDropdown` function selects an option from either a native `<select>` element or a custom dropdown component.

## Syntax

```javascript
selectDropdown(
    page: Page, 
    field: string | Locator, 
    value: string | number | (string | number)[], 
    options?: string | Record<string, any>
)
```

## Parameters

### Required Parameters
|**Parameter** |**Type**|**Description**|
|--------------|--------|---------------|
| page | Page | Playwright page instance |
| Field | string / Locator | Dropdown identifier (label, id, selector) |
| value | string / number / Array | Option to select |

### Optional Parameters

```javascript
{
    actionTimeout?: number;      // Default: from config or 30000ms
    pattern?: string;           // Custom pattern for element search
    screenshot?: boolean;       // Take screenshot after selection
    screenshotText?: string;   // Screenshot description
    screenshotFullPage?: boolean; // Full page screenshot
}
```

## Usage Examples

### Basic Usage

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
    ```javascript
    // Simple drop down select test
        test('select dropdown test', async ({ page }) => {
            await web.openBrowser(page, "https://letcode.in/dropdowns");
            // Simple select - select a fruit
            await web.selectDropdown(page, locLetcode.letcode_dropdowns_page.select_fruit(page), "Apple");

        });
    ```
  </TabItem>
  <TabItem value="Cucumber" label="Cucmber" default>

  </TabItem>
</Tabs>