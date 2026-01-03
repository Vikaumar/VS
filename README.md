🎓 EduFace AI: Smart Attendance & LMS PlatformA Multi-Role Educational Platform merging Face Recognition, Generative AI, and Voice Analytics.EduFace AI extends traditional attendance systems by integrating a Role-Based Learning Management System (LMS). It uses InsightFace for real-time biometric attendance and OpenAI/LangChain to allow teachers to generate quizzes from curriculum PDFs and query student performance using Voice Commands.🚀 Key Features by Role👨‍🏫 Teacher (The AI Command Center)Real-Time Attendance Dashboard: View live check-ins from the Face Recognition node.Curriculum AI: Upload PDF textbooks/notes; the system automatically generates Quizzes and Lesson Plans using GPT-4o.Voice Analytics: "Talk to your Database." Ask complex questions via voice (e.g., "Who has attendance below 75% and failed the last quiz?") and get instant verbal/text reports.👩‍🎓 Student (Performance View)Personal Dashboard: View personal attendance history and visuals.Performance Tracking: Access quiz scores and generated progress reports.🏫 Management (Oversight)Global Analytics: Aggregate view of attendance trends across the institution.Anomaly Detection: Automated flagging of irregular attendance patterns.🏗️ Architecture & Tech StackComponentTech UsedPurposeBiometricsInsightFace, OpenCVSOTA Face Recognition & Anti-spoofingFrontend/UIStreamlitInteractive Web Dashboard for all rolesBackend LogicPythonCore logic orchestrationDatabaseSQLiteRelational storage for Users, Attendance, MarksGenAIOpenAI API, LangChainQuiz Generation & Natural Language-to-SQLVoiceOpenAI WhisperSpeech-to-Text transcription for analytics📂 Project StructurePlaintextEduFace_AI/
│
├── app.py                   # Main Streamlit Web Application (The Dashboard)
├── auth.py                  # Role-based login logic
│
├── database/
│   ├── db_manager.py        # SQLite connection & Schema creation
│   ├── school.db            # The Relational Database (Replaces CSVs)
│   └── embeddings.pkl       # Face Embeddings storage
│
├── core_ai/
│   ├── face_rec_service.py  # Background service running the Webcam/InsightFace
│   ├── rag_engine.py        # PDF Parsing & Quiz Generation Logic
│   └── voice_agent.py       # LangChain SQL Agent for Voice Queries
│
├── utils/
│   ├── pdf_parser.py        # Extract text from uploaded PDFs
│   └── plot_utils.py        # Graphs for Student/Teacher Dashboards
│
├── requirements.txt
└── README.md
⚡ Quick Start (Hackathon Mode)Clone the Repo:Bashgit clone https://github.com/yourusername/EduFace-AI.git
Install Dependencies:Bashpip install -r requirements.txt
Configure Secrets:Create a .env file:Code snippetOPENAI_API_KEY=sk-proj-....
Run the Platform:Bash# Terminal 1: Run the Web Dashboard
streamlit run app.py

# Terminal 2: Run the Face Recognition Node
python core_ai/face_rec_service.py
🔮 Future RoadmapMobile App integration for students.Emotion analysis during class for engagement tracking.Integration with Google Classroom API.
