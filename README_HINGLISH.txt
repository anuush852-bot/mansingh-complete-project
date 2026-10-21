PRABHUBHAI VASAVA E-OFFICE BACKEND

1. Copy .env.example and rename the copy to .env.
2. In .env, change ADMIN_PASSWORD and JWT_SECRET (secret at least 32 characters).
3. Put your existing website index.html inside public/index.html. Keep your current design.
4. Open VS Code terminal in the folder containing package.json and server.js.
5. Run: npm install
6. Run: npm start
7. Open http://localhost:3000 and check http://localhost:3000/api/health

API:
POST /api/login JSON {"username":"admin","password":"your-password"}
POST /api/records JSON {"type":"complaint","name":"Test User","message":"Demo request"}
GET /api/records requires Authorization: Bearer TOKEN
PATCH /api/records/1/status requires token and JSON {"status":"Resolved"}

Allowed types: complaint, appointment, application, contact, other
Allowed statuses: Pending, In Progress, Resolved, Rejected
Photos go in public/images/ and HTML path can be /images/member.jpg.
Never share .env. This is a local/demo starter; harden security before public deployment.
