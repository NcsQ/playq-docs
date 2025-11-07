---
sidebar_position: 4
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Overview

Verifies that an input field is present and visible on the page. Supports both Playwright and Cucumber test runners.

## Syntax

```javascript
verifyInputFieldPresent(
    page: Page, 
    field: string | Locator,
    options?: string | Record<string, any>
)
```

## Parameters

### Required Parameters
|**Parameter** |**Type**|**Description**|
|--------------|--------|---------------|
|page | Page | Playwright Page instance |
|field | string / Locator | Input field identifier (label, id, selector)|


### Optional Parameters

```javascript
{
    actionTimeout?: number;      // Default: from config or 30000ms
    pattern?: string;           // Custom pattern for element search
    assert?: boolean;           // Throw on failure (Default: true)
    screenshot?: boolean;       // Take screenshot (Default: true)
    screenshotText?: string;    // Screenshot description
    screenshotFullPage?: boolean; // Full page screenshot (Default: true)
}
```

## Usage Examples

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
    ```javascript
        // Basic input field verification test
        test('basic input field verification test', async ({ page }) => {
            await web.openBrowser(page, `https://letcode.in/edit`);
            // verify the input field presence
            await web.verifyInputFieldPresent(page, "id=fullName");
        });
    ```
  </TabItem>
  <TabItem value="Cucumber" label="Cucmber" default>

  </TabItem>
</Tabs>

### With options

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
   ```javascript
   // Input field verification without assertion test
    test('input field verification without assertion test', async ({ page }) => {
        await web.openBrowser(page, `https://letcode.in/edit`);
        // verify the input field presence without assertion
        await web.verifyInputFieldPresent(page, "id=fullName",{
            assert: false
        });
    });
    ```
  </TabItem>
  <TabItem value="Cucumber" label="Cucmber" default>

  </TabItem>
</Tabs>