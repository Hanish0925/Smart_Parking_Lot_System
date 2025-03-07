# Smart Parking lot System

## Overview
The **Smart parking lot system** is a backend application designed to manage parking spot allocation, user reservations, and parking zone preferences. It optimizes spot allocation by prioritizing proximity, floor preference, and designated parking zones.

This project is built using **Node.js**, **Express.js**, and an in-memory database (arrays) for simplicity. It uses **JWT (JSON Web Tokens)** for authentication and **bcrypt** for password hashing.

---

## Features 
- **Parking spot allocation**:
  - Prioritize spots based on proximity, floor preference, and parking zones.
  - Real-time availability updates.
- **Reservation Management**:
  - Reserve and release parking spots.
  - Manage reservation time slots.
- **Session Management**:
  - Uses MongoDB session that enables transactions.
  - Transactions ensure that all database operations within them are atomic—either all succeed, or none are applied.
- **Solid Principles**:
  - Applied solid principles to make sure my code is smooth and transparent.

---

## Technologies Used
- **Backend**: Node.js, Express.js
- **Environment Variables**: dotenv

---

## Setup Instructions

### Prerequisites
- Node.js (v14 or higher)
- npm (Node Package Manager)

### Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/Hanish0925/Smart_Parking_Lot_System.git
cd Smart_Parking_Lot_System
   ```
2. Install dependencies:
    ```sh
    npm install
    ```
3. Set up environment variables:
    - Create a `.env` file in the root directory.
    - Add the following environment variables:
        ```
        MONGO_URI="your_mongo_uri"
        PORT=portnumber

## Usage

1. Start the server:
    ```sh
    npm run dev
    ```

2. The server will be running on `http://localhost:3000`.

## API Endpoints

### Parking Spot Allocation

- **Check In**
    - `POST /parking/checkin`
    - Request Body:
        ```json
        {
          "type": "motorcycle",
          "licensePlate": "ABC-2134"
        }
        ```
- **Check Out**
    - `POST /parking/checkout`
    -  Request Body:
        ```json
        {
          "transactionId": "67c994aa4a8ce06fe718e658"
        }
        ```
- **Get Availabilty**
    - `GET /parking/availability`
    
## Running Tests

To run the tests, use the following command:
```sh
npm test