Agri Ecommerce Platform
Overview
This project is a agricultural e-commerce platform designed to provide fair pricing for farmers and seamless purchasing for consumers. It includes essential e-commerce functionalities such as product listing, cart management, checkout, and user authentication. The backend is built using Node.js/Express with MySQL, and the frontend is developed using React.js.
Features
User Authentication: Registration, Login, and Session Management.
Product Listings: Display products with images and descriptions.
Cart Functionality: Add, remove, and update items in the cart.
Checkout Process: Secure order processing and payment gateway integration.
Order Management: View order history and invoice generation.
Admin Panel (Future Scope): Manage products, orders, and users.

Folder Structure
Agri-Ecommerce/
│── backend/               # Backend implementation
│   ├── models/           # Database models
│   ├── routes/           # API routes
│   ├── middleware/       # Authentication and validation middleware
│   ├── config/           # Database configuration
│   ├── server.js         # Express server setup
│
│── frontend/              # Frontend implementation
│   ├── src/
│   │   ├── components/    # Reusable UI components
│   │   ├── pages/         # Pages (Home, Products, Checkout, etc.)
│   │   ├── context/       # Context API for state management
│   │   ├── assets/        # Static images and styles
│   │   ├── App.js         # Main React component
│   │   ├── index.js       # React entry point
│
│── README.md              # Project documentation
│── package.json           # Dependencies and scripts
│── .env                   # Environment variables


Backend Implementation
Technology Stack:
Node.js - Server-side runtime
Express.js - Web framework for API development
MySQL - Database for storing users, products, and orders
JWT (JSON Web Token) - User authentication
bcrypt.js - Password hashing for security
Key Files:
server.js: Initializes the Express server.
routes/: Contains API endpoints for authentication, products, orders, and cart.
models/: Defines MySQL database schemas using Sequelize or raw queries.
middleware/: Authentication middleware for securing routes.
Database Schema:
Users Table: Stores user information (id, name, email, password, etc.).
Products Table: Stores product details (id, name, price, image, etc.).
Cart Table: Manages user cart items (user_id, product_id, quantity, etc.).
Orders Table: Tracks completed purchases (order_id, user_id, total_amount, etc.).

Frontend Implementation
Technology Stack:
React.js - Frontend framework for UI development
React Context API - State management for authentication and cart
Axios - Handling API requests
React Router - Navigation between pages
Tailwind CSS - Styling
Key Components:
Navbar.jsx: Navigation bar with dynamic cart count.
Home.jsx: Landing page displaying featured products.
Products.jsx: Displays product listings fetched from the backend.
Cart.jsx: Shows items added to the cart and allows checkout.
Checkout.jsx: Order summary and payment processing.
AuthContext.js: Manages user authentication state.
CartContext.js: Manages cart operations across the application.

Installation & Setup
1. Clone the Repository:
git clone https://github.com/your-repo/agri-ecommerce.git
cd agri-ecommerce

2. Backend Setup:
cd backend
npm install
cp .env.example .env   # Update database credentials
node server.js

3. Frontend Setup:
cd frontend
npm install
npm start

4. Database Setup:
mysql -u root -p < database_dump.sql


API Endpoints
Authentication Routes:
Method
Endpoint
Description
POST
/api/auth/register
Register new user
POST
/api/auth/login
User login
POST
/api/auth/logout
Logout user
GET
/api/auth/session
Check user session

Product Routes:
Method
Endpoint
Description
GET
/api/products
Get all products
GET
/api/products/:id
Get product by ID

Cart Routes:
Method
Endpoint
Description
POST
/api/cart/add
Add product to cart
GET
/api/cart
Get user cart
DELETE
/api/cart/remove
Remove item from cart

Order Routes:
Method
Endpoint
Description
POST
/api/orders/checkout
Process checkout
GET
/api/orders
Get user orders


Future Enhancements
Admin Dashboard: For managing products and orders.
Payment Gateway Integration: Secure online payments.
Reviews & Ratings: Allow users to review products.
Mobile App Version: React Native-based mobile app.

Contributors
Your Name - Aditi Perim

