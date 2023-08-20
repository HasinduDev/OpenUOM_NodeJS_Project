# NodeJS Guided Project: Customer Registration API

This project demonstrates the development of a NodeJS application that serves as a REST API for registering customers and storing their information in a SQLite database. The API also includes validation for email addresses and credit card numbers.

## Prerequisites

- Node.js: Ensure you have Node.js installed on your machine.
- SQLite: Make sure you have SQLite installed as the database engine.

## Getting Started

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create the SQLite database:
   ```bash
   touch db.sqlite
   ```

4. Initialize the database schema:
   ```bash
   node app.js
   ```

5. Start the server:
   ```bash
   node app.js
   ```

## Usage

### Register a Customer

**Endpoint:** POST `/api/customer/register`

**Request Body:**
```json
{
    "name": "John Doe",
    "address": "123 Main St",
    "email": "john@example.com",
    "dateOfBirth": "1990-01-01",
    "gender": "male",
    "age": 30,
    "cardHolderNames": "John Doe",
    "cardNumber": "123456789012",
    "expiryDate": "12/25",
    "cvv": 123,
    "timeStamp": "2023-08-21T12:00:00Z"
}
```

**Response:**
- If successful:
  ```json
  {
      "message": "Customer John Doe has registered",
      "customerId": "1"
  }
  ```
- If validation fails (e.g., invalid email or credit card):
  ```json
  {
      "error": "Invalid Email Address"
  }
  ```

### Root Path

**Endpoint:** GET `/`

**Response:**
```json
{
    "message": "University of Moratuwa"
}
```

## Contributing

Contributions to this project are welcome! If you find any bugs or want to enhance the functionality, please submit an issue or a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

*Note: This project was developed as part of the University of Moratuwa's guided project for NodeJS. It showcases the implementation of a customer registration API using Node.js and SQLite.*