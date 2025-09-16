# MERN Ecommerce Backend

A robust backend API for a full-featured ecommerce application built with Node.js, Express.js, and MongoDB.

**Author:** Youssef Abdalnaby

## Features

- **Authentication**: JWT-based auth with role management (Admin/User)
- **Product Management**: CRUD operations, image upload, search & filtering
- **Shopping Cart**: Add/remove items, quantity management
- **Order Processing**: PayPal integration, order tracking
- **Review System**: Product reviews with ratings
- **Address Management**: Multiple shipping addresses per user

## Tech Stack

- Node.js & Express.js
- MongoDB with Mongoose
- JWT Authentication
- Cloudinary (Image Storage)
- PayPal REST SDK
- Multer (File Upload)

## Project Structure

```
server/
├── controllers/     # Business logic
├── models/         # Database schemas
├── routes/         # API endpoints
├── helpers/        # Utilities (Cloudinary, PayPal)
└── server.js      # Entry point
```

## Quick Setup

1. **Install dependencies**
```bash
npm install
```

2. **Environment variables** (create `.env`)
```env
MONGODB_URI=your_mongodb_connection
JWT_SECRET=your_jwt_secret
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
PAYPAL_MODE=sandbox
PAYPAL_CLIENT_ID=your_paypal_client_id
PAYPAL_CLIENT_SECRET=your_paypal_client_secret
PORT=5000
```

3. **Update configuration files**
- Replace hardcoded values in `server.js`, `helpers/cloudinary.js`, `helpers/paypal.js`, and auth controller with environment variables

4. **Start server**
```bash
npm run dev  # Development
npm start    # Production
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/check-auth` - Verify auth

### Admin
- `GET /api/admin/products/get` - Get all products
- `POST /api/admin/products/add` - Add product
- `PUT /api/admin/products/edit/:id` - Update product
- `DELETE /api/admin/products/delete/:id` - Delete product
- `GET /api/admin/orders/get` - Get all orders
- `PUT /api/admin/orders/update/:id` - Update order status

### Shop
- `GET /api/shop/products/get` - Get filtered products
- `POST /api/shop/cart/add` - Add to cart
- `GET /api/shop/cart/get/:userId` - Get cart
- `POST /api/shop/order/create` - Create order
- `GET /api/shop/order/list/:userId` - Get user orders
- `POST /api/shop/review/add` - Add review
- `GET /api/shop/search/:keyword` - Search products

## Security

- Bcrypt password hashing
- JWT token authentication
- CORS protection
- Input validation

## Deployment

1. Set environment variables on hosting platform
2. Update CORS origin to your frontend domain
3. Ensure MongoDB is accessible
4. Configure Cloudinary and PayPal for production

**Recommended**: Heroku/Railway + MongoDB Atlas + Cloudinary

## Author

**Youssef Abdalnaby**