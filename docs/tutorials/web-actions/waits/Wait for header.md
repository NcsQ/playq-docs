---
sidebar_position: 3
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Overview

Waits for a header element to contain specific text. Supports both exact and partial text matching with configurable timeouts.

## Syntax

```javascript
waitForHeader(
    page: Page, 
    header: string | Locator, 
    headerText: string,
    options?: string | Record<string, any>
)
```


## Parameters

### Required Parameters
|**Parameter** |**Type**|**Description**|
|--------------|--------|---------------|
|page | Page | Playwright Page instance |
|header  | string / Locator	 | Header element identifier |
|headerText | string | Expected text in header|


### Optional Parameters

```javascript
{
    actionTimeout?: number;      // Default: from config or 30000ms
    pattern?: string;           // Header element pattern
    partialMatch?: boolean;     // Allow partial text match
    ignoreCase?: boolean;       // Case-insensitive matching
    screenshot?: boolean;       // Take screenshot after match
    screenshotText?: string;    // Screenshot description
    screenshotFullPage?: boolean; // Full page screenshot
}
```

## Usage Examples

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
    ```javascript
    // Basic wait for header test
    test('basic wait for header test', async ({ page }) => {
        await web.openBrowser(page, `https://letcode.in/edit`);
        // wait for the header to be visible
        await web.waitForHeader(page, ".section .container .title", "Input");
    });
    ```
  </TabItem>
  <TabItem value="Cucumber" label="Cucmber" default>

  </TabItem>
</Tabs>