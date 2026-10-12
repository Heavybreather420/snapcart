# SnapCart

A full-stack e-commerce platform built with Next.js, featuring real-time notifications, interactive maps, and payment processing.

## 🚀 Features

- **Real-time notifications** with Socket.io
- **Interactive maps** with Leaflet for location services
- **Payment processing** with Stripe
- **Authentication** with NextAuth (Google OAuth)
- **Image management** with Cloudinary
- **AI integration** with Gemini API
- **Email notifications** with Nodemailer
- **State management** with Redux Toolkit
- **Modern UI** with Tailwind CSS and Framer Motion

## 📁 Project Structure

```
snapcart/
├── 1.snapcart/          # Next.js frontend application
│   ├── src/             # Source files
│   ├── public/          # Static assets
│   └── package.json
└── socketServer/        # Express + Socket.io backend
    ├── index.js         # Server entry point
    └── package.json
```

## 🛠️ Prerequisites

- Node.js 20.x or higher
- MongoDB database
- npm or yarn

## ⚙️ Setup Instructions

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd 1.snapcartFolder
```

### 2. Install dependencies

**Frontend:**
```bash
cd 1.snapcart
npm install
```

**Backend:**
```bash
cd socketServer
npm install
```

### 3. Environment Configuration

**Frontend (`1.snapcart/.env.local`):**

Copy `.env.example` to `.env.local` and fill in your credentials:

```bash
cp .env.example .env.local
```

Required variables:
- `MONGODB_URL` - MongoDB connection string
- `AUTH_SECRET` - NextAuth secret key
- `GOOGLE_CLIENT_ID` - Google OAuth client ID
- `GOOGLE_CLIENT_SECRET` - Google OAuth client secret
- `CLOUDINARY_CLOUD_NAME` - Cloudinary cloud name
- `CLOUDINARY_API_KEY` - Cloudinary API key
- `CLOUDINARY_API_SECRET` - Cloudinary API secret
- `STRIPE_SECRET_KEY` - Stripe secret key
- `STRIPE_WEBHOOK_SECRET` - Stripe webhook secret
- `GEMINI_API_KEY` - Google Gemini API key
- `EMAIL` - Email for notifications
- `PASS` - Email app password
- `NEXT_BASE_URL` - Frontend URL (default: http://localhost:3000)
- `NEXT_PUBLIC_SOCKET_SERVER` - Socket server URL (default: http://localhost:4000)

**Backend (`socketServer/.env`):**

Copy `.env.example` to `.env`:

```bash
cp .env.example .env
```

Required variables:
- `NEXT_BASE_URL` - Frontend URL
- `PORT` - Server port (default: 4000)

### 4. Run the application

**Start the Socket Server (Terminal 1):**
```bash
cd socketServer
npm run dev
```

**Start the Next.js App (Terminal 2):**
```bash
cd 1.snapcart
npm run dev
```

The application will be available at:
- Frontend: http://localhost:3000
- Socket Server: http://localhost:4000

## 🔧 Available Scripts

### Frontend (1.snapcart)
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm start` - Start production server
- `npm run lint` - Run ESLint

### Backend (socketServer)
- `npm run dev` - Start development server with nodemon

## 📦 Tech Stack

### Frontend
- **Framework:** Next.js 16 with React 19
- **Styling:** Tailwind CSS 4
- **State Management:** Redux Toolkit
- **Authentication:** NextAuth 5
- **Maps:** Leaflet & React Leaflet
- **Animations:** Framer Motion
- **Charts:** Recharts
- **HTTP Client:** Axios
- **Real-time:** Socket.io Client

### Backend
- **Runtime:** Node.js
- **Framework:** Express 5
- **Database:** MongoDB with Mongoose
- **Real-time:** Socket.io
- **Environment:** dotenv

## 🔐 Security Notes

- Never commit `.env` or `.env.local` files to version control
- Keep your API keys and secrets secure
- Use environment variables for all sensitive data
- Rotate secrets regularly

## 📝 License

This project is private and proprietary.

## 🤝 Contributing

Please contact the project maintainer for contribution guidelines.

## 📧 Support

For questions or issues, please open an issue in the GitHub repository.
