# Mail Tracker

A comprehensive email management and tracking application that helps you manage, track, and automate your email workflows with AI-powered features.

## Features

✅ **Gmail Integration** - Connect and manage your Gmail account directly  
✅ **Email Tracking** - Track email opens, replies, and engagement  
✅ **Draft Management** - Create, save, and manage email drafts  
✅ **AI-Powered Replies** - Generate intelligent email responses using AI  
✅ **Follow-up Reminders** - Automatic reminders for important emails  
✅ **User Authentication** - Secure login with O-auth 2.0    
✅ **Cloud Storage Integration** - Cloudinary for file management    
✅ **Logging & Analytics** - Comprehensive activity logging and insights

## Tech Stack

### Backend

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: MongoDB
- **Authentication**: JWT + OTP
- **Email Service**: Gmail API, NodeMailer
- **AI Integration**: Google Gemini API
- **File Upload**: Cloudinary
- **File Handling**: Multer
- **Task Scheduling**: Node Cron

### Frontend

- **Framework**: React 18
- **Build Tool**: Vite
- **Styling**: Tailwind CSS
- **HTTP Client**: Axios
- **Routing**: React Router
- **State Management**: React Context API
- **ESLint**: Code quality

## Project Structure

```
mail-tracker/
├── mail-tracker-api/          # Backend API
│   ├── app/
│   │   ├── config/           # Configuration files (MongoDB, Gmail, Gemini, etc.)
│   │   ├── controllers/      # Route controllers
│   │   ├── models/           # MongoDB schemas
│   │   ├── routes/           # API endpoints
│   │   ├── services/         # Business logic
│   │   ├── middleware/       # Authentication, file upload
│   │   ├── cron/             # Scheduled tasks
│   │   └── connection.js     # Database connection
│   ├── common/               # Shared utilities
│   ├── constants/            # Constants and enums
│   ├── middleware/           # Global middleware
│   └── server.js             # Application entry point
│
├── mail-tracker-ui/          # Frontend React App
│   ├── src/
│   │   ├── components/       # Reusable components
│   │   ├── pages/           # Page components
│   │   ├── layouts/         # Layout wrappers
│   │   ├── context/         # React Context
│   │   ├── utils/           # Utility functions & API config
│   │   ├── assets/          # Images, icons
│   │   ├── styles/          # Global styles
│   │   └── main.jsx         # Application entry point
│   ├── public/              # Static files
│   ├── index.html           # HTML template
│   └── vite.config.js       # Vite configuration
│
└── README.md                # This file
```

## Installation

### Prerequisites

- Node.js (v14 or higher)
- MongoDB (local or Atlas)
- Gmail API credentials
- Google Gemini API key
- Cloudinary account (for file uploads)

### Backend Setup

1. Navigate to the backend directory:

```bash
cd mail-tracker-api
```

2. Install dependencies:

```bash
npm install
```

3. Create a `.env` file in the `mail-tracker-api` directory with the following variables:

```
PORT=5000
MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
GOOGLE_CLIENT_ID=your_gmail_client_id
GOOGLE_CLIENT_SECRET=your_gmail_client_secret
GOOGLE_REDIRECT_URI=your_redirect_uri
GEMINI_API_KEY=your_gemini_api_key
CLOUDINARY_CLOUD_NAME=your_cloudinary_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_secret
NODEMAILER_EMAIL=your_email
NODEMAILER_PASSWORD=your_app_password
```

4. Start the backend server:

```bash
npm start
```

The server will run on `http://localhost:5000`

### Frontend Setup

1. Navigate to the frontend directory:

```bash
cd mail-tracker-ui
```

2. Install dependencies:

```bash
npm install
```

3. Create a `.env` file in the `mail-tracker-ui` directory:

```
VITE_API_BASE_URL=http://localhost:5000
```

4. Start the development server:

```bash
npm run dev
```

The application will be available at `http://localhost:5173`

## Available Scripts

### Backend

- `npm start` - Start the production server
- `npm run dev` - Start with nodemon for development

### Frontend

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint


## Usage

1. **Sign Up/Login** - Create an account or log in
2. **Connect Gmail** - Authorize your Gmail account
3. **Manage Emails** - View, track, and manage emails
4. **Create Drafts** - Write and save email drafts
5. **Set Follow-ups** - Schedule follow-up reminders
6. **Use AI Replies** - Generate smart email responses
7. **View Analytics** - Check engagement metrics and logs

## Environment Configuration

All configuration files are located in `mail-tracker-api/app/config/`:

- `mongodb.js` - Database connection
- `google.js` - Gmail & OAuth setup
- `gemini.js` - AI integration
- `cloudinary.js` - File upload service
- `nodeMailer.js` - Email service

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For issues, questions, or suggestions, please open an issue on the GitHub repository.

---
