# Locality Information Extractor

This repository contains a Python script that uses Selenium and ChromeDriver to scrape locality information from the MagicBricks website for a specific city (Varanasi, in this case) and saves the extracted data to an Excel file.

## Prerequisites

Before running the script, ensure you have the following installed:

- Python 3.x
- Google Chrome browser
- ChromeDriver (version must match your installed Chrome browser version)
- Required Python packages (`selenium`, `openpyxl`)

## Setup

1. **Clone the repository:**

    ```bash
    git clone https://github.com/Manish-Kumarrrr/Locality-Information-Extractor.git
    cd Locality-Information-Extractor
    ```
   or
   
   ** Download the repository as a ZIP file and extract it:**
    If you prefer, you can download the repository as a ZIP file and extract it to your local machine.
    
3. **Download ChromeDriver:**

    Download the ChromeDriver that matches your installed Chrome browser version from [ChromeDriver - WebDriver for Chrome](https://developer.chrome.com/docs/chromedriver/downloads).

    Make sure to place the `chromedriver` executable in your project directory or add it to your system's PATH.

## Usage

1. **Update the `driver_path` in the script:**

    Ensure the `driver_path` variable in the script points to the correct path of your `chromedriver` executable.

    ```python
    driver_path = r"./chromedriver"  # Replace with your actual path
    ```

2. **Run the script:**

    You can run the script using Python. Open a terminal in the project directory and execute:

    ```bash
    pip install papermill
    papermill extract_localities.ipynb executed_notebook.ipynb

    ```

    The script will open the MagicBricks website, scroll down to load locality information, and save the data to an Excel file named `localities.xlsx`.

## Script Explanation

The script performs the following steps:

1. Initializes the Chrome WebDriver with necessary options.
2. Opens the MagicBricks locality page for Varanasi.
3. Scrolls down the page to load more locality information.
4. Extracts locality names from elements with the class name `loc-card__title`.
5. Writes the extracted locality names to an Excel file using the `openpyxl` library.

## Example Output

The script will generate an Excel file `localities.xlsx` with a list of locality names extracted from the MagicBricks website.

## Troubleshooting

- Ensure that your Chrome browser version matches the ChromeDriver version.
- If you encounter issues with ChromeDriver, you may need to update your Chrome browser or ChromeDriver.
- Make sure all required Python packages are installed.


## Acknowledgements

- [Selenium](https://www.selenium.dev/)
- [OpenPyXL](https://openpyxl.readthedocs.io/en/stable/)

