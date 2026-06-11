# AI SQL Query Generator using LangChain & Gemini

## Overview

This project converts natural language questions into executable MySQL queries using Google's Gemini AI and LangChain. The application automatically reads the database schema, generates SQL queries from user prompts, cleans the generated SQL, and executes it on a MySQL database.

## Features

* Natural Language to SQL Conversion
* Google Gemini 2.5 Flash Integration
* MySQL Database Connectivity
* Automatic Schema Extraction
* SQL Query Execution
* LangChain Prompt Engineering
* SQL Cleanup Before Execution
* Error Handling

---

## Technologies Used

* Python
* LangChain
* Google Gemini AI
* MySQL
* SQLAlchemy
* PyMySQL
* Python Dotenv

---

## Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/ai-sql-query-generator.git
cd ai-sql-query-generator
```

### Install Required Packages

```bash
pip install python-dotenv
pip install langchain-community
pip install langchain-core
pip install langchain-google-genai
pip install google-generativeai
pip install pymysql
pip install sqlalchemy
```

Or install everything at once:

```bash
pip install python-dotenv langchain-community langchain-core langchain-google-genai google-generativeai pymysql sqlalchemy
```

---

## Configuration

### Step 1: Create a .env File

Create a file named `.env` in the project root directory.

```env
GOOGLE_API_KEY=your_google_api_key_here
```

Replace `your_google_api_key_here` with your Gemini API key.

---

### Step 2: Configure MySQL Connection

Locate this line in the code:

```python
db = SQLDatabase.from_uri(
    "mysql+pymysql://root:YOURPASSWORD@localhost:3306/college_db"
)
```

Replace:

```text
YOURPASSWORD
```

with your actual MySQL password.

Example:

```python
db = SQLDatabase.from_uri(
    "mysql+pymysql://root:MyPassword123@localhost:3306/college_db"
)
```

Also make sure:

* MySQL Server is running
* Database `college_db` exists
* User credentials are correct

---

## Project Structure

```text
AI-SQL-Generator/
│
├── SQL.py
├── .env
├── requirements.txt
├── README.md
└── .gitignore
```

---

## How It Works

1. Connects to the MySQL database.
2. Extracts the database schema.
3. Sends the schema and user question to Gemini AI.
4. Gemini generates a SQL query.
5. The application removes markdown formatting if present.
6. The SQL query is executed.
7. Results are displayed.

---

## Example

### User Question

```text
create a table for student marks
```

### Generated SQL

```sql
CREATE TABLE student_marks (
    student_id INT AUTO_INCREMENT PRIMARY KEY,
    marks INT
);
```

---

## Running the Application

```bash
python SQL.py
```

---

## Security Notes

### Never Upload These Files to GitHub

* `.env`
* Files containing API keys
* Files containing database passwords

Create a `.gitignore` file:

```gitignore
.env
__pycache__/
*.pyc
.idea/
venv/
.venv/
```

---

## Future Improvements

* Streamlit Interface
* Voice-Based Query Input
* Query Validation
* Query History
* Multi-Database Support
* Database Visualization

---

## Learning Outcomes

This project demonstrates:

* Generative AI Integration
* LangChain Workflows
* Prompt Engineering
* Database Automation
* SQL Generation Using LLMs
* Python Backend Development

---

## Author

Amal

Computer Science Student

Interests:

* Artificial Intelligence
* Machine Learning
* Generative AI
* LangChain
* SQL Automation
* Python Development

---

## License

This project is open-source and available under the MIT License.
