---
sidebar_position: 4
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Overview

Verifies that a header element contains the expected text. 

## Syntax

```javascript
verifyHeaderText(
  page: Page,
  expectedText: string,
  options?: string | Record<string, any>
):
```

## Parameters

### Required Parameters
|**Parameter** |**Type**|**Description**|
|--------------|--------|---------------|
|page | Page | Playwright Page instance |
|expectedText | string |  text to wait for|
|options: string | object  |  JSON string or object with optional fields (see below) |


### Optional Parameters

```javascript
{
  actionTimeout?: number;       // ms, default: config.testExecution.actionTimeout || 10000
  navigationTimeout?: number;   // ms, default: config.testExecution.navigationTimeout || 20000
  partialMatch?: boolean;       // default: false
  ignoreCase?: boolean;         // default: false  (false => case-insensitive by implementation note)
  assert?: boolean;             // throw on failure if true, default: true
  locator?: string;             // override locator (CSS/XPath)
  headerType?: string;          // "h1" | "h2" ... limit search to specific header tag
  screenshot?: boolean;         // default: true
  screenshotText?: string;      // description for screenshot
  screenshotFullPage?: boolean; // default: true
}
```

## Usage Examples

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
    ```javascript
    // Basic header verification test
    test('basic header verification test', async ({ page }) => {
        await web.openBrowser(page, `https://letcode.in/edit`);
        // verify the header text
        await web.verifyHeaderText(page, "Input");
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
    // Header verification with custom action timeout test
    test('header verification with custom action timeout test', async ({ page }) => {
        await web.openBrowser(page, `https://letcode.in/edit`);
        // verify the header text with custom action timeout
        await web.verifyHeaderText(page, "Input", {
            actionTimeout: 90000
        });
    });

    // Header verification with custom navigation timeout test
    test('header verification with custom navigation timeout test', async ({ page }) => {
        await web.openBrowser(page, `https://letcode.in/edit`);
        // verify the header text with custom navigation timeout
        await web.verifyHeaderText(page, "Input", {
            navigationTimeout: 90000
        });
    });

    // Header verification with partial match test
    test('header verification with partial match test', async ({ page }) => {
        await web.openBrowser(page, `https://letcode.in/edit`);
        // verify the header text with partial match
        await web.verifyHeaderText(page, "In", {
            partialMatch: true
        });
    });

    // Header verification with overriden pattern test
    test('header verification with overriden pattern test', async ({ page }) => {
        await web.openBrowser(page, `https://letcode.in/edit`);
        // verify the header text with overriden pattern
        await web.verifyHeaderText(page, "Input", {
            pattern: "//section/div/h1"
        });
    });

    // Header verification with ignore case test
    test('header verification with ignore case test', async ({ page }) => {
        await web.openBrowser(page, `https://letcode.in/edit`);
        // verify the header text with ignore case
        await web.verifyHeaderText(page, "InPut", {
            ignoreCase: true
        });
    });

    // Header verification with assert false test
    test('header verification assert false test', async ({ page }) => {
        await web.openBrowser(page, `https://letcode.in/edit`);
        // verify the header text with assert false
        await web.verifyHeaderText(page, "Hello", {
            assert: false
        });
    });


    // Header verification with assert false test
    test('header verification with assert false test', async ({ page }) => {
        await web.openBrowser(page, `https://letcode.in/edit`);
        // verify the header text with assert false
        await web.verifyHeaderText(page, "Hello", {
            assert: false
        });
    });


    // Header verification with specifying the locator test
    test('header verification with specifying the locator test', async ({ page }) => {
        await web.openBrowser(page, `https://letcode.in/edit`);
        // verify the header text with specifying the locator
        await web.verifyHeaderText(page, "Input", {
            locator: "//section/div/h1"
        });
    });


    // Header verification with header type test
    test('header verification with header type test', async ({ page }) => {
        await web.openBrowser(page, `https://letcode.in/edit`);
        // verify the header text with header type
        await web.verifyHeaderText(page, "Input", {
            headerType: "h1"
        });
    });

    // Header verification with screenshot full page test
    test('header verification with screenshot full page test', async ({ page }) => {
        await web.openBrowser(page, `https://letcode.in/edit`);
        // verify the header text with screenshot full page
        await web.verifyHeaderText(page, "Input", {
            screenshotFullPage: true
        });
    });

    ```
  </TabItem>
  <TabItem value="Cucumber" label="Cucmber" default>

  </TabItem>
</Tabs>