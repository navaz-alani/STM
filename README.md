# Selenium Testing Module

This module contains a set of functions which automate browser initiation and prettify logging for Selenium.

## Motivation

When using Selenium WebDriver to automate E2E testing, one needs a driver which Selenium can use to control the browser. In the case of Google Chrome, its the `chromedriver`.

Getting the driver and setting it up is usually manual and is somewhat error prone.

## What this module offers

This module offers the `browser_init` function which can be used as follows:

`browser_init : browser_name: str, ops=[], exp_ops=[], headless_download=False) -> WebDriver`

Arguments:

`broswer_init` takes the following arguments:

- REQUIRED: `browser_name: str` - one of `"firefox", "chrome", "edge","gecko", "opera_chromium", "opera"`
- `ops: list = []` - options such as `"headless", "verbose"`
- `exp_ops: list = []` - experimental options
- `headless_download: bool = False` - This is a feature which is aimed at working around the chromium sercurity feature prohibiting downloads in headless mode. Set `True` to download in `headless` mode.

and returns a `WebDriver` object.

Also offered is the `p_print` function which can be used to prettify command line output so that tests can be understood by the greater team.

`p_print` takes in the following arguments:

- REQUIRED: `s: any` - object to print
- `n: int = 0` - This is the parameter specifying the indent level of the output
- `toc: str = None` - Token which can be used to color the output. Use token `'info'` for yellow, `'s'` for green (success) and `'f'` for red (failure).

returns `None` and outputs to `stdout`.

Finally, `user_exit` is a debug function that can be used to prevent the driver from closing when the test script execution complete. It prompts the user to close the session. It should be executed as the last command in the script.

`user_exit` takes in 1 argument:

REQUIRED: `driver: WebDriver` - a WebDriver object

returns `None` and prompts the user to exit test manually.
