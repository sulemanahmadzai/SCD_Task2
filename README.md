# Staging-Server

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

- **Document Scanning & Analysis**
  - PDF parsing and text extraction
  - Document format conversion
  - OCR capabilities using Tesseract.js
  - Plagiarism detection
- **Authentication & Authorization**
  - JWT-based authentication
  - Role-based access control
- **File Management**
  - Multi-format file upload support
  - Google Drive integration
  - File conversion and processing
- **Payment Integration**
  - Stripe payment processing
  - Order management
- **AI Integration**

  - OpenAI API integration
  - Natural language processing capabilities

- **Additional Features**
  - Email notifications
  - Interactive reporting
  - QR code generation
  - PDF manipulation and generation

## Installation

1. Clone the repository:

```bash
git clone <repository-url>
cd Staging-Server
```

2. Install dependencies:

```bash
cd skyline_backend-main
npm install
```

3. Set up environment variables:
   Create a `.env` file in the root directory with the following variables:

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

## Usage

1. Start the development server:

```bash
npm start
```

2. The server will be running at `http://localhost:4000`

3. API Endpoints:

- `/api/scan` - Document scanning endpoints
- `/api/user` - User management
- `/api/order` - Order processing
- `/api/payment` - Payment processing
- `/interactive-report` - Report generation
- `/api/google-drive` - Google Drive integration

## Folder Structure

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

## Support

For support, please contact the development team or create an issue in the repository.

---

© 2024 Skyline Staging Server. All rights reserved.
