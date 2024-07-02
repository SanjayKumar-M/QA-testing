# QA-testing-for-Python

Name: Sanjay Kumar M
Role: SDET Intern

Bugs found:

1. Absolute paths can lead to test failures if the UI structure changes. Use relative paths for better stability.
 # Line 22
driver.find_element(By.XPATH, "/html/body/div[3]/div/section/section/div/header/button").click()
# Line 60
driver.find_element(By.XPATH, "/html[1]/body[1]/div[3]/div[1]/section[1]/section[1]/div[1]/div[1]/section[1]/div[1]/div[1]/div[2]/div[1]/div[2]/div[1]/table[1]/tbody[1]/tr[9]/td[2]").click()
# Line 67
driver.find_element(By.XPATH, "/html[1]/body[1]/div[3]/div[1]/header[1]/div[2]/nav[1]/div[7]/div[1]/div[1]").click()

2. Static waits are not efficient. Use dynamic waits like WebDriverWait to handle conditions properly.

4. Initializing the driver as Chrome() limits the tests to Chrome. Use the WebDriver interface for flexibility.   # Line 77
driver = webdriver.Chrome()

5. Raising a general Exception is not informative. Use assertions to validate conditions.
# Line 105
raise Exception("Not on the home page")


