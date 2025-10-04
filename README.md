# Week 2 Assignment - Express.js RESTful API

## 🚀 Objective
Build a RESTful API using Express.js that implements CRUD operations, middleware (logging, authentication, validation), error handling, and advanced features like filtering, pagination, search, and product statistics.

---

## 📂 Project Structure
├── server.js # Main server file
├── package.json # Node.js project file
├── package-lock.json # Auto-generated dependency lock file
├── README.md # Project documentation
└── .env.example # Example environment variables

---

## 🛠️ Setup Instructions

1. **Clone your GitHub repository**:
```bash
git clone <your-repo-url>
cd <your-repo-folder>
2. Install dependencies:
npm install
3. Start the server:
node server.js
4. Server will run at:
http://localhost:3000
🔑 Environment Variables

Create a .env file based on .env.example:
PORT=3000
API_KEY=mysecretkey
📌 API Endpoints
Root

GET /
Returns a welcome message.
Products
Get All Products

GET /api/products

Optional query parameters:

category → filter by category

page → page number for pagination

limit → number of items per page

Get Product by ID

GET /api/products/:id

Create New Product

POST /api/products

Requires Header: Products
Get All Products

GET /api/products

Optional query parameters:

category → filter by category

page → page number for pagination

limit → number of items per page

Get Product by ID

GET /api/products/:id

Create New Product

POST /api/products

Requires Header: 
x-api-key: mysecretkey
Body (JSON):
{
  "name": "Product Name",
  "description": "Product Description",
  "price": 100,
  "category": "electronics",
  "inStock": true
}
Update Product

PUT /api/products/:id

Requires Header:
x-api-key: mysecretkey
Body (JSON) same as above
Delete Product

DELETE /api/products/:id

Requires Header:
x-api-key: mysecretkey
Search Products

GET /api/search?name=keyword

Search products by name (case-insensitive).
Product Statistics

GET /api/stats

Returns count of products by category.
⚙️ Middleware

Logger → Logs method, URL, and timestamp for each request.

Authentication → Protects POST, PUT, DELETE routes using x-api-key.

Validation → Ensures proper product data on creation or update.

Global Error Handling → Returns errors with status code and message.
🧪 Testing the API

You can use Postman. Examples:
Get all products:
GET http://localhost:3000/api/products
Create product:
POST http://localhost:3000/api/products
Headers:
x-api-key: mysecretkey
Content-Type: application/json

Body:
{
  "name": "Blender",
  "description": "High-speed kitchen blender",
  "price": 150,
  "category": "kitchen",
  "inStock": true
}
