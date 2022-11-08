# InstagramBot

```Python
from selenium import webdriver
from selenium import webdriver
from webdriver_manager.chrome import ChromeDriverManager
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from selenium.webdriver.common.by import By
import undetected_chromedriver as webdriver
import csv


def login():
    chrome_options = webdriver.ChromeOptions()

    prefs = {"profile.default_content_setting_values.notifications": 2}

    chrome_options.add_experimental_option("prefs", prefs)

    browser = webdriver.Chrome(chrome_options=chrome_options)

    browser.implicitly_wait(5)

    browser.get('https://www.instagram.com/')

    with open("cookies.txt", "r", encoding="utf8") as cookie_file:
        tsv_reader = csv.reader(cookie_file, delimiter="\t")

    # Skip the first row, which is the header
        next(tsv_reader)

        for row in tsv_reader:
            (Domain, Include_subdomains, Path, Secure, Expiry, Name, Value) = row
            browser.add_cookie(
                {"name": Name, "value": Value, "path": Path, "domain": Domain})

    browser.get('https://www.instagram.com/')

    wait = WebDriverWait(browser, 10)

    notifications = wait.until(
        EC.element_to_be_clickable((By.CLASS_NAME, "_a9_1")))
    notifications.click()
    return browser


def savePosts(session, number_of_likes):

    print(number_of_likes)
    postsToSave = session.find_elements(By.CLASS_NAME, "_aamz")
    i = 0
    for postToSave in postsToSave:
        if i < 4:
            postToSave.click()
            i += 1
        else:
            return 0
        print(i)


session = login()
number_of_likes = int(input("Number of post to save: "))

savePosts(session, number_of_likes)
```