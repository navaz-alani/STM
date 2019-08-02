This is the initial release of Selenium Testing Module which features a set of functions that may prove useful to improve testing experience.

This release features `browser_init()`; a powerful function that automates the procedure of instantiating a WebDriver object for testing. At the moment, this function only fully works with Chromium based browsers. For other browsers, `browser_init()` will only be able to simply instantiate the WebDriver. For chromium based browsers, within one function call, the user is able to accomplish the following:

- Download and save the chromedriver executable (specific to your operating system)
- Supply the testing options (e.g. `headless` or `verbose`)
- Supply experimental options to add to the WebDriver configuration
- Instantiate the WebDriver object

Along with `browser_init`, comes the `p_print()` function which can be used to prettify command line output by specifying a token and an output indent level.

This module aims to make testing scripts easier to write (and understand) as well as make test results easier to understand to the end user.
