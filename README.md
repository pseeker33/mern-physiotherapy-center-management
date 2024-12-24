# Medical Management System

A medical management system built with the MERN stack (MongoDB, Express, React, Node.js) focused on physiotherapy and rehabilitation centers.

## Features

- Patient management
- Medical history records
- Therapist management
- Appointment scheduling
- Dashboard with statistics

## Prerequisites

Before you begin, ensure you have installed:
- [Node.js](https://nodejs.org/) (v18 or higher)
- [MongoDB](https://www.mongodb.com/try/download/community)
- [Git](https://git-scm.com/)

## Project Structure

```
medical-management/
├── src/
│   ├── models/
│   │   ├── Patient.js
│   │   └── Therapist.js
│   ├── controllers/
│   │   ├── patientController.js
│   │   └── therapistController.js
│   ├── routes/
│   │   ├── patientRoutes.js
│   │   └── therapistRoutes.js
│   ├── middleware/
│   │   ├── auth.js
│   │   └── errorHandler.js
│   ├── config/
│   │   └── db.js
│   └── app.js
├── .env
├── .gitignore
└── README.md
```

## Installation

1. Clone the repository
```bash
git clone <repository-url>
cd medical-management
```

2. Install dependencies
```bash
npm install
```

3. Create `.env` file in the root directory with the following variables:
```env
MONGODB_URI=mongodb://localhost:27017/medical-management
PORT=5000
```

4. Start MongoDB service
```bash
# On Windows
net start MongoDB

# On macOS
brew services start mongodb-community

# On Linux
sudo systemctl start mongod
```

5. Run the development server
```bash
npm run dev
```

## API Endpoints

### Patients
- `GET /api/patients` - Get all patients
- `GET /api/patients/:id` - Get specific patient
- `POST /api/patients` - Create new patient
- `PUT /api/patients/:id` - Update patient
- `DELETE /api/patients/:id` - Delete patient
- `POST /api/patients/:id/medical-record` - Add medical record

### Therapists
- `GET /api/therapists` - Get all therapists
- `GET /api/therapists/:id` - Get specific therapist
- `POST /api/therapists` - Create new therapist
- `PUT /api/therapists/:id` - Update therapist
- `DELETE /api/therapists/:id` - Delete therapist

## API Request Examples

### Create Patient
```bash
POST /api/patients
Content-Type: application/json

{
  "firstName": "John",
  "lastName": "Doe",
  "dateOfBirth": "1990-01-01",
  "email": "john@example.com",
  "phone": "123456789"
}
```

### Add Medical Record
```bash
POST /api/patients/:id/medical-record
Content-Type: application/json

{
  "diagnosis": "Lower back pain",
  "treatment": "Physical therapy",
  "notes": "Patient shows improvement",
  "therapist": "therapistId"
}
```

## Development

To start the development server with hot-reload:
```bash
npm run dev
```

## Testing

```bash
npm test
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details

## Acknowledgments

- Based on modern MERN stack practices
- Inspired by healthcare management systems
