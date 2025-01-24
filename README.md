# Student Data Management

## Overview

The Student Data Management project is a comprehensive application designed to manage student information, attendance,
grades, and more. It provides a user-friendly interface for data entry and visualization, making it easy to handle
student records efficiently.

This project is a Student Management System built using Python. It allows users to manage student records, including
adding, updating, and retrieving student information from a MySQL database.

## Features

- **Student Data Management**: Add, edit, and view student information including names and registration numbers.
   ![Student Management System](/assets/view_student_data.png)
- **Attendance Tracking**: Record and view student attendance with the ability to add columns for specific dates.
   ![Student Management System](/assets/add_attendance.png)
- **Grade Calculation**: Automatically calculate and update student grades based on their total scores.
   ![Student Management System](/assets/add_marks.png)
- **Marks Management**: Edit and update marks for various categories such as projects, assignments, quizzes, etc.
   ![Student Management System](/assets/add_student_data.png)
- **Data Visualization**: View student data and attendance records in a tabular format.
   ![Student Management System](/assets/view_attendance.png)
- **Query Execution**: Run predefined queries to extract meaningful insights from the data. 
   ![Student Management System](/assets/queries.png)
- **CRUD Operations**: Add, update, retrieve, and delete student records.

## Requirements

- Python 3.x
- MySQL Server
- MySQL Connector for Python

## Installation

### Prerequisites

- Python 3.x
- MySQL
- Required Python packages (mysql connector, tkinter)

### Setup

1. **Clone the Repository**

   ```bash
   git clone https://github.com/Nikhil-818/Student-Data-Management.git
   cd student-data-management
   ```

2. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

3. **Database Configuration**

    - For MySQL: Update the database configuration in the Python scripts with your MySQL credentials.
    - For SQLite: To use sqlite, update the `DatabaseConfig` class in the `DatabaseConfig.py` file and add the `.db` file to the directory.

4. **Initialize the Database**

    - Run the database initialization script to create necessary tables and insert sample data.

   ```bash
   python insert_sample_data.py
   ```

## Configuration

The database connection parameters are hardcoded in the `DatabaseConfig` class. You can modify these parameters directly
in the code if needed.

```python
class DatabaseConfig:
    @staticmethod
    def get_connection_params():
        return {
            "host": "your_host",
            "user": "user_name",
            "password": "password",
            "database": "database_name"
        }
```

## Usage

1. **Run the Application**

   Start the main application by executing the `user_name_Window.py` script.

   ```bash
   python user_name_Window.py
   ```

2. **Interact with the Application**

   Follow the prompts to add, update, retrieve, or delete student records.

3. **Navigate the Interface**

    - Use the tabs to switch between different functionalities such as adding attendance, viewing data, editing marks,
      etc.
    - Execute queries to gain insights into the student data.

## Project Structure

- `Attendance_Edit.py`: Module for managing attendance records.
- `Attendance_View.py`: Module for viewing attendance data.
- `Grade_Calculation.py`: Module for calculating and updating student grades.
- `Marks_Edit.py`: Module for editing student marks.
- `Queries.py`: Module for executing predefined queries.
- `user_name_Window.py`: Main application window.
- `Student_Data_Edit.py`: Module for managing student data.
- `Student_Data_View.py`: Module for viewing student data.
- `Total_Marks_Calculation.py`: Module for calculating total marks.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any improvements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.