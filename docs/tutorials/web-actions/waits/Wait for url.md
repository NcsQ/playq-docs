---
sidebar_position: 1
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Overview

The `waitForUrl` function waits for the page URL to match a specified pattern or exact URL. Useful for verifying navigation and page transitions.

## Syntax

```javascript
waitForUrl(page: Page, url: string, options?: string | Record<string, any>)
```


## Parameters

### Required Parameters
|**Parameter** |**Type**|**Description**|
|--------------|--------|---------------|
|page | Page | Playwright Page instance |
|url  | string | Expected URL or URL pattern|


### Optional Parameters

```javascript
{
    actionTimeout?: number;      // Default: from config or 30000ms
    match?: 'exact' | 'contains'; // URL matching strategy (Default: 'contains')
    screenshot?: boolean;        // Take screenshot after URL match
    screenshotText?: string;    // Screenshot description
    screenshotFullPage?: boolean; // Full page screenshot (Default: true)
}
```

## Usage Examples

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
    ```javascript
    // Basic wait for URL test
        test('basic wait for url test', async ({ page }) => {
            await web.openBrowser(page, url);
            await web.clickLink(page, example_letcode.letcode_home_page.link_explore_workspace(page));
            // wait for the URL to change
            await web.waitForUrl(page, `https://letcode.in/test`);
        });
    ```
  </TabItem>
  <TabItem value="Cucumber" label="Cucmber" default>

  </TabItem>
</Tabs>