# crunch-debate

## Frontend

**01 - Project Initialization**

- Create React app: `npx create-react-app client`
- Install dependencies: `npm install redux react-redux axios socket.io-client material-ui`

**02 - Directory Structure and Components**:

- `components`: Reusable UI components (e.g., Navbar, Footer, DebateCard)
- `pages`: Main application pages (e.g., Home, DebateDetail, CreateDebate, Login, Register)
- `services`: API services for interacting with the backend
- `utils`: Utility functions and constants

**03 - State Management**:
- Configure Redux store and slices for authentication, debates, comments, etc.

**04 - Routing**:
- Set up React Router for navigation between pages.

**05 - UI/UX**:
- Implement Material-UI for consistent styling and responsive design.

**06 - Integration with Video Conferencing APIs**:
- Create services to interact with Zoom and Google Meet APIs for creating and managing meetings.


## Backend (Server)


**01 - Project Initialization**:

- Initialize Node.js project: `npm init -y`
- Install dependencies: `npm install express mongoose dotenv bcryptjs jsonwebtoken socket.io axios`

**Directory Structure**:
- `models`: Mongoose schemas (User, Debate, Comment, Vote)
- `controllers`: Logic for handling routes (auth, debates, comments, votes)
- `routes`: API endpoints (authRoutes, debateRoutes, commentRoutes, voteRoutes)
- `middleware`: Middleware functions (auth, error handling)
- `utils`: Utility functions (generateToken, email service)


**Authentication**:
- Implement JWT authentication for user login/register.
- Set up OAuth for Google and Zoom integration.

**Database**:
- Define Mongoose schemas and models.
- Connect to MongoDB using Mongoose.

**Real-time Communication**:
- Integrate Socket.io for real-time chat and voting during debates.

**API Endpoints**:
- **Auth Routes**: Register, Login, OAuth
- **Debate Routes**: Create, Update, Get Debates, Join Debate
- **Comment Routes**: Add Comment, Get Comments
- **Vote Routes**: Cast Vote, Get Vote Results

**Video Conferencing Integration**:
- Use Axios to interact with Zoom and Google Meet APIs.
- Schedule and manage video meetings, generate join links.


## Deployment and Maintenance

- **Frontend**: Deploy React app to Render, Heroku or AWS S3 + CloudFront.
- **Backend**: Deploy Node.js server to Render, Heroku,  AWS EC2, or similar.
- Use Docker for containerization and ease of deployment.

**CI/CD**:
- Set up GitHub Actions for automated testing and deployment.

**Environment Variables**:
- Use `.env` file to manage sensitive configuration details (API keys, database URI).

**Monitoring and Maintenance**:
- Use tools like New Relic or LogRocket for monitoring performance and errors.
- Regularly update dependencies and perform security audits.


## Detailed User Flow

**User Registration/Login**:
- **Frontend**: Form validation, API calls to backend, JWT handling.
- **Backend**: User model, JWT generation, password hashing.

**Creating a Debate**:
- **Frontend**: Form to input debate details, call to backend to create debate.
- **Backend**: Store debate details in database, generate meeting link via Zoom/Google Meet API.


**Joining a Debate**:
- **Frontend**: Display list of available debates, join link button.
- **Backend**: Validate user role (pro/con), provide meeting link.

**Voting and Commenting**:
- **Frontend**: Real-time updates via Socket.io for votes and comments.
- **Backend**: Store votes and comments, update debate status.

**Moderation**:
- **Frontend**: Moderator dashboard, actions for managing debates and users.
- **Backend**: Middleware for role-based access control, endpoints for managing content.

## Folder Project structure
```
/debate-platform
├── /client
│   ├── /public
│   ├── /src
│   │   ├── /assets
│   │   ├── /components
│   │   ├── /pages
│   │   ├── /services
│   │   ├── /utils
│   │   └── App.js
│   └── package.json
├── /server
│   ├── /config
│   ├── /controllers
│   ├── /middleware
│   ├── /models
│   ├── /routes
│   ├── /utils
│   ├── server.js
│   └── package.json
├── /scripts
├── .env
├── .gitignore
├── README.md
└── package.json
```

## Technologies Used

- **Frontend**: `React.js, Redux (state management), Material-UI (UI components), `
- **Axios** `(HTTP requests), react-google-login`
- **Backend**: `Node.js, Express.js, Passport.js`
- **Database**: `MongoDB, Mongoose (ORM)`
- **Real-time Communication:** `Socket.io`
- **Authentication**: `JWT (JSON Web Tokens), OAuth (Google SSO)`
- **Video Conferencing:** `Zoom API, Google Meet API`
- **Deployment**: `Heroku/AWS/React`
- **Testing**: `Jest, Enzyme (frontend), Mocha, Chai (backend)`
- **DevOps**: `Docker, CI/CD (GitHub Actions)`



