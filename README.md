## API Python

This project aims to provide endpoints for the extraction of basic data from an Excel file (.xlsx) and, also, a simple image
conversion route.

## Requirements
- Python 3.7.2
- Flask 1.1.2 

## Extra Libraries
- Cross Origin Resource Sharing (CORS)
>> pip install -U flask-cors
- pyjwt
>> pip install pyjwt
- openpyxl
>> pip install openpyxl
- Pyllow
>> pip install --upgrade Pillow

## Installation
- Install the requirements
- Install and create a virtualenv
>> pip install virtualenv
- Install the extra libraries
- clone the reposotory
>> git clone https://github.com/JailsonS/api_sheetgo

## Structure of Project
-> <b>controllers</b> [ it contains the controllers with the routes to perform conversion ] <br>
-------> <b>excelcontroller.py</b> [ it contains the route and methods to read an excel file ] <br>
-------> <b>imagecontroller.py</b> [ it contains the route and methods to read and convert an image file ] <br>
-> <b>models</b> <br>
-------> <b>auth.py</b> [ it contains information and methods to authenticate data ] <br>
-> <b>sample</b> <br>
-------> <b>sample.xlsx</b> [ it contains a simple xlsx file with some information. It can be used to test the routes ]

## Testing the API
A very simple way to test the API is using the website https://resttesttest.com/. The endpoints that will be tested are:
- [YOUR_BASE_DIR]/excel/info
- [YOUR_BASE_DIR]/image/convert
### Run the project
- Activate the virtualenv and go to the project's directory
- run the code below:
>> flask run
### Testing [YOUR_BASE_DIR]/excel/info route
#### Input data
- email credentials, the parameter name must be "email"
- .xlsx file (there is a sample file in sample folder), the parameter name must be "sample_file"
#### Output data
- json with some info: res_tab (tabs of the file ordered alphabetically), res (value of the first tab), jwt_token (JWT token encoded)