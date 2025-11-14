Optima IDP/ 
├── README.md
├── .gitignore
├── docs/
│   ├── architecture-diagram.png
│   ├── api-spec.md
│   ├── system-design.md
│   ├── db-schema.md
│   └── ml-model-notes.md
│
├── frontend/                     # ReactJS App (UI)
│   ├── package.json
│   ├── public/
│   └── src/
│       ├── index.js
│       ├── App.jsx
│       ├── pages/
│       │   ├── Login.jsx
│       │   ├── EmployeeDashboard.jsx
│       │   ├── ManagerDashboard.jsx
│       │   ├── AdminPanel.jsx
│       │   └── NotFound.jsx
│       ├── components/
│       │   ├── Navbar.jsx
│       │   ├── Sidebar.jsx
│       │   ├── SkillCard.jsx
│       │   ├── ResourceCard.jsx
│       │   └── RecommendationList.jsx
│       ├── hooks/
│       ├── utils/
│       │   └── calculateSkillGap.js
│       ├── services/
│       │   └── api.js            # Axios instance + API routes
│       ├── context/
│       │   └── AuthContext.jsx   # Global Auth
│       └── assets/
│
├── backend/                       # NodeJS Express API
│   ├── package.json
│   ├── server.js
│   ├── config/
│   │   ├── db.js
│   │   └── env.js
│   ├── routes/
│   │   ├── auth.routes.js
│   │   ├── user.routes.js
│   │   ├── skill.routes.js
│   │   ├── resource.routes.js
│   │   ├── performance.routes.js
│   │   └── idp.routes.js
│   ├── controllers/
│   │   ├── auth.controller.js
│   │   ├── user.controller.js
│   │   ├── skill.controller.js
│   │   ├── resource.controller.js
│   │   ├── performance.controller.js
│   │   └── idp.controller.js
│   ├── models/
│   │   ├── User.js
│   │   ├── Skill.js
│   │   ├── Resource.js
│   │   ├── PerformanceReport.js
│   │   └── IDP.js
│   ├── middleware/
│   │   ├── authMiddleware.js
│   │   └── roleMiddleware.js
│   ├── utils/
│   │   ├── token.js
│   │   ├── logger.js
│   │   └── apiResponse.js
│   └── services/
│       └── recommender.service.js   # Calls Python ML service
│
├── recommender/                  # Python FastAPI ML Service
│   ├── main.py
│   ├── requirements.txt
│   ├── routers/
│   │   └── recommend.py
│   ├── core/
│   │   ├── skill_similarity.py
│   │   ├── resource_ranker.py
│   │   └── preprocessing.py
│   ├── models/
│   │   └── model.pkl            # Optional ML model file
│   └── data/
│       └── skills.json
│
├── scripts/
│   ├── seedSkills.js
│   ├── seedResources.js
│   └── exportReports.js
│
├── docker-compose.yml            # Optional
└── .env.example
