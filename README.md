# URL Shortener Web Application

A simple URL shortener web application built using Python, Flask, and the pyshorteners library.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Code Explanation](#code-explanation)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project demonstrates how to create a URL shortener web application using Python and Flask. The application allows users to input a long URL and receive a shortened version using the pyshorteners library.

## Features

- Shorten long URLs using the pyshorteners library
- Simple and user-friendly web interface
- Easy to deploy and run locally

## Requirements

- Python 3.x
- Flask
- pyshorteners

## Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/yourusername/url-shortener.git
    cd url-shortener
    ```

2. Create a virtual environment:

    ```sh
    python -m venv myenv
    ```

3. Activate the virtual environment:

    - On Windows:

        ```sh
        myenv\Scripts\activate.bat
        ```

    - On Linux/macOS:

        ```sh
        source myenv/bin/activate
        ```

4. Install the required packages:

    ```sh
    pip install flask pyshorteners
    ```

## Usage

1. Run the application:

    ```sh
    python main.py
    ```

2. Open your web browser and navigate to `http://127.0.0.1:5000/`.

3. Enter a long URL in the provided input field and click "Submit" to generate a shortened URL.

## Project Structure

## Code Explanation

The code imports the pyshorteners library and the following modules from the Flask framework, all of which are needed for shortening URLs:

- **Flask**: The Flask framework itself, which is used to create the web application.
- **render_template**: A template rendering package used to generate the output of HTML files from the folder `templates`.
- **request**: An object from the Flask framework that contains all the data that a user sends from the frontend to the backend as a part of an HTTP request.

The function `home()` is created to take a URL submitted in the form and output a short URL. The `app.route()` decorator binds the function to the specific URL route for running the app, and the POST/GET methods handle the requests.

In the `home()` function, there is an if-else conditional statement:

- For the if statement (`if request.method=="POST"`):
  - A variable called `url_received` is set to `request.form["url"]`, which is the URL submitted in the form. Here, `url` is the name of the input field defined in the HTML form created earlier.
  - A variable called `short_url` is set to `pyshorteners.Shortener().tinyurl.short(url_received)`. Here, two methods are used from the pyshorteners library: `.Shortener()` and `.short()`. The `.Shortener()` function creates a pyshorteners class instance, and the `.short()` function takes in the URL as an argument and shortens it.
  - The `short()` function `tinyurl.short()` is one of the pyshorteners library’s many APIs. Another example is `osdb.short()`, which can also be used for the same purpose.
  - The `render_template()` function is used to render the HTML file template `form.html` and send URLs back to the form through arguments. The `new_url` argument is set to `short_url` and `old_url` is set to `url_received`.

- For the else statement (`else`):
  - If the request method is other than POST, only the `form.html` HTML template will be rendered.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

