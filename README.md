# Patreon Payment API

The **Patreon Payment API** provides a Python-based solution for interacting with Patreon. This API allows you to retrieve data about paid and non-paid members, simplifying the integration of Patreon payment information into your projects.

![license](https://img.shields.io/badge/license-MIT-red)

## Table of Contents
- [Installation](#installation)
- [Setup](#setup)
- [Running the API](#running-the-api)
- [API Endpoints](#api-endpoints)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Installation

To set up the project locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/exrod/patreon-payment-api.git
   cd patreon-payment-api
   ```

2. Create a virtual environment:
   ```bash
   python3 -m venv venv
   ```

3. Activate the virtual environment:
   - On **Windows**:
     ```bash
     venv\Scripts\activate
     ```
   - On **Unix** or **MacOS**:
     ```bash
     source venv/bin/activate
     ```

4. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Setup

Before running the API, you need to configure your Patreon API access:

1. Obtain a **Patreon API access token**.
2. Set the token as an environment variable:
   ```bash
   export ACCESS_TOKEN=your_access_token
   ```
   Alternatively, you can update the `.env` file with your access token.

## Running the API

To run the API server:

1. Start the Flask server:
   ```bash
   python main.py
   ```

2. The API will be accessible at `http://localhost:6969`.

## API Endpoints

### 1. Get Non-Paid Members Information

- **Endpoint**: `/patreon/non_active`
- **Method**: `GET`
- **Description**: Fetches detailed information about non-paid members.
- **Example Request**:
  ```bash
  curl -X GET "http://localhost:6969/patreon/non_active"
  ```

### 2. Get Paid Members Information

- **Endpoint**: `/patreon/active`
- **Method**: `GET`
- **Description**: Fetches detailed information about paid members.
- **Example Request**:
  ```bash
  curl -X GET "http://localhost:6969/patreon/active"
  ```

### 3. Get All Members Information

- **Endpoint**: `/patreon`
- **Method**: `GET`
- **Description**: Retrieves detailed information about all members, both paid and non-paid.
- **Example Request**:
  ```bash
  curl -X GET "http://localhost:6969/patreon"
  ```

## Usage

After starting the server, you can interact with the API using tools like `curl` or Postman. Simply send HTTP requests to the appropriate endpoints to retrieve the desired member data.

## Contributing

We welcome contributions to improve this project! To contribute:
- Open an issue if you encounter a bug or have suggestions for enhancements.
- Submit a pull request with your proposed changes.

## License

This project is licensed under the [MIT License](LICENSE).

## Contact

For any inquiries, please contact the repository owner via [devinrhinos](https://github.com/exrod).
