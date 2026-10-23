# 🐾 Animal Rescue & Welfare Platform

Full-stack web application designed to connect citizens, volunteers, and non-governmental organizations (NGOs) to improve the response to animal emergencies. The platform enables users to report injured or distressed animals, share incident locations, track rescue progress, and coordinate response efforts through dedicated volunteer and NGO interfaces.

The project aims to make animal rescue reporting more accessible and help rescue organizations manage incidents in a centralized digital environment.

## 📌 About the Project

Animal emergencies often go unreported or receive delayed assistance because people may not know whom to contact. Communication gaps between citizens, volunteers, and rescue organizations can also make it difficult to assign responsibilities and track the progress of reported incidents.

Addresses these challenges by providing a shared platform for reporting incidents, coordinating rescue activities, and monitoring case status.

## 🎯 Objectives

- Simplify the reporting of animal-related emergencies.
- Connect citizens with volunteers and animal welfare organizations.
- Support the assignment and management of rescue incidents.
- Enable users to track the progress of reported cases.
- Provide NGOs with centralized incident management and analytics.
- Use location-based information to support coordinated rescue efforts.

## ✨ Key Features

### 👥 Citizen Features

- Report animal emergencies with incident details.
- Upload photographs of animals requiring assistance.
- Provide location information for reported incidents.
- Track the status of submitted reports.
- Access a centralized interface for reporting and monitoring incidents.

### 🦺 Volunteer Features

- Access a dedicated volunteer interface.
- View and manage rescue tasks.
- Assign incidents to themselves for resolution.
- Create new incident reports when necessary.
- Coordinate rescue activities through incident status updates.

### 🏢 NGO Management

- View reported incidents across the relevant service area.
- Manage incident records and response workflows.
- Update incident statuses, including Pending, In Process, and Resolved.
- View incident statistics and analytics.
- Visualize incident locations on a map.
- Coordinate volunteer responses to reported emergencies.

### 🐕 Animal Records

The backend includes dedicated pet-related API routes for animal record management. These routes provide a foundation for extending the platform's animal welfare functionality.

### 📍 Location-Based Incident Visualization

The application includes a map-based interface for displaying incident locations, helping users and organizations understand where assistance is required.

### 🔐 Authentication and Access

- User authentication and account management.
- JWT-based authentication support.
- Password hashing using bcrypt.
- Cookie handling for authentication-related workflows.
- Separate route groups for users, volunteers, NGOs, incidents, and pet records.

### 📄 DocuSign Integration

The backend includes a dedicated DocuSign integration route for document-related workflows.

## 🛠️ Technology Stack

| Component | Technologies |
|---|---|
| Frontend | React.js |
| Styling | Tailwind CSS, DaisyUI |
| Mapping | Leaflet, React Leaflet |
| UI and animation | Material Tailwind, Heroicons, Framer Motion |
| HTTP requests | Axios |
| Routing | React Router |
| Backend | Node.js, Express.js |
| Database | MongoDB |
| ODM | Mongoose |
| Authentication | JSON Web Tokens (JWT) |
| Password hashing | bcrypt |
| File uploads | Multer |
| Document integration | DocuSign eSignature SDK |
| Development tools | Vite, Nodemon, npm |

## 🏗️ Project Architecture

The repository is organized into separate frontend and backend applications.

```text
animal-rescue/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── ...
│   ├── package.json
│   └── vite.config.js
│
├── backend/
│   ├── db/
│   │   └── ConnectDB.js
│   ├── Routes/
│   │   ├── userRoutes.js
│   │   ├── incidentRoutes.js
│   │   ├── NgoRoutes.js
│   │   ├── volunteerRoutes.js
│   │   ├── petRoutes.js
│   │   └── docuSignRoutes.js
│   ├── index.js
│   └── package.json
│
├── Contribution.md
├── LICENCE
└── README.md
```

*This is a simplified overview of the repository's structure.*

## 🔄 How It Works

1. A citizen identifies an animal requiring assistance.
2. The citizen submits an incident report with relevant details, photographs, and location information.
3. The incident becomes available through the platform's incident management workflow.
4. Volunteers can review incidents and assign tasks to themselves.
5. NGOs can monitor incidents and update their status.
6. Users can track reported incidents as rescue efforts progress.
7. NGOs can use the incident dashboard and map visualization to support coordination and review incident statistics.

## 🚀 Getting Started

### Prerequisites

Ensure the following tools are installed:

- [Node.js](https://nodejs.org/)
- npm
- [MongoDB](https://www.mongodb.com/) or a MongoDB Atlas connection
- [Git](https://git-scm.com/)

### 1. Clone the repository

```bash
git clone https://github.com/abhayvijayan/animal-rescue.git
cd animal-rescue
```

### 2. Configure the backend

Navigate to the backend directory and install the dependencies:

```bash
cd backend
npm install
```

Create a `.env` file inside the `backend` directory with the required configuration:

```env
PORT=3000
MONGO_URI=your_mongodb_connection_string
JWT_KEY=your_strong_secret_key
```

Replace the placeholder values with your own configuration.

Additional credentials may be required for integrations such as DocuSign. Check the relevant route implementation before configuring these services.

### 3. Start the backend

From the `backend` directory, run:

```bash
node index.js
```

The backend connects to MongoDB and starts the Express server on the configured port, defaulting to `3000`.

### 4. Configure and start the frontend

Open a separate terminal from the project root:

```bash
cd frontend
npm install
npm run dev
```

Vite will display the local development URL in the terminal, typically:

```text
http://localhost:5173
```

Open the URL in your browser to access the application.

### 5. Production build

To build the frontend for production:

```bash
cd frontend
npm run build
```

The build output is generated in the frontend's `dist` directory. The backend is configured to serve the built frontend when deployed together.

**Important:** Configure the frontend's API URL and the backend's CORS origins for your local environment or deployment. Keep credentials and API secrets out of version control.

## 🔐 Security Considerations

Before deploying the application for public use:

- Use strong secrets for JWT signing.
- Keep database credentials and third-party API credentials in environment variables.
- Verify user roles and permissions on protected backend routes.
- Ensure volunteers and NGOs can perform only authorized incident-management actions.
- Validate uploaded files and restrict permitted file types and sizes.
- Protect sensitive user and incident information.
- Configure production CORS origins carefully.
- Avoid exposing internal errors or sensitive information in API responses.

## 🔮 Future Enhancements

Potential improvements to the platform include:

- Real-time notifications for newly reported incidents.
- Automated assignment of incidents to nearby volunteers.
- Live rescue progress updates.
- Integration with veterinary clinics and animal shelters.
- Rescue history and reporting analytics.
- Improved mobile accessibility.
- Multilingual support.
- Expanded animal adoption and rehabilitation workflows.

## 🎓 Project Purpose

HopesAlive demonstrates how full-stack web development can be applied to a real-world social challenge. The project brings together frontend development, REST API design, database management, authentication, file uploads, and map-based visualization to support animal welfare initiatives.

It also provides a foundation for exploring how digital platforms can improve communication and coordination between citizens, volunteers, and organizations working to protect animals.

---

*HopesAlive — Connecting compassion with action to help animals in need.*
