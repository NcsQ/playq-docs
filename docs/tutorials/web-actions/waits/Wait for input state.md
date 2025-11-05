---
sidebar_position: 2
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Overview

Waits for an input field to reach a specific state (enabled, disabled, visible, hidden). Supports both native and custom input elements with configurable timeouts.

## Syntax

```javascript
waitForInputState(
    page: Page, 
    field: string | Locator, 
    state: 'enabled' | 'disabled' | 'visible' | 'hidden',
    options?: string | Record<string, any>
)
```


## Parameters

### Required Parameters
|**Parameter** |**Type**|**Description**|
|--------------|--------|---------------|
|page | Page | Playwright Page instance |
|field  | string / Locator	 | 	Input field identifier|
|state | string | Expected state: 'enabled', 'disabled', 'visible', 'hidden'|


### Optional Parameters

```javascript
{
    actionTimeout?: number;      // Default: from config or 30000ms
    pattern?: string;           // Input field pattern
    screenshot?: boolean;       // Take screenshot after state match
    screenshotText?: string;   // Screenshot description
    screenshotFullPage?: boolean; // Full page screenshot
}
```

## Usage Examples

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
    ```javascript
    // Basic wait for input state test
    test('basic wait for input state test', async ({ page }) => {
        await web.openBrowser(page, `https://letcode.in/edit`);
        // wait for a specific element to be enabled
        await web.waitForInputState(page, example_letcode.letcode_edit_page.input_fullname(page), "enabled");
    });
    ```
  </TabItem>
  <TabItem value="Cucumber" label="Cucmber" default>

  </TabItem>
</Tabs>