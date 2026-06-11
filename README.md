# AI-Powered SQL Query Generator using LangChain & Gemini

## Overview

This project uses Google's Gemini AI model and LangChain to automatically generate MySQL queries from natural language questions. The application analyzes the database schema, converts user requests into valid SQL statements, executes them on a MySQL database, and returns the results.

## Features

* Natural language to SQL conversion
* Google Gemini 2.5 Flash integration
* Automatic database schema analysis
* MySQL database connectivity
* SQL query execution
* LangChain-powered prompt engineering
* Supports DDL, DML, and SELECT operations

## Technologies Used

* Python
* LangChain
* Google Gemini AI
* MySQL
* SQLAlchemy
* PyMySQL

## Installation

### Clone the Repository

```bash
git clone https://github.com/yourusername/ai-sql-generator.git
cd ai-sql-generator
```

### Install Dependencies

```bash
pip install langchain-community
pip install langchain-core
pip install langchain-google-genai
pip install google-generativeai
pip install pymysql
pip install sqlalchemy
```

Or install all at once:

```bash
pip install langchain-community langchain-core langchain-google-genai google-generativeai pymysql sqlalchemy
```

## Configuration

Set your Google API Key:

```python
os.environ["GOOGLE_API_KEY"] = "YOUR_API_KEY"
```

Configure your MySQL database connection:

```python
db = SQLDatabase.from_uri(
    "mysql+pymysql://username:password@localhost:3306/database_name"
)
```

## Project Workflow

1. Connect to MySQL database.
2. Retrieve database schema.
3. Accept a natural language question.
4. Send schema and question to Gemini AI.
5. Generate a valid SQL query.
6. Execute the query.
7. Display the results.

## Example

### User Question

```text
create a table for student marks
```

### Generated SQL

```sql
CREATE TABLE student_marks (
    student_id INT PRIMARY KEY,
    student_name VARCHAR(100),
    marks INT
);
```

## Project Structure

```text
project/
│
├── main.py
├── README.md
└── requirements.txt
```

## Future Improvements

* Streamlit Web Interface
* Voice Input Support
* Query Validation
* Database Visualization
* Multi-Database Support
* Query History Management

## Learning Outcomes

This project demonstrates:

* Generative AI integration
* LangChain workflows
* Prompt engineering
* Database automation
* Natural Language Processing
* SQL generation using LLMs

## Author

Amal

Computer Science Student

Interested in:

* Artificial Intelligence
* Machine Learning
* LangChain
* RAG Applications
* Python Development

## License

This project is open source and available under the MIT License.
