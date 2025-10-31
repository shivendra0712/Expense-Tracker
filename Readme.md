# Expense Tracker - MERN Stack Application

A full-stack expense tracking application built with MongoDB, Express.js, React.js, and Node.js. Features user authentication, CRUD operations, and real-time expense management.

##  Quick Start

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or Atlas)
- Git

### Installation

1. **Clone the repository**
```bash
git clone <repository-url>
cd Expense-Tracker
```

2. **Backend Setup**
```bash
cd backend
npm install
```

Create `.env` file in backend directory:
```env
PORT=5000
MONGODB_URI=mongodb+srv://shivendra:Shivendra123@patient-dashboard.9yngvv4.mongodb.net/Patient-Dashboard-mongodb
JWT_SECRET=expense-tracker
JWT_EXPIRES_IN=7d
FRONTEND_URL=http://localhost:5173
FRONTEND_URL=https://expense-tracker-pi-eight-11.vercel.app (deploy frontend url  on vercel)
```

3. **Frontend Setup**
```bash
cd frontend
npm install
```

Create `.env` file in Frontend directory:
```env
 VITE_BACKEND_URL=http://localhost:5000/api/
VITE_BACKEND_URL=https://expense-tracker-gst1.onrender.com/api (deploy backend url on render)
```


### Running the Application

1. **Start MongoDB**
```bash
mongod
```

2. **Start Backend Server**
```bash
cd backend
npm run dev
```
Server runs on: `http://localhost:5000`

3. **Start Frontend**
```bash
cd frontend
npm run dev
```
Frontend runs on: `http://localhost:5173`

##  Project Structure

```
Expense-Tracker/
├── backend/
│   ├── src/
│   │   ├── config/database.js
│   │   ├── controllers/
│   │   ├── middleware/
│   │   ├── models/
│   │   ├── routes/
│   │   └── app.js
│   ├── server.js
│   └── package.json
└── frontend/
    ├── src/
    │   ├── components/
    │   ├── pages/
    │   ├── store/
    │   └── App.jsx
    └── package.json
```

##  Features

### Core Features 
- **CRUD Operations**: Add, edit, delete, list expenses
- **Expense Fields**: Title, amount, category, date
- **Summary Display**: Total expenses and category-wise breakdown
- **React Hooks**: useState, useEffect for state management
- **Responsive Design**: TailwindCSS styling
- **RESTful APIs**: POST, GET, PUT, DELETE endpoints
- **MongoDB Integration**: Local/Atlas connection
- **Field Validation**: Required field validation

### Bonus Features 
- **JWT Authentication**: Login/signup with user-specific expenses
- **Edit Functionality**: Update existing expenses
- **Search & Filter**: Filter by category, date range, search by title
- **User Management**: Each user has isolated expenses

##  API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/me` - Get current user

### Expenses
- `GET /api/expenses` - Get user expenses
- `POST /api/expenses/create` - Create expense
- `PUT /api/expenses/:id` - Update expense
- `DELETE /api/expenses/:id` - Delete expense

##  Tech Stack

### Frontend
- **React.js** (Vite)
- **Redux Toolkit** (State management)
- **TailwindCSS** (Styling)
- **React Router** (Navigation)
- **Axios** (HTTP client)
- **React Toastify** (Notifications)

### Backend
- **Node.js** + **Express.js**
- **MongoDB** + **Mongoose**
- **JWT** (Authentication)
- **bcryptjs** (Password hashing)
- **CORS** (Cross-origin requests)

##  Usage

1. **Register/Login**: Create account or sign in
2. **Add Expenses**: Click "Add Expense" button
3. **View Summary**: See total and category breakdown
4. **Filter/Search**: Use search bar and filters
5. **Edit/Delete**: Use action buttons on expense items
6. **User Isolation**: Each user sees only their expenses

##  Development Notes

- User authentication required for all expense operations
- Expenses are filtered by user ID on backend
- Redux state cleared on user login/logout
- Responsive design works on mobile and desktop
- Real-time updates without page refresh

