# ShopBill - Billing Management System

A full-stack billing and inventory management system built with Java Spring Boot (backend) and React.js (frontend).

## 📋 Features

- User authentication and authorization (JWT, role-based)
- Product and category management (CRUD)
- Order processing and shopping cart
- Payment integration with Razorpay
- AWS S3 file uploads for product images
- Dashboard analytics and reporting
- Invoice generation and receipt printing
- Responsive UI with React.js

## 🛠️ Tech Stack

- **Backend:** Java 17+, Spring Boot, Spring Security, MySQL, JWT, Maven
- **Frontend:** React.js, Vite, Axios, CSS
- **Other:** Razorpay API, AWS S3, RESTful APIs

## 🚀 Getting Started

### Prerequisites

- Java 17 or higher
- Node.js and npm
- MySQL database
- Maven (or use the included Maven wrapper)

### 1. Clone the Repository

```sh
git clone https://github.com/aakashkrrj/ShopBill.git
cd ShopBill/Billing-System
```

### 2. Backend Setup

1. Navigate to the backend directory:
   ```sh
   cd billingsoftware
   ```

2. Configure your database and third-party credentials in `src/main/resources/application.properties`:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/billing_app
   spring.datasource.username=YOUR_DB_USER
   spring.datasource.password=YOUR_DB_PASSWORD
   razorpay.key_id=YOUR_RAZORPAY_KEY_ID
   razorpay.key_secret=YOUR_RAZORPAY_KEY_SECRET
   aws.accessKey=YOUR_AWS_ACCESS_KEY
   aws.secretKey=YOUR_AWS_SECRET_KEY
   aws.region=YOUR_AWS_REGION
   aws.s3.bucket=YOUR_BUCKET_NAME
   ```

3. Import the database schema:
   - Import `billing_app.sql` into your MySQL database.

4. Run the backend server:
   ```sh
   ./mvnw spring-boot:run
   # or on Windows
   mvnw.cmd spring-boot:run
   ```
   - The backend will run on [http://localhost:8081](http://localhost:8081) (or as configured).

### 3. Frontend Setup

1. Open a new terminal and navigate to the frontend directory:
   ```sh
   cd client
   ```

2. Install dependencies:
   ```sh
   npm install
   ```

3. Start the React development server:
   ```sh
   npm run dev
   ```
   - The frontend will run on [http://localhost:5173](http://localhost:5173) or [http://localhost:5174](http://localhost:5174).

### 4. Configuration

- Ensure the frontend API base URL matches your backend port (e.g., `http://localhost:8081`).
- Update CORS settings in the backend if you change frontend port.

## 📖 Usage

- Register or log in as a user or admin.
- Manage products, categories, and users (admin only).
- Add items to cart, place orders, and process payments.
- View dashboard analytics and order history.

## 📁 Project Structure

```
ShopBill/
├── Billing-System/
│   ├── billingsoftware/     # Spring Boot backend
│   ├── client/              # React.js frontend
│   └── billing_app.sql      # Database schema
└── README.md
```

## 📝 License

MIT

## 👤 Author

**aakashkrrj**

- GitHub: [@aakashkrrj](https://github.com/aakashkrrj)

