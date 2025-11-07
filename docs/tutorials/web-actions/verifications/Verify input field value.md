---
sidebar_position: 4
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Overview

Verifies that an input field contains the expected value. Supports exact/partial matching, case sensitivity, and custom timeouts.

## Syntax

```javascript
verifyInputFieldValue(
    page: Page,
    field: string | Locator,
    expectedValue: string,
    options?: string | Record<string, any>
)
```

## Parameters

### Required Parameters
|**Parameter** |**Type**|**Description**|
|--------------|--------|---------------|
|page | Page | Playwright Page instance |
|field | string / Locator | Input field identifier (label, id, selector)|
|expectedValue | string | Expected value text |


### Optional Parameters

```javascript
{
  actionTimeout?: number;      // Default: from config or 30000ms
    pattern?: string;           // Custom pattern for element search
    partialMatch?: boolean;     // Allow partial value match (Default: false)
    ignoreCase?: boolean;       // Case-insensitive comparison (Default: false)
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
      // Basic input field value verification test
      test('basic input field value verification test', async ({ page }) => {
          await web.openBrowser(page, `https://letcode.in/edit`);
          // verify the input field value
          await web.verifyInputFieldValue(page, "id=dontwrite","This text is readonly");
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
      // Input field value verification with custom timeout test
      test('input field value verification with custom timeout test', async ({ page }) => {
          await web.openBrowser(page, `https://letcode.in/edit`);
          // verify the input field value with custom timeout
          await web.verifyInputFieldValue(page, "id=dontwrite","This text is readonly",{
              actionTimeout: 120000
          });
      });

      // Input field value verification with partial match test
      test('input field value verification with partial match test', async ({ page }) => {
          await web.openBrowser(page, `https://letcode.in/edit`);
          // verify the input field value with partial match
          await web.verifyInputFieldValue(page, "id=dontwrite","This text",{
              partialMatch: true
          });
      });

      // Input field value verification with ignore case test
      test('input field value verification with ignore case test', async ({ page }) => {
          await web.openBrowser(page, `https://letcode.in/edit`);
          // verify the input field value with ignore case
          await web.verifyInputFieldValue(page, "id=dontwrite","This text is Readonly",{
              ignoreCase: true
          });
      });

      // Input field value verification with assert false test
      test('input field value verification with assert false test', async ({ page }) => {
          await web.openBrowser(page, `https://letcode.in/edit`);
          // verify the input field value with assert false
          await web.verifyInputFieldValue(page, "id=dontwrite","This text is Readonly",{
              assert: false
        });
      });
    ```
  </TabItem>
  <TabItem value="Cucumber" label="Cucmber" default>

  </TabItem>
</Tabs>