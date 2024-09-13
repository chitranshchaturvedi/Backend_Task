# Rental Property Management & Trip Planning Backend

This backend provides APIs for a rental property management application where users can create property listings, plan trips, and allow others to join those trips. Built using **Node.js**, **Express.js**, and **MongoDB**, the backend supports user authentication, booking management, and listing of rental properties.

## Features

- **User Authentication**: Register and login users with JWT-based authentication.
- **Property Listings**: Create, update, delete, and view property listings.
- **Trip Planning**: Users can plan trips and allow others to join.
- **Booking Management**: Manage bookings and reservations.
- **Image Uploads**: Store and serve property images.

## Project Structure

```bash
├── models/                 # Mongoose models for MongoDB
│   ├── Booking.js          # Booking model for managing trip bookings
│   ├── Listing.js          # Listing model for properties
│   ├── User.js             # User model for authentication
├── public/uploads/         # Stores image uploads for listings
├── routes/                 # API route files
│   ├── auth.js             # Routes for user authentication
│   ├── booking.js          # Routes for managing bookings
│   ├── listing.js          # Routes for managing listings
│   ├── user.js             # Routes for user-specific data (profile, trips, etc.)
├── .env                    # Environment variables (JWT secret, Mongo URI, etc.)
├── index.js                # Main entry point to the backend
├── package.json            # Project metadata and dependencies
```

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/chitranshchaturvedi/Backend_Task
Install the dependencies:

bash
Copy code
cd rental-app
npm install
Set up the backend server (assuming you have already set up the Node.js, Express, and MongoDB backend):

bash
Copy code
cd backend
npm install
npm start
Start the React frontend:

bash
Copy code
cd frontend
npm start
Open http://localhost:3000 to view the application in the browser.

Project Structure
frontend/: Contains the React frontend code.
backend/: Contains the Express and MongoDB backend code.
models/: Mongoose models for the application (e.g., User, Listing).
routes/: API routes for handling requests to the backend.
pages/: Contains all the React pages such as HomePage, RegisterPage, LoginPage, etc.
components/: Reusable components across different pages.
Technologies Used
Frontend: React, React Router, Axios, Tailwind CSS
Backend: Node.js, Express, MongoDB, Mongoose
Other: React Toastify for notifications, bcrypt for password hashing
How to Contribute
Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make your changes.
Commit and push your changes (git push origin feature-branch).
Open a pull request.
License
This project is licensed under the MIT License - see the LICENSE file for details.

csharp
Copy code

This README provides an overview of the app, including setup instructions, routes, and features.
[9:59 pm, 13/9/2024] niKhiL RaJpuT Bhaiya : Rental Property Management & Trip Planning Backend
This backend provides APIs for a rental property management application where users can create listings, plan trips, and allow others to join those trips. Built using Node.js, Express.js, and MongoDB, the backend supports user authentication, booking management, and the listing of rental properties.

Features
User Authentication: Register and login users with JWT-based authentication.
Property Listings: Create, update, delete, and view property listings.
Trip Planning: Users can plan trips and allow others to join their trips.
Booking Management: Manage bookings and reservations for users.
Image Uploads: Store and serve property images.

Models Overview
User Model (User.js): Handles user information, authentication, and password encryption.
Listing Model (Listing.js): Manages property listing details such as address, price, amenities, and uploaded images.
Booking Model (Booking.js): Tracks bookings and trips planned by users. Other users can join the planned trips.
API Endpoints
User Authentication (auth.js)
Method	Endpoint	Description
POST	/api/auth/register	Register a new user
POST	/api/auth/login	Login and obtain JWT token
Property Listings (listing.js)
Method	Endpoint	Description
GET	/api/listings	Get all property listings
POST	/api/listings	Create a new property listing (authenticated)
GET	/api/listings/:listingId	Get a single property listing by ID
PUT	/api/listings/:listingId	Update a listing (authenticated)
DELETE	/api/listings/:listingId	Delete a listing (authenticated)
Trip Planning and Bookings (booking.js)
Method	Endpoint	Description
POST	/api/bookings	Create a new booking or plan a trip (authenticated)
GET	/api/bookings/:userId	Get all bookings/trips for a specific user
PUT	/api/bookings/:bookingId/join	Join an existing planned trip
DELETE	/api/bookings/:bookingId	Cancel or delete a trip/booking
User Management (user.js)
Method	Endpoint	Description
GET	/api/users/:userId/trips	Get all trips planned by a user
GET	/api/users/:userId/wishlist	Get all wishlist items for a user
GET	/api/users/:userId/profile	Get user profile information
Installation
Clone the repository:

bash
Copy code
git clone [https://github.com/your-username/rental-app-backend.git](https://github.com/chitranshchaturvedi/Backend_Task/tree/main)
Navigate into the project directory:

bash
Copy code
cd rental-app-backend
Install dependencies:

bash
Copy code
npm install
Set up the environment variables. Create a .env file in the root directory with the following values:

env
Copy code
MONGO_URI=<your-mongodb-connection-string>
JWT_SECRET=<your-jwt-secret>
PORT=5000
Start the server:

bash
Copy code
npm start
The server will run on http://localhost:5000.

Usage
Register a User
Endpoint: POST /api/auth/register
Description: Registers a new user and returns a JWT for authentication.
Create a Property Listing
Endpoint: POST /api/listings
Description: Authenticated users can create a new property listing.
Plan a Trip and Let Others Join
Endpoint: POST /api/bookings
Description: Authenticated users can plan a trip. Others can join with PUT /api/bookings/:bookingId/join.
Get User's Trips
Endpoint: GET /api/users/:userId/trips
Description: Retrieve all trips that a user has planned.
Image Uploads
The folder /public/uploads/ stores all image uploads for the listings.
Images are uploaded via multipart/form-data through the listing creation endpoint.
Dependencies
Express.js: Fast, unopinionated, minimalist web framework for Node.js.
Mongoose: Elegant MongoDB object modeling for Node.js.
JWT (jsonwebtoken): For user authentication.
bcryptjs: For hashing passwords.
multer: For handling multipart/form-data, used for uploading images.
Contributing
Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make your changes.
Commit and push your changes (git push origin feature-branch).
Open a pull request.
License
This project is licensed under the MIT License. See the LICENSE file for details.

yaml
