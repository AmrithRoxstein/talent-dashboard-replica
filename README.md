# Talent Dashboard Replica

A comprehensive fullstack replica of the **AppViewX Talent Acquisition Dashboard** with React frontend, Express.js backend, and PostgreSQL database. This project demonstrates modern web development practices and can be extended for real-world recruitment management applications.

## 🎯 Features

### Frontend
- **Interactive Dashboard** with real-time metrics and KPIs
- **Hiring Funnel Charts** showing recruitment pipeline progression
- **Position Overview Table** with filters and search functionality
- **Talent Source Analytics** tracking candidate origins
- **University Recruiting Section** with campus hiring timeline
- **Process Flow Visualization** with swim lane diagrams
- **Responsive Design** with Tailwind CSS
- **Component-based Architecture** for easy maintenance and scaling

### Backend
- **RESTful API** with Express.js
- **Database Schema** with PostgreSQL and Prisma ORM
- **Authentication & Authorization** with JWT
- **Data Validation** and error handling
- **CORS Support** for cross-origin requests
- **Modular Route Structure** for scalability

### Database
- **Positions Table** - Job openings and requisitions
- **Candidates Table** - Candidate profiles and tracking
- **Pipeline Events** - Hiring process milestones
- **Metrics** - Performance KPIs and analytics
- **Users Table** - TA team members and hiring managers
- **Campus Programs** - University recruiting data

## 📁 Project Structure

```
talent-dashboard-replica/
├── frontend/                    # React frontend
│   ├── src/
│   │   ├── components/         # Reusable UI components
│   │   │   ├── Dashboard/
│   │   │   ├── Process/
│   │   │   └── Navigation/
│   │   ├── pages/              # Page components
│   │   ├── hooks/              # Custom React hooks
│   │   ├── context/            # Context API for state
│   │   └── styles/             # Tailwind CSS
│   ├── package.json
│   └── vite.config.js
│
├── backend/                     # Express backend
│   ├── src/
│   │   ├── routes/             # API endpoints
│   │   ├── controllers/        # Business logic
│   │   ├── models/             # Prisma models
│   │   ├── middleware/         # Auth, validation
│   │   ├── db/                 # Database initialization
│   │   └── server.js           # Entry point
│   ├── prisma/
│   │   └── schema.prisma       # Database schema
│   ├── package.json
│   └── .env.example
│
├── README.md
├── .gitignore
├── LICENSE
└── docker-compose.yml          # Local deployment
```

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- PostgreSQL 12+
- npm or yarn

### Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

The frontend will be available at `http://localhost:5173`

### Backend Setup

```bash
cd backend
npm install
cp .env.example .env
# Update DATABASE_URL in .env
npm run dev
```

The backend will be available at `http://localhost:3000`

### Database Setup

```bash
cd backend
npx prisma migrate dev
npx prisma db seed
```

## 🔌 API Endpoints

### Dashboard
- `GET /api/dashboard/metrics` - Fetch key performance metrics
- `GET /api/dashboard/positions` - Get open positions list
- `GET /api/dashboard/charts/hiring-funnel` - Hiring funnel data
- `GET /api/dashboard/charts/quarterly-trend` - Quarterly hiring trends

### Positions
- `GET /api/positions` - List all positions
- `POST /api/positions` - Create new position
- `PUT /api/positions/:id` - Update position
- `DELETE /api/positions/:id` - Delete position

### Candidates
- `GET /api/candidates` - List all candidates
- `POST /api/candidates` - Add new candidate
- `PUT /api/candidates/:id` - Update candidate status
- `GET /api/candidates/source/analytics` - Source analytics

## 🛠️ Technology Stack

**Frontend**
- React 18
- Vite
- Tailwind CSS
- Recharts for visualizations
- Radix UI for accessible components
- Zustand for state management
- TanStack Query for data fetching
- Axios for HTTP requests

**Backend**
- Express.js 4
- Node.js
- PostgreSQL
- Prisma ORM
- JWT for authentication
- Helmet for security
- CORS for cross-origin requests

**Database**
- PostgreSQL 12+
- Prisma Client

## 📊 Database Schema

Key tables include:
- **users** - TA team members and hiring managers
- **positions** - Open job positions
- **candidates** - Candidate records
- **pipeline_events** - Interview stages and milestones
- **metrics** - KPI tracking
- **campus_program** - University recruiting data
- **talent_source** - Candidate source tracking

## 🔐 Authentication

The API uses JWT tokens for authentication:

```bash
POST /api/auth/login
{
  "email": "user@example.com",
  "password": "password"
}
```

Include the token in subsequent requests:
```bash
Authorization: Bearer <token>
```

## 🧪 Testing

```bash
cd backend
npm test
```

## 🐳 Docker Deployment

```bash
docker-compose up
```

## 📝 Environment Variables

Create a `.env` file in the backend directory:

```env
DATABASE_URL="postgresql://user:password@localhost:5432/talent_db"
JWT_SECRET="your-secret-key"
NODE_ENV="development"
PORT=3000
FRONTEND_URL="http://localhost:5173"
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🎓 Learning Resources

- [React Documentation](https://react.dev)
- [Express.js Guide](https://expressjs.com)
- [Prisma Documentation](https://www.prisma.io/docs)
- [Tailwind CSS](https://tailwindcss.com)
- [PostgreSQL Documentation](https://www.postgresql.org/docs)

## 🤖 LLM Integration Ideas

This project can be extended with AI capabilities:

1. **Smart Resume Parsing** - Use LLMs to extract candidate information
2. **Automated Screening** - AI-powered candidate assessment
3. **Talent Recommendations** - ML models for best candidate matches
4. **Interview Insights** - NLP for interview transcript analysis
5. **Conversational Analytics** - Chat-based dashboard queries

## 📞 Support

For issues and questions, please open an issue in the repository.

---

**Made with ❤️ by AmrithRoosstein**
