---
sidebar_position: 1
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';


## Overview

The `fill` function fills form input fields with text values. It supports both Playwright and Cucumber test runners, with comprehensive options for screenshots and error handling.

## Syntax

```javascript
fill(page: Page, field: string | Locator, value: string | number, options?: string | Record<string, any>)
```

## Parameters

### Required Parameters
|**Parameter** |**Type**|**Description**|
|--------------|--------|---------------|
| page | Page | Playwright page instance |
| Field | string / Locator | Input field identifier (label, placeholder, selector) |
| value | string / number	 | Value to fill in the field |

### Optional Parameters

```javascript
{
    actionTimeout?: number;      // Default: from config or 30000ms
    pattern?: string;           // Custom pattern for element search
    screenshot?: boolean;       // Take screenshot after filling
    screenshotText?: string;   // Screenshot description
    screenshotField?: boolean; // Screenshot just the field
    screenshotFullPage?: boolean; // Full page screenshot
    iframe?: string;           // iframe selector if input is in frame
}
```
### Aliases
 - `type`
 - `input`
 - `set`
 - `enter`

## Usage Examples

### Basic Usage

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
  ```javascript
   // Simple fill test
    test('input field fill test', async ({ page }) => {
        await web.openBrowser(page, url);
        // Simple fill - fill in the fullname field
        await web.fill(page, locLetcode.letcode_edit_page.input_fullname(page), "John Doe");
    });
    ```
  </TabItem>
  <TabItem value="Cucumber" label="Cucmber" default>

  </TabItem>
</Tabs>

### Using aliases


<Tabs>
  <TabItem value="playwright" label="Playwright" default>
 ```javascript
        // type -  fill a field using aliases
        test('type to a field test', async ({ page }) => {
            await web.openBrowser(page, url);
            // Simple fill - type in the fullname field
            await web.type(page, locLetcode.letcode_edit_page.input_fullname(page), "John Doe");
        });

        // input -  fill a field using aliases
        test('input to a field test', async ({ page }) => {
            await web.openBrowser(page, url);
            // Simple fill - fill in the fullname field
            await web.input(page, locLetcode.letcode_edit_page.input_fullname(page), "John Doe");
        });

        // set -  fill a field using aliases
        test('set to a field test', async ({ page }) => {
            await web.openBrowser(page, url);
            // Simple fill - fill in the fullname field
            await web.set(page, locLetcode.letcode_edit_page.input_fullname(page), "John Doe");
        });

        // enter -  fill a field using aliases
        test('enter to a field test', async ({ page }) => {
            await web.openBrowser(page, url);
            // Simple fill - fill in the fullname field
            await web.enter(page, locLetcode.letcode_edit_page.input_fullname(page), "John Doe");
        });
```
  </TabItem>
  <TabItem value="Cucumber" label="Cucmber" default>
   
  </TabItem>
</Tabs>