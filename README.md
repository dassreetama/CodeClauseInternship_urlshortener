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

