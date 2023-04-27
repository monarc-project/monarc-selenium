# Monarc Test Suite

This is a test suite for the login functionality of the Monarc web application. The test suite is implemented using Selenium in Python, and uses the unittest framework to define and run test cases.

## Requirements

- Python 3.x
- Selenium WebDriver
- ChromeDriver
- chromedriver-binary package
- unittest

## Installation

1. Clone this repository to your local machine.
2. Install Python 3.x if you don't have it installed already.
3. Install the Selenium WebDriver for Chrome. You can download it from the [official website](https://sites.google.com/a/chromium.org/chromedriver/downloads) or install it using a package manager like `apt-get` or `brew`.
4. Install the `chromedriver-binary` package using `pip`: `pip install chromedriver-binary`.
5. Install the `unittest` package using `pip`: `pip install unittest`.

## Configuration

Before running the test suite, you need to configure the test environment by setting some variables in the `config.py` file. In particular, you need to set the path to the ChromeDriver executable and the base URL for the MyMonarc web application. You also need to set the login credentials for valid and invalid logins.

```python
class Config:
    """Config class to store configuration variables"""

    # Selenium configuration
    BASE_URL = "https://127.0.0.1:5000/"

    # Login configuration
    VALID_USERNAME = "valid_username"
    VALID_PASSWORD = "valid_password"
    INVALID_USERNAME = "invalid_username"
    INVALID_PASSWORD = "invalid_password"
```

## Usage

To run the test suite, simply execute the `run_tests.py` script:

```
python run_tests.py
```

This will run all the test cases defined in the `TestLogin` module and print the results to the console.

## Test Suite Structure

The test suite is organized as follows:

- `config.py`: Configuration variables for the test suite.
- `run_tests.py`: Script to run the test suite.
- `pages/`: Directory containing page object classes for the different pages of the MyMonarc web application.
- `tests/`: Directory containing the test case classes for the MyMonarc web application.
- `tests/test_login.py`: Test case class for the login functionality of the MyMonarc web application.
- `tests/__init__.py`: Empty file that tells Python that the `tests` directory should be treated as a package.

## License

This software is licensed under
[GNU Affero General Public License version 3](http://www.gnu.org/licenses/agpl-3.0.html)