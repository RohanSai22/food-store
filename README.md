

# MERN Stack - Xen Estate

**Xen Estate** is a full-stack real estate application built using the MERN stack (MongoDB, Express.js, React, Node.js). This application allows users to browse properties, view property details, and manage listings, creating a smooth and responsive experience for real estate needs.

## Features

- **User Authentication** - Sign in and sign up using email/password and OAuth options
- **Property Listings** - Users can create, update, and delete their property listings
- **Profile Management** - Users can view and update their profile information
- **Real-Time Search** - Search for properties by location, type, or other filters
- **Responsive Design** - Optimized for desktop and mobile

## Technologies Used

- **Frontend**: React, Redux, Tailwind CSS, Vite
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: Firebase (OAuth), JWT
- **Deployment**: Vite

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/your-username/xen_estate.git
   cd xen_estate
   ```

2. **Install Dependencies**

   Install server dependencies:

   ```bash
   cd server
   npm install
   ```

   Install client dependencies:

   ```bash
   cd ../client
   npm install
   ```

3. **Environment Variables**

   Set up your environment variables. Create a `.env` file in the `server` directory and add:

   ```plaintext
   MONGO_URI=your-mongodb-connection-string
   JWT_SECRET=your-jwt-secret
   ```

   In the `client` directory, create a `.env` file to store Firebase credentials for authentication.

4. **Run the Application**

   In separate terminals for client and server:

   - **Client**: `npm run dev` (from the `client` directory)
   - **Server**: `npm run dev` (from the `server` directory)

   The client should be available at `http://localhost:3000`, and the server at `http://localhost:5000`.

## Project Structure

The project is organized into logical directories and files:

### Server

- **api/** - Contains the main entry file for API endpoints
  - **controllers/**
    - `auth.controller.js` - Handles authentication operations like login and signup
    - `listing.controller.js` - Manages CRUD operations for property listings
    - `user.controller.js` - Handles user-related operations
  - **models/**
    - `listing.model.js` - Mongoose schema for property listings
    - `user.model.js` - Mongoose schema for users
  - **routes/**
    - `auth.route.js` - Routes related to authentication
    - `listing.route.js` - Routes for creating, updating, and deleting listings
    - `user.route.js` - Routes for user profiles and related actions
  - **utils/**
    - `error.js` - Custom error handling utilities
    - `verifyUser.js` - Middleware for user verification using JWT
  - `index.js` - The main entry point of the server, initializing Express and connecting to MongoDB

### Client

- **src/**
  - **components/** - Reusable components for building the UI
    - `Contact.jsx` - Contact form for inquiries
    - `Header.jsx` - Main navigation and header
    - `ListingItem.jsx` - Component to display individual property listings
    - `OAuth.jsx` - OAuth functionality with Firebase
    - `PrivateRoute.jsx` - Protected route for authenticated users
  - **pages/** - Pages representing main application views
    - `About.jsx` - About page
    - `CreateListing.jsx` - Page for creating new listings
    - `Home.jsx` - Homepage with featured listings
    - `Listing.jsx` - Detailed view of an individual listing
    - `Profile.jsx` - User profile page
    - `Search.jsx` - Search page for finding properties
    - `SignIn.jsx` - Sign-in page
    - `SignUp.jsx` - Sign-up page
    - `UpdateListing.jsx` - Page for updating existing listings
  - **redux/**
    - `user/` - Redux logic for managing user state
    - `store.js` - Redux store setup for state management
  - `App.jsx` - Main application file managing routes and layout
  - `firebase.js` - Firebase configuration for authentication
  - `index.css` - Global CSS styles
  - `main.jsx` - Root file rendering the React app

### Configuration & Build Files

- `.eslintrc.cjs` - Linting configuration for code consistency
- `postcss.config.js` - PostCSS configuration for Tailwind CSS
- `tailwind.config.js` - Tailwind CSS configuration
- `vite.config.js` - Vite configuration for building the React application

## API Endpoints

The backend provides the following RESTful API endpoints:

- **Auth**:
  - `POST /auth/register` - Register a new user
  - `POST /auth/login` - Login user and return JWT
- **Users**:
  - `GET /users/:id` - Get user profile by ID
  - `PUT /users/:id` - Update user profile
- **Listings**:
  - `GET /listings` - Retrieve all property listings
  - `POST /listings` - Create a new listing
  - `GET /listings/:id` - Retrieve a listing by ID
  - `PUT /listings/:id` - Update a listing by ID
  - `DELETE /listings/:id` - Delete a listing by ID

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature-branch`)
3. Make your changes
4. Commit the changes (`git commit -m 'Add new feature'`)
5. Push to the branch (`git push origin feature-branch`)
6. Open a Pull Request

## License

This project is licensed under the MIT License.

## Contact

For any questions or feedback, please reach out at [maragonirohansai@gmail.com](mailto:maragonirohansai@gmail.com).

