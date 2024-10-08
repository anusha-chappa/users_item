# users_item

# FastAPI User Management API
This project demonstrates a simple User Management API built using [FastAPI](https://fastapi.tiangolo.com/). 
The API allows users to create, retrieve, and update user information stored in a JSON file.

## Features

- **GET /user**: Fetch user details by `user_id` or `name`.
- **POST /user**: Create a new user with `name`, `email`, and `phone_number`.
- **PUT /user/{user_id}**: Update existing user details by `user_id`.

## Setup Instructions

To run this project locally, follow these steps:

### Prerequisites
- Python 3.7 or higher
- [pip](https://pip.pypa.io/en/stable/) (Python package manager)

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/progress-journal.git
   cd progress-journal`` 

2.  **Install dependencies**:
    
    bash
    
    `pip install fastapi[all]` 
    
3.  **Create a JSON file for user data**:
    
    -   Ensure that you have a `users.json` file in the root directory. You can initialize it as an empty JSON object:
    
    json
    
    `{}` 
    

### Running the Application

Run the FastAPI application using Uvicorn:

bash
`uvicorn app:app --reload` 

-   The application will be available at `http://127.0.0.1:8000`.

### API Endpoints

1.  **Get User Details**:
    
    -   **Endpoint**: `GET /user`
    -   **Query Parameters**: `user_id` (optional), `name` (optional)
    -   **Response**: User details or a 404 error if not found.
    
    Example request:
    
    arduino
    `http://127.0.0.1:8000/user?user_id=1` 
    
2.  **Create a New User**:
    
    -   **Endpoint**: `POST /user`
    -   **Body**: JSON object with `name`, `email`, and `phone_number`.
    
    Example request:
    
    json
    `{
        "name": "bubby",
        "email": "xyz@example.com",
        "phone_number": "123-456-7890"
    }` 
    
    **Response**:
    
    json
    `{
        "message": "User bubby, ID {id} saved successfully"
    }` 
    
3.  **Update an Existing User**:
    
    -   **Endpoint**: `PUT /user/{user_id}`
    -   **Body**: JSON object with updated user details.
    
    Example request:
    
    json
    `{
        "name": "bubby",
        "email": "xyz@example.com",
        "phone_number": "987-654-3210"
    }` 
    
    **Response**:
    
    json
    `{
        "message": "User ID {user_id} updated successfully"
    }`