---
sidebar_position: 2
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem'

## Overview

Simulates keyboard key presses on a webpage using Playwright's keyboard API.

 ## Syntax

 ```javascript
 pressKey(page: Page, key: string, options?: string | Record<string, any>)
 ```
## Parameters

### Required Parameters
|**Parameter** |**Type**|**Description**|
|--------------|--------|---------------|
| page | Page | Playwright page instance |
| Key | string | Key to press (e.g., "Enter", "Tab", "ArrowDown") |

### Optional Parameters

```javascript
{
    screenshot?: boolean;        // Take screenshot after key press (Default: false)
    screenshotText?: string;    // Screenshot description
    screenshotFullPage?: boolean; // Full page screenshot (Default: true)
}
```

## Common Key Values
- Navigation: "Enter", "Tab", "Escape"
- Arrows: "ArrowUp", "ArrowDown", "ArrowLeft", "ArrowRight"
- Function: "F1" through "F12"
- Modifiers: "Control", "Alt", "Shift"
- Special: "Backspace", "Delete", "Home", "End"

## Usage Examples

<Tabs>
  <TabItem value="playwright" label="Playwright" default>
    ```javascript
   // Simple  press key test
    test('press key test', async ({ page }) => {
        await web.openBrowser(page, "http://the-internet.herokuapp.com/key_presses");
        // Press the Enter key
        await web.pressKey(page, "Enter");
        // Verify the key press
        await web.verifyTextOnPage(page, "You entered: ENTER");
    });

    ```
  </TabItem>
  <TabItem value="Cucumber" label="Cucmber" default>

  </TabItem>
</Tabs>