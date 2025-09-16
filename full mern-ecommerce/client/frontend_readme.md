# MERN Ecommerce Frontend

A modern React.js frontend for a full-featured ecommerce application with Redux Toolkit state management and Tailwind CSS styling.

**Author:** Youssef Abdalnaby

## Features

### User Interface
- **Modern Design**: Responsive UI with Tailwind CSS and shadcn/ui components
- **Role-based Access**: Separate interfaces for admin and shopping users
- **Interactive Elements**: Smooth animations and real-time updates

### Authentication & Shopping
- **User Authentication**: JWT-based login/register system
- **Product Catalog**: Browse, filter, and search products
- **Shopping Cart**: Add/remove items with quantity management
- **Checkout System**: PayPal payment integration
- **Order Tracking**: View order history and status

### Admin Features
- **Dashboard**: Feature image management and analytics
- **Product Management**: CRUD operations with image upload
- **Order Management**: View and update order status

### User Account
- **Profile Management**: Address management (max 3 addresses)
- **Review System**: Rate and review purchased products
- **Order History**: Track past orders and payments

## Tech Stack

- **Framework**: React 18 + Vite
- **State Management**: Redux Toolkit
- **Styling**: Tailwind CSS + shadcn/ui
- **Routing**: React Router DOM v6
- **HTTP Client**: Axios
- **UI Components**: Radix UI primitives
- **Icons**: Lucide React

## Project Structure

```
client/
├── src/
│   ├── components/
│   │   ├── admin-view/          # Admin interface
│   │   ├── shopping-view/       # Shopping interface  
│   │   ├── common/              # Shared components
│   │   └── ui/                  # UI primitives
│   ├── pages/                   # Route components
│   ├── store/                   # Redux store & slices
│   ├── config/                  # Form configs & constants
│   └── lib/                     # Utilities
├── components.json              # shadcn/ui config
├── tailwind.config.js           # Tailwind configuration
└── vite.config.js              # Vite configuration
```

## Quick Setup

1. **Install dependencies**
```bash
npm install
```

2. **Environment setup** (`.env`)
```env
VITE_API_BASE_URL=http://localhost:5000
```

3. **Start development**
```bash
npm run dev        # Development server
npm run build      # Production build
npm run preview    # Preview build
```

## Key Components & Features

### Redux Store Structure
- **Auth**: User authentication state
- **Admin**: Products and orders management
- **Shop**: Products, cart, orders, addresses, reviews, search
- **Common**: Feature images and shared data

### Component Architecture
- **Layouts**: AuthLayout, AdminLayout, ShoppingLayout
- **Forms**: Dynamic form builder with validation
- **UI Components**: Reusable button, card, dialog, table components
- **Product Components**: ProductTile, ProductDetails, CartItems

### Key Features Implementation

**Authentication Flow:**
- CheckAuth component handles route protection
- Role-based redirection (admin → dashboard, user → shop)
- JWT token management with cookies

**Shopping Experience:**
- Product filtering by category/brand
- Real-time search with debouncing
- Cart persistence and stock validation
- Multi-step checkout process

**Admin Panel:**
- Drag-drop image upload with Cloudinary
- Product CRUD with form validation
- Order status management
- Feature image carousel for homepage

**Payment Integration:**
- PayPal REST SDK integration
- Order creation and payment capture
- Success/failure handling

### Configuration Files

**Tailwind Config:**
- Custom color scheme with CSS variables
- Responsive breakpoints
- Animation utilities

**Vite Config:**
- Path aliases (`@/` for `src/`)
- React plugin configuration
- Development server setup

**shadcn/ui Config:**
- Component styling system
- Utility classes setup
- Theme configuration

## API Integration

All API calls use Axios with base URL from environment variables:
- Authentication endpoints (`/api/auth/`)
- Admin endpoints (`/api/admin/`)
- Shop endpoints (`/api/shop/`)
- Common endpoints (`/api/common/`)

## State Management

**Redux Slices:**
- Async thunks for API calls
- Normalized state structure
- Error and loading states
- Local storage integration for cart persistence

## Development Guidelines

- **Component Pattern**: Functional components with hooks
- **State Management**: Redux for global state, local state for UI
- **Styling**: Tailwind utility classes with shadcn/ui components
- **File Structure**: Feature-based organization
- **Code Quality**: ESLint configuration for React best practices

## Build & Deployment

**Development:**
- Vite dev server with HMR
- ESLint for code quality
- Path aliases for clean imports

**Production:**
- Optimized bundle with code splitting
- Environment variable configuration
- Static asset optimization

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile responsive design
- Progressive enhancement

## Author

**Youssef Abdalnaby**