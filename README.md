# Student API

Simple RESTful API for managing students using Node.js, Express, and MongoDB.



## Prerequisites

- Node.js (v14 or higher recommended)
- MongoDB (local or Atlas cluster)
- Git (optional, for cloning)



## Setup Instructions

### 1. Clone the repository


git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name


### 2. Install dependencies


npm install


### 3. Configure MongoDB connection

* Replace the MongoDB URI in `app.js` with your own connection string, e.g.:

js
mongoose.connect("mongodb+srv://<username>:<password>@cluster0.mongodb.net/your-db-name");


* **Optional:** Use environment variables for security:

Create a `.env` file:


MONGO_URI=mongodb+srv://<username>:<password>@cluster0.mongodb.net/your-db-name


Update `app.js` to load it:


require('dotenv').config();
mongoose.connect(process.env.MONGO_URI);


### 4. Start the server


node app.js


or, if you have nodemon installed:


npx nodemon app.js


### 5. Server will run at


http://localhost:5000


## API Endpoints

| Endpoint            | Method | Description            |
| ------------------- | ------ | ---------------------- |
| `/api/students`     | POST   | Create a new student   |
| `/api/students`     | GET    | Retrieve all students  |
| `/api/students/:id` | PUT    | Update a student by ID |
| `/api/students/:id` | DELETE | Delete a student by ID |



## Example JSON for Creating a Student

json
{
  "name": "John Doe",
  "semester": "Fall 2025",
  "age": 22,
  "address": "123 Main Street",
  "DateOfBirth": "2003-01-15"
}


## Troubleshooting

* Ensure MongoDB connection URI is correct and accessible
* Verify MongoDB user has appropriate permissions
* Confirm port 5000 is free or change it in `app.js`


