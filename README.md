# Secure-E-Voting-Platform
A secure and scalable online voting platform built with the MERN stack (MongoDB, Express, React, Node.js).


A full-stack implementation of an electronic voting system that lets authorised voters cast ballots online, while providing roles for administrators, secure authentication, and vote tallying.

Description
This platform enables voters to register, login, and vote in an election via a web interface. Administrators can create elections, define candidates, view results. The system enforces that each voter votes only once per election, and uses encrypted storage of vote data. The design emphasises security, auditability, and ease of deployment for small-to-medium election scenarios.

Features
Administrator dashboard to manage elections, candidates, voters.
Voter registration and authentication (sign up / login).
Role-based access: separate views and permissions for amin and voter.
Each election has its candidate list, voting period.
Voter casts one vote per election; system ensures no duplicate votes.
Secure backend storage of vote data (for example using encryption/hashing).
Results are calculated and displayed after the election closes.
Responsive front-end UI for ease of use.

Technologies Used
Front-end: JavaScript, React (or other modern JS framework)
Back-end: Node.js with Express (or another server framework)
Database: MongoDB (or other NoSQL / SQL)
Authentication: JWT / token-based sessions
Security: bcrypt for password hashing, AES (or similar) for vote data encryption
UI libraries: Bootstrap or Material UI for responsive design
Other: API endpoints, role middleware, voter / admin flows
(Adjust the above list to reflect the exact technologies used in the repo.)

Installation
Clone the repository
git clone https://github.com/PrathvirajGawali/Secure-E-Voting-Platform.git
cd Secure-E-Voting-Platform

Install backend dependencies
cd server
npm install

Install front-end dependencies
cd ../client
npm install

Set up environment variables in .env (example):
PORT=5000
MONGO_URI=<your_mongo_connection_string>
JWT_SECRET=<a_secret_key>

Start the backend server
npm run start

Start the front-end development server
cd client
npm start
Open browser at http://localhost:3000 (or whichever port) to use the application.

Usage
As an administrator:
Login with admin credentials (create one if first run).
Create a new election: specify title, description, candidate list, start & end date/time.
View list of registered voters; approve or add new ones.
After election ends, open result page to view vote counts and determine winner.

As a voter:
Register by providing basic details (name, email, etc.).
Login and view active elections.
Select an election, view the candidate list, and cast your vote.
After completion you may see that your vote is recorded (depending on implementation).
You cannot vote again in the same election.

Folder Structure
Secure-E-Voting-Platform/
├── server/                     # backend code (Node.js / Express)
│   ├── models/                 # database models (User, Election, Vote, Candidate)
│   ├── routes/                 # API routes for auth, election, vote
│   ├── middleware/             # JWT auth, role checks
│   ├── controllers/            # business logic
│   ├── config/                 # database connection, env variables
│   └── server.js               # entry point
├── client/                     # front-end code (React)
│   ├── src/
│   │   ├── components/         # UI components (AdminDashboard, VoterDashboard, etc)
│   │   ├── pages/              # routes / views
│   │   └── utils/              # helper functions (API calls, auth)
│   ├── public/
│   └── package.json
├── README.md                   # project overview and instructions
└── .env.example                # sample environment variables

Future Enhancements
Deploy to production environment (setup process, SSL, domain).
Integrate blockchain or immutable ledger for vote audit trail.
Add biometric or multi-factor authentication for voters.
Mobile-first UI / offline support for remote polling stations.
Real-time notifications or live result updates.
Improve UI/UX with multilingual support.
