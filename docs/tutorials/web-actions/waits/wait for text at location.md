---
sidebar_position: 4
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Overview

Wait until a specified element contains the expected text. Returns when the text appears or throws on timeout.


## Syntax

```javascript
waitForTextAtLocation(
  page: Page,
  field: string | Locator,
  expectedText: string,
  options?: string | Record<string, any>
)
```

## Parameters

### Required Parameters
|**Parameter** |**Type**|**Description**|
|--------------|--------|---------------|
|page | Page | Playwright Page instance |
|header  | string / Locator	 |  locator descriptor (label, id, selector, xpath) or a Playwright Locator |
|expectedText | string |  text to wait for|
| options: string | object  |  JSON string or object with optional fields (see below) |


### Optional Parameters

```javascript
{
    actionTimeout?: number,      // default: config.testExecution.actionTimeout || 10000
    partialMatch?: boolean,      // default: false
    ignoreCase?: boolean,        // default: true
    screenshot?: boolean,        // default: false
    screenshotText?: string,     // default: ""
    screenshotFullPage?: boolean,// default: true
    pattern?: string             // optional pattern key for webLocResolver
}
```

## Usage Examples

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
    ```javascript
    // Basic wait for text at a location test
    test('basic wait for text at a location test', async ({ page }) => {
        await web.openBrowser(page, `https://letcode.in/elements`);
        // wait for the text to be visible at the specified location
        await web.waitForTextAtLocation(page, "//button[@type='submit']", "Search");
    });
    ```
  </TabItem>
  <TabItem value="Cucumber" label="Cucmber" default>

  </TabItem>
</Tabs>