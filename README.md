# PPL C5 Backend - Medical Equipment Management System

A robust backend API for managing medical equipment, maintenance requests, spare parts, and calibration history. Built with Node.js, Express, TypeScript, and Prisma ORM.

## 🏥 Project Overview

This backend system provides comprehensive management capabilities for medical equipment including:
- **Equipment Management**: Track medical devices with inventory details
- **Maintenance Requests**: Handle maintenance and calibration requests
- **Spare Parts Management**: Manage spare parts inventory and usage
- **User Management**: Role-based access control with division management
- **Notification System**: Real-time notifications for request updates
- **Reporting**: Generate reports for equipment and maintenance activities

## 🚀 Features

- **Authentication & Authorization**: JWT-based authentication with role-based access
- **Database Management**: MySQL database with Prisma ORM
- **API Documentation**: Auto-generated OpenAPI documentation
- **Security**: Helmet.js security headers, CORS protection, rate limiting
- **Error Monitoring**: Sentry integration for error tracking
- **Testing**: Jest testing framework with unit and integration tests
- **Code Quality**: Prettier formatting, Husky pre-commit hooks
- **Docker Support**: Containerized deployment

## 🛠️ Tech Stack

- **Runtime**: Node.js 22
- **Framework**: Express.js
- **Language**: TypeScript
- **Database**: MySQL
- **ORM**: Prisma
- **Authentication**: JWT
- **Security**: Helmet.js, CORS
- **Testing**: Jest
- **Documentation**: Express OAS Generator
- **Monitoring**: Sentry
- **Containerization**: Docker

## 📋 Prerequisites

- Node.js 22 or higher
- MySQL database
- npm or yarn package manager

## 🔧 Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd PPL-C5-BACKEND
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Setup**
   Create a `.env` file in the root directory with the following variables:
   ```env
   DATABASE_URL="mysql://username:password@localhost:3306/database_name"
   JWT_SECRET_KEY="your-jwt-secret-key"
   PROD_CLIENT_URL="http://localhost:3000"
   WHATSAPP_API_URL="your-whatsapp-api-url"
   WHATSAPP_API_KEY="your-whatsapp-api-key"
   PORT=8000
   ```

4. **Database Setup**
   ```bash
   # Generate Prisma client
   npx prisma generate
   
   # Run database migrations
   npx prisma migrate dev
   ```

## 🚀 Running the Application

### Development Mode
```bash
npm run dev
```

### Production Mode
```bash
npm start
```

### Testing
```bash
# Run all tests
npm test

# Run unit tests only
npm run test:unit

# Run integration tests only
npm run test:integration
```

### Code Quality
```bash
# Check code formatting
npm run lint

# Format code
npx prettier --write 'src/**/*.{js,ts}'
```

## 🐳 Docker Deployment

1. **Build the Docker image**
   ```bash
   docker build -t ppl-c5-backend .
   ```

2. **Run the container**
   ```bash
   docker run -p 8000:8000 \
     -e DATABASE_URL="your-database-url" \
     -e JWT_SECRET_KEY="your-jwt-secret" \
     -e PROD_CLIENT_URL="your-client-url" \
     ppl-c5-backend
   ```

## 📚 API Endpoints

### Authentication
- `POST /auth/login` - User login
- `POST /auth/register` - User registration

### Users
- `GET /user` - Get all users
- `GET /user/:id` - Get user by ID
- `PUT /user/:id` - Update user
- `DELETE /user/:id` - Delete user

### Medical Equipment
- `GET /medical-equipment` - Get all equipment
- `POST /medical-equipment` - Create new equipment
- `GET /medical-equipment/:id` - Get equipment by ID
- `PUT /medical-equipment/:id` - Update equipment
- `DELETE /medical-equipment/:id` - Delete equipment

### Maintenance History
- `GET /medical-equipment/maintenance` - Get maintenance history
- `POST /medical-equipment/maintenance` - Create maintenance record

### Calibration History
- `GET /medical-equipment/calibration` - Get calibration history
- `POST /medical-equipment/calibration` - Create calibration record

### Spare Parts
- `GET /spareparts` - Get all spare parts
- `POST /spareparts` - Create new spare part
- `GET /spareparts/:id` - Get spare part by ID
- `PUT /spareparts/:id` - Update spare part
- `DELETE /spareparts/:id` - Delete spare part

### Requests
- `GET /request` - Get all requests
- `POST /request` - Create new request
- `GET /request/:id` - Get request by ID
- `PUT /request/:id` - Update request
- `DELETE /request/:id` - Delete request

### Comments
- `GET /comment` - Get all comments
- `POST /comment` - Create new comment
- `GET /comment/:id` - Get comment by ID
- `PUT /comment/:id` - Update comment
- `DELETE /comment/:id` - Delete comment

### Reports
- `GET /report` - Generate reports

### Notifications
- `GET /notification` - Get notifications
- `PUT /notification/:id` - Mark notification as read

## 🗄️ Database Schema

The application uses the following main entities:

- **User**: User accounts with role-based access
- **ListDivisi**: Division/Department management
- **MedicalEquipment**: Medical device inventory
- **Spareparts**: Spare parts inventory
- **Request**: Maintenance and calibration requests
- **MaintenanceHistory**: Equipment maintenance records
- **CalibrationHistory**: Equipment calibration records
- **PartsHistory**: Spare parts usage history
- **Comment**: Request comments
- **Notifikasi**: User notifications

## 🔒 Security Features

- **Helmet.js**: Security headers protection
- **CORS**: Cross-origin resource sharing configuration
- **Rate Limiting**: Request rate limiting
- **Input Validation**: Express-validator for request validation
- **JWT Authentication**: Secure token-based authentication
- **Password Hashing**: bcrypt for password security

## 🧪 Testing

The project includes comprehensive testing with Jest:

- **Unit Tests**: Test individual functions and components
- **Integration Tests**: Test API endpoints and database interactions
- **Coverage Reports**: Code coverage analysis

## 📊 Monitoring

- **Sentry Integration**: Error tracking and performance monitoring
- **Logging**: Comprehensive application logging

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the ISC License.

## 👥 Team

PPL C5 Backend Development Team

## 📞 Support

For support and questions, please contact the development team or create an issue in the repository.
