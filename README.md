# Internship_Flask_Task_1
# Flask Username Uppercase Converter
## Project Overview

This project is a lightweight Flask web application that demonstrates how to handle URL query parameters in a web application. The application accepts a username from the browser URL, converts the name into UPPER CASE, and displays the transformed output directly on the web page.

The project was developed and tested using Jupyter Notebook, making it easy for beginners to understand Flask fundamentals and local server execution.

This project is ideal for learning:

Flask basics

Routing and request handling

Query parameters

Simple dynamic HTML responses

Running Flask applications in Jupyter Notebook

## Features

✔️ Accepts user input through URL query parameters

✔️ Converts the username to UPPER CASE

✔️ Displays original and transformed output in the browser

✔️ Error handling when no name is provided

✔️ Lightweight and beginner-friendly

✔️ Easily extendable for additional features

## Technologies Used

Python

Flask

Jupyter Notebook

HTML (basic rendering)

## Project Structure
Flask-Username-Uppercase/
│
├── notebook.ipynb     # Jupyter Notebook containing Flask code
├── README.md          # Project documentation

## How to Run the Project (Jupyter Notebook)
Step 1: Install Flask

Run this command in a Jupyter cell:

!pip install flask

Step 2: Paste Flask Code
from flask import Flask, request

app = Flask(__name__)

@app.route("/name")
def convert_to_upper():
    user_name = request.args.get("user")

    if not user_name:
        return "<h3 style='color:red'>Please provide a name in URL</h3>"

    upper_name = user_name.upper()

    return f"""
    <h2>Username Converter</h2>
    <p><b>Original Name:</b> {user_name}</p>
    <p><b>Upper Case Name:</b> {upper_name}</p>
    """


Run the cell.

Step 3: Start Flask Server

In a new cell, run:

app.run(port=5000)


The server will start at:

http://127.0.0.1:5000/

Step 4: Test in Browser

Open your browser and visit:

http://127.0.0.1:5000/name?user=venu


Replace venu with any name.

## Sample Output

Input URL:

http://127.0.0.1:5000/name?user=alex


Output:

Original Name: alex
Upper Case Name: ALEX

## Limitations

Designed for local execution only

Flask server blocks notebook execution

Not recommended for production deployment

Best suited for learning and demonstration

## Future Enhancements

Add HTML templates and CSS styling

Add input form instead of URL typing

Add reverse name feature

Add name length counter

Add API JSON response

Deploy on cloud platform

# Author

Bathula Venu Gopal
Data Science Intern – Innomatics Research Labs
Batch 419
