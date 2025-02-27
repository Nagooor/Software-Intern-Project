Spreadsheet Backend Project
This project is a Django-based backend for managing spreadsheet-like data. It provides APIs to store, retrieve, and manipulate cell data, along with utility functions for calculations and data quality operations.

Table of Contents
1.Project Overview
2.Features
3.Installation
4.API Endpoints
5.Utility Functions
6.Admin Interface
7.Contributing
8.License

Project Overview
This project is designed to simulate a spreadsheet backend, where each cell is stored in a database with its unique ID, value, and optional formula. The backend provides RESTful APIs to interact with the data and includes utility functions for common spreadsheet operations like calculations and data cleaning.

Features
Cell Management: Store and retrieve cell data (ID, value, formula).
Calculations: Perform calculations like sum, average, max, min, and count on a range of cells.
Data Quality: Functions to trim, convert case, remove duplicates, and find/replace cell values.
RESTful API: Exposes endpoints for CRUD operations on cells.
Admin Interface: Manage cells via Django's built-in admin panel.

Installation
Follow these steps to set up the project locally:

1.Clone the Repository:
git clone https://github.com/Nagooor/Software-Intern-Project/tree/main
cd spreadsheet-backend

2.Set Up a Virtual Environment:
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

3.Install Dependencies:
pip install -r requirements.txt

4.Run Migrations:
python manage.py migrate

5.Create a Superuser (Optional):
python manage.py createsuperuser

6.Run the Development Server:
python manage.py runserver

7.Access the API:
Open your browser and go to http://127.0.0.1:8000/api

API Endpoints
The following endpoints are available:

Cells
1.List All Cells: GET /api/cells/
2.Create a New Cell: POST /api/cells/
3.Retrieve a Specific Cell: GET /api/cells/<cell_id>/
4.Update a Cell: PUT /api/cells/<cell_id>/
5.Delete a Cell: DELETE /api/cells/<cell_id>/

Utility Functions
The utils.py file contains helper functions for calculations and data quality:

Calculation Functions
calculate_sum(cell_range): Calculate the sum of numeric values in a range of cells.
calculate_average(cell_range): Calculate the average of numeric values in a range of cells.
calculate_max(cell_range): Find the maximum value in a range of cells.
calculate_min(cell_range): Find the minimum value in a range of cells.
calculate_count(cell_range): Count the number of numeric values in a range of cells.

Data Quality Functions
trim_cell_value(cell_id): Trim whitespace from a cell's value.
upper_cell_value(cell_id): Convert a cell's value to uppercase.
lower_cell_value(cell_id): Convert a cell's value to lowercase.
remove_duplicates(cell_range): Remove duplicate values in a range of cells.
find_and_replace(cell_range, find_text, replace_text): Find and replace text in a range of cells.

Admin Interface
The Django admin interface allows you to manage cells directly. To access it:
Go to http://127.0.0.1:8000/admin/.
Log in with your superuser credentials.
Manage Spreadsheet entries under the API section.

Contributing
Contributions are welcome! Follow these steps to contribute:
1.Fork the repository.
2.Create a new branch for your feature or bugfix.
3.Commit your changes and push to the branch.
4.Submit a pull request.




