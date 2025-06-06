# SkyLine

[![Node.js](https://img.shields.io/badge/Node.js-v18+-green.svg)](https://nodejs.org/)
[![Express.js](https://img.shields.io/badge/Express.js-v4.19.2-blue.svg)](https://expressjs.com/)
[![MySQL](https://img.shields.io/badge/MySQL-v8+-blue.svg)](https://www.mysql.com/)
[![License: ISC](https://img.shields.io/badge/License-ISC-yellow.svg)](https://opensource.org/licenses/ISC)

A robust document scanning and analysis server that provides plagiarism detection, text analysis, and document management capabilities.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Folder Structure](#folder-structure)
- [Technologies Used](#technologies-used)
- [License](#license)
- [Support](#support)

## Features

### 🔍 Plagiarism & AI Detection

- Advanced content matching with detailed similarity reports
- AI-generated text identification with confidence scoring
- Support for multiple document formats
- Real-time scanning and analysis

### ✍️ Proofreading & Editing

- Grammar, spelling, and style checking
- Academic writing standards compliance
- Citation format verification
- Document structure optimization

### 📚 Assignment Aid

- Research and writing assistance
- Citation management
- Topic analysis and outlining
- Quality assurance checks

### 🎓 Additional Features

- Live tutoring with expert assistance
- Secure document management
- Version control and tracking
- Multi-format file support
- Real-time collaboration tools

## Installation

### Backend Setup

1. Clone the repository:

```bash
git clone https://github.com/WaqasKhan4842/Staging-Server.git
cd Staging-Server
```

2. Install backend dependencies:

```bash
cd skyline_backend-main
npm install
```

3. Set up environment variables:
   Create a `.env` file in the backend directory with the following variables:

```env
DB_HOST=your_database_host
DB_USER=your_database_user
DB_PASSWORD=your_database_password
DB_NAME=your_database_name
JWT_SECRET=your_jwt_secret
STRIPE_SECRET_KEY=your_stripe_secret
OPENAI_API_KEY=your_openai_api_key
```

4. Set up the database:

- Ensure MySQL is installed and running
- Create a database with the name specified in your .env file
- The tables will be created automatically when you run the server

### Frontend Setup

1. Navigate to the frontend directory:

```bash
cd ../skyline_frontend-main
```

2. Install frontend dependencies:

```bash
npm install
```

3. Set up environment variables (if needed):
   Create a `environment.ts` file in the `src/environments` directory:

```typescript
export const environment = {
  production: false,
  apiUrl: "http://localhost:4000/api",
  // Add other environment variables as needed
};
```

## Usage

### Starting the Services

1. Start the backend server:

```bash
cd skyline_backend-main
npm start
```

The backend server will run at `http://localhost:4000`

2. Start the frontend development server:

```bash
cd skyline_frontend-main
ng serve
```

The frontend application will be available at `http://localhost:4200`

### Accessing the Application

- Frontend Application: http://localhost:4200
- Backend API: http://localhost:4000

## Folder Structure

### Backend Structure

```
skyline_backend-main/
├── src/
│   ├── controllers/    # Business logic
│   ├── routes/         # API routes
│   ├── middleware/     # Custom middleware
│   ├── db/            # Database configuration
│   ├── utils/         # Utility functions
│   └── config/        # Configuration files
├── uploads/           # File upload directory
├── ScanDoc/          # Scanned documents
├── index.js          # Main application file
└── package.json      # Project dependencies
```

### Frontend Structure

```
skyline_frontend-main/
├── src/
│   ├── app/
│   │   ├── components/     # Reusable UI components
│   │   │   ├── plagiarism/    # Plagiarism detection components
│   │   │   ├── ai-detection/  # AI detection components
│   │   │   ├── proofreading/  # Proofreading components
│   │   │   └── assignment/    # Assignment aid components
│   │   ├── services/      # API and business services
│   │   ├── models/        # Data models and interfaces
│   │   ├── guards/        # Route guards
│   │   └── shared/        # Shared utilities and components
│   ├── assets/           # Static files (images, fonts, etc.)
│   ├── environments/     # Environment configurations
│   └── styles/          # Global styles and themes
├── angular.json         # Angular configuration
├── package.json         # Project dependencies
└── tsconfig.json        # TypeScript configuration
```

## Technologies Used

- **Backend Framework**: Express.js
- **Database**: MySQL
- **Authentication**: JWT
- **File Processing**:
  - Tesseract.js (OCR)
  - pdf-lib
  - mammoth (Word processing)
  - xlsx (Excel processing)
- **Cloud Services**:
  - Google Drive API
  - OpenAI API
- **Payment Processing**: Stripe
- **Other Tools**:
  - Nodemailer (Email)
  - Puppeteer (Web scraping)
  - QRCode generation
  - Natural language processing

## License

This project is licensed under the ISC License.
