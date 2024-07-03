1. The code didn't followed Page Object Model.

2. The WebDriver session opened by FirefoxDriver is not closed properly at the end of the test case. This could lead to resource leaks:
WebDriver driver = new FirefoxDriver();
