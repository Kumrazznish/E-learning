# E-Learning Platform

A full-stack e-learning platform built with React, Express.js, MongoDB, and Stripe for payments.

## 🚀 Features

- **User Authentication** - Login/Register with JWT
- **Course Management** - Create, edit, and publish courses
- **Video Lectures** - Upload and stream video content
- **Payment Integration** - Stripe checkout for course purchases
- **Progress Tracking** - Track student progress through courses
- **Admin Dashboard** - Analytics and course management
- **Responsive Design** - Works on all devices
- **Dark/Light Mode** - Theme switching support

## 🛠️ Tech Stack

### Frontend
- React 18
- Redux Toolkit & RTK Query
- React Router DOM
- Tailwind CSS
- Shadcn/ui Components
- Vite

### Backend
- Node.js & Express.js
- MongoDB & Mongoose
- JWT Authentication
- Stripe Payments
- Cloudinary (File uploads)
- Multer (File handling)

## 📁 Project Structure

```
├── src/                    # Frontend source code
│   ├── components/         # Reusable UI components
│   ├── pages/             # Page components
│   ├── features/          # Redux slices & API
│   ├── lib/               # Utilities & store
│   └── layout/            # Layout components
├── server/                # Backend source code
│   ├── controllers/       # Route controllers
│   ├── models/           # Database models
│   ├── routes/           # API routes
│   ├── middlewares/      # Custom middlewares
│   ├── utils/            # Utility functions
│   └── config/           # Configuration files
├── public/               # Static assets
└── uploads/              # File uploads directory
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v18 or higher)
- MongoDB database
- Cloudinary account
- Stripe account

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd e-learning-platform
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Setup**
   ```bash
   cp .env.example .env
   ```
   
   Fill in your environment variables:
   ```env
   MONGODB_URI=your-mongodb-connection-string
   SECRET_KEY=your-jwt-secret
   API_KEY=your-cloudinary-api-key
   API_SECRET=your-cloudinary-api-secret
   CLOUD_NAME=your-cloudinary-cloud-name
   STRIPE_SECRET_KEY=your-stripe-secret-key
   WEBHOOK_ENDPOINT_SECRET=your-stripe-webhook-secret
   ```

4. **Start Development Server**
   ```bash
   npm run dev
   ```
   
   This will start both frontend (http://localhost:5173) and backend (http://localhost:8080)

### Production Build

```bash
npm run build
npm start
```

## 📝 Available Scripts

- `npm run dev` - Start development servers (frontend + backend)
- `npm run dev:client` - Start only frontend development server
- `npm run dev:server` - Start only backend development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm start` - Start production server
- `npm run lint` - Run ESLint

## 🔧 API Endpoints

### Authentication
- `POST /api/v1/user/register` - User registration
- `POST /api/v1/user/login` - User login
- `GET /api/v1/user/logout` - User logout
- `GET /api/v1/user/profile` - Get user profile

### Courses
- `GET /api/v1/course/published-courses` - Get published courses
- `POST /api/v1/course` - Create course (instructor only)
- `PUT /api/v1/course/:id` - Update course
- `GET /api/v1/course/search` - Search courses

### Payments
- `POST /api/v1/purchase/checkout/create-checkout-session` - Create Stripe session
- `POST /api/v1/purchase/webhook` - Stripe webhook

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License.

## 🙏 Acknowledgments

- [Shadcn/ui](https://ui.shadcn.com/) for the beautiful UI components
- [Stripe](https://stripe.com/) for payment processing
- [Cloudinary](https://cloudinary.com/) for media management