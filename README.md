
![Python Version](https://img.shields.io/badge/python-3.11-blue.svg)
![Flask Version](https://img.shields.io/badge/Flask-3.0.0-blue.svg)
![Pandas Version](https://img.shields.io/badge/pandas-2.1.4-blue.svg)
![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

# Dictionary API Flask Application

## Introduction

This Flask application provides a simple API to retrieve word definitions from a CSV file. It features two primary routes: a home route that serves an HTML page and an API route to fetch definitions of specific words.

## Installation

To run this application, you will need Python and Flask installed on your system. 

### Requirements
- Python 3.x
- Flask
- Pandas

### Steps
1. Clone the repository or download the source code.
2. Install the required dependencies:
   ```bash
   pip install Flask pandas
   ```
3. Place your dictionary CSV file named `dictionary.csv` in the same directory as the app. The CSV file should have at least two columns: `word` and `definition`.

## Usage

### Starting the Application
Run the application by executing:
```bash
python <app_file_name>.py
```
Replace `<app_file_name>` with the name of your Python script.

### Accessing the Application
- Open a web browser and navigate to `http://localhost:5001/` to view the home page.
- To retrieve the definition of a word, use the API endpoint: `http://localhost:5001/api/v1/<word>`. Replace `<word>` with the word you want to search for.

## API Reference

### Endpoints
- `/` : The home route that serves the `home.html` page.
- `/api/v1/<word>` : A GET request to this endpoint returns the definition of the specified word in JSON format.

### Response Format
The response for the API call is a JSON object containing the word and its definition:
```json
{
  "word": "example",
  "definition": "This is a sample definition."
}
```

## Additional Notes

- Ensure the CSV file is correctly formatted and placed in the application's directory.
- The application runs in debug mode on port 5001. Adjust configurations as needed for production use.
