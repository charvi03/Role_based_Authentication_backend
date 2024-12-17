# Role-Based Authentication Backend

This is a Node.js and Express.js backend project implementing role-based authentication. It allows users to sign up, log in, and access different routes based on their assigned roles (Admin, Student).

---

## **Features**
- User registration and login.
- Password hashing using `bcrypt`.
- Role-based access control (RBAC).
- JWT authentication with tokens stored in **cookies**.
- Secure `.env` configuration for environment variables.

---

## **Technologies Used**
- **Node.js**: JavaScript runtime.
- **Express.js**: Web framework for Node.js.
- **MongoDB**: Database for storing user data.
- **bcrypt**: For password hashing.
- **jsonwebtoken (JWT)**: To generate and verify access tokens.
- **cookie-parser**: To parse and manage cookies.
- **dotenv**: For environment variables.
- **mongoose**: ODM for MongoDB.

---

## **Project Setup**

### **1. Clone the Repository**
```bash
git clone <repository-url>
cd <project-folder>
```
## **2. Install Dependencies**
Run the following command to install the required packages:

```bash
npm install
```

## **3. Configure Environment Variables**
Create a .env file in the project root and add your environment variables as shown below:

```bash
PORT = 5000
MONGODB_URL = "db_link"
JWT_SECRET = secret_code
```
## **4. Start the Server**
Start the development server using the following command:

```bash
npm run dev
```

## **API Endpoints**
### **1. User Signup**
- Endpoint: POST /api/roles/signup
- Request Body:
```bash
{
  "name": "abc",
  "email": "abc@example.com",
  "password": "SecurePass123",
  "role": "Admin"
}

```
### **2. User Login**
- Endpoint: POST /api/roles/login
- Request Body:
```bash
{
  "email": "abc@example.com",
  "password": "SecurePass123",
 }
```
### **3. Protected Role-Based Route**
- Endpoints:
  - GET /api/roles/student
  - GET /api/roles/admin
  - GET /api/roles/test
 - Request Body:
```bash
{
  "email": "abc@example.com",
  "password": "SecurePass123",
 }
```
