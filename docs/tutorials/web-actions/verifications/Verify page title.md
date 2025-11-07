---
sidebar_position: 4
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Overview

Verifies the page title matches the expected text with support for partial matching, case sensitivity, and screenshot capture options.


## Syntax

```javascript
verifyPageTitle(
    page: Page, 
    expectedTitle: string,
    options?: string | Record<string, any>
)
```

## Parameters

### Required Parameters
|**Parameter** |**Type**|**Description**|
|--------------|--------|---------------|
|page | Page | Playwright Page instance |
|expectedTitle | string | Expected page title to verify|


### Optional Parameters

```javascript
{
    partialMatch?: boolean;       // Allow partial title match (Default: false)
    ignoreCase?: boolean;        // Case-sensitive matching (Default: false)
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
    // Basic verify page title test
      test('basic verify page title test', async ({ page }) => {
          await web.openBrowser(page, `http://the-internet.herokuapp.com/`);
          // verify the page title
          await web.verifyPageTitle(page, "The Internet");
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
   // verify page title with partial match test
    test('verify page title with partial match test', async ({ page }) => {
        await web.openBrowser(page, `${url}`);
        // verify page title with partial match
        await web.verifyPageTitle(page, "The",{
            partialMatch: true
        });
    });
    ```
  </TabItem>
  <TabItem value="Cucumber" label="Cucmber" default>

  </TabItem>
</Tabs>