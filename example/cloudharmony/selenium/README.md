# Uplink Stats

# Dependencies
We used Selenium version 3.5.0, it can be installed with `pip`.

We coded in Python.

Our platform is Microsoft Windows 10 Enterprise (Version 10.0.17134 N/A Build 17134).

We used [chromedriver.exe (version - 73+)](https://chromedriver.storage.googleapis.com/index.html?path=73.0.3683.20/).
Don't forget to add folder paths to the Windows path variable, if you don't want to specify path to executable every time.

[chromedriver_test.py](chromedriver_test.py) can be run to test if all the dependancies are installed.

# Script
See [cloudharmony.py](cloudharmony.py)

The webpage fails if too many service are tested all at once, so tests are carried out one by one.

Example results: [uplink.json](uplink.json)