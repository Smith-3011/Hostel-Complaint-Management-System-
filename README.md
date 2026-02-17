🏫 Hostel Complaint Management System
=====================================

A full-stack web application to **digitize and streamline hostel issue reporting and resolution**. Students can raise complaints (even anonymously), track their status in real time, and receive updates, while admins and officers can manage, assign, and resolve issues efficiently. The system is built using the **MERN stack** and includes **AI-powered assistance** for better complaint quality and faster resolution.

🚀 Key Features
---------------

### 👩‍🎓 For Students

*   Submit complaints with **title, description, category, image, and location**
    
*   Option to submit **anonymous complaints** to avoid fear of retaliation
    
*   Track complaint status in real time (Pending → In Progress → Resolved)
    
*   Receive **email notifications** on status updates
    
*   View complaint history and responses from staff
    
*   Use **AI assistance** to:
    
    *   Auto-correct and improve complaint wording
        
    *   Convert rough text into clear, well-formatted complaints
        

### 🧑‍💼 For Admin / Officers

*   Role-based dashboards (Admin / Officer)
    
*   View, filter, and search complaints by status, category, or date
    
*   Assign complaints to officers
    
*   Update status and add resolution notes
    
*   View complaint analytics and workload distribution
    
*   Prevent spam and duplicate complaints using server-side validation
    
*   Track anonymous complaints while still preventing abuse internally
    

### 🤖 AI-Powered Features

*   **AI Complaint Enhancer**: Improves grammar, clarity, and structure of user complaints
    
*   **Smart Categorization (Optional)**: Suggests complaint category based on content
    
*   **Duplicate Detection (Optional)**: Flags similar complaints to reduce repeated issues
    

🛠️ Tech Stack
--------------

### Frontend

*   React.js
    
*   Tailwind CSS
    
*   React Router
    
*   Axios
    
*   Toastify (Notifications)
    

### Backend

*   Node.js
    
*   Express.js
    
*   MongoDB (Mongoose)
    
*   JWT Authentication
    
*   Cloudinary (Image Uploads)
    
*   Nodemailer (Email Notifications)
    

### AI Integration

*   Google Gemini / Groq (for text improvement & analysis)
    

### Dev Tools

*   Vite
    
*   Postman
    
*   Git & GitHub
    

🏗️ System Architecture
-----------------------

*   **Frontend (React)**: Handles UI, forms, dashboards, and real-time user interactions
    
*   **Backend (Node + Express)**: Handles business logic, authentication, role checks, AI calls, and APIs
    
*   **Database (MongoDB)**: Stores users, complaints, status history, and logs
    
*   **Cloudinary**: Stores complaint images
    
*   **Email Service (Nodemailer)**: Sends status update notifications
    
*   **AI Service**: Improves complaint text and assists categorization
    

📁 Project Structure
--------------------

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   Hostel-Complaint-Management-System/  ├── backend/  │   ├── controllers/  │   ├── models/  │   ├── routes/  │   ├── middleware/  │   ├── utils/  │   ├── index.js  │   └── package.json  ├── frontend/  │   ├── src/  │   │   ├── components/  │   │   ├── pages/  │   │   ├── services/  │   │   ├── App.jsx  │   │   └── main.jsx  │   └── package.json  └── README.md   `

🔐 Authentication & Roles
-------------------------

*   **JWT-based Authentication**
    
*   Roles:
    
    *   **Student**: Can create and track complaints
        
    *   **Officer**: Can view, update, and resolve assigned complaints
        
    *   **Admin**: Can manage all complaints, assign officers, and monitor system activity
        
*   **Anonymous Complaints**:
    
    *   Identity hidden from staff
        
    *   Internally tracked to prevent abuse
        

🧾 Complaint Lifecycle
----------------------

1.  Student submits complaint (optionally anonymous)
    
2.  Admin reviews and assigns to an officer
    
3.  Officer marks it **In Progress**
    
4.  Officer resolves and marks it **Resolved**
    
5.  Student receives email notification
    
6.  Complaint is stored in history for analytics and reporting
    

⚙️ Installation & Setup
-----------------------

### Prerequisites

*   Node.js (v18+)
    
*   MongoDB (Local or Atlas)
    
*   Cloudinary Account
    
*   Email SMTP Credentials
    
*   AI API Key (Gemini / Groq)
    

### 🔧 Backend Setup

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   cd backend  npm install   `

Create a .env file in backend/:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   PORT=5000  MONGO_URI=your_mongodb_connection_string  JWT_SECRET=your_jwt_secret  CLOUDINARY_CLOUD_NAME=your_cloud_name  CLOUDINARY_API_KEY=your_api_key  CLOUDINARY_API_SECRET=your_api_secret  EMAIL_USER=your_email  EMAIL_PASS=your_email_password  AI_API_KEY=your_ai_api_key   `

Start backend:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   npm run dev   `

### 🎨 Frontend Setup

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   cd frontend  npm install  npm run dev   `

📡 API Highlights
-----------------

*   POST /api/auth/login – User login
    
*   POST /api/complaints – Create complaint
    
*   GET /api/complaints – Get complaints (role-based)
    
*   PUT /api/complaints/:id/status – Update complaint status
    
*   POST /api/ai/improve – Improve complaint text using AI
    

📊 Performance & Reliability
----------------------------

*   Server-side validation to prevent invalid or duplicate complaints
    
*   Indexed MongoDB queries for faster dashboard filtering
    
*   Cloudinary CDN for fast image loading
    
*   Async email and AI processing
    
*   Handles **500+ complaints** and **100+ concurrent users** reliably
    

🚀 Deployment
-------------

### Backend

*   Deploy on Render / Railway / AWS / etc.
    
*   Set environment variables in hosting dashboard
    

### Frontend

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   npm run build   `

*   Deploy dist/ folder to Netlify / Vercel
    

🧪 Testing
----------

*   API tested using Postman
    
*   Manual end-to-end testing for:
    
    *   Auth flows
        
    *   Complaint lifecycle
        
    *   Role-based access
        
    *   Anonymous complaints
        
    *   AI text enhancement
        

🤝 Contributing
---------------

1.  Fork the repo
    
2.  Create a new branch
    
3.  Commit your changes
    
4.  Open a Pull Request
    

📄 License
----------

This project is licensed under the **MIT License**.

💡 Future Improvements
----------------------

*   Mobile app version
    
*   SLA-based auto-escalation
    
*   Predictive maintenance using complaint history
    
*   Team dashboards and performance scoring
    
*   Real-time notifications using WebSockets
