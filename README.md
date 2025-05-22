# 💅 Nail Design App (Tinder-style)

A mobile app where customers swipe through nail designs posted by technicians, favorite styles, chat in real-time, and eventually book appointments. Built with **Swift (SwiftUI)** on the frontend and **AWS serverless services** on the backend.

---

## 🌟 MVP Features

### 🧑‍🎨 For Customers
- Swipe to browse nail designs
- Favorite and save designs
- Chat with technicians after matching

### 💼 For Technicians
- Upload nail designs (with tags)
- Manage profile and contact info
- Chat with interested customers

---

## 🛠 Tech Stack

### **Frontend (iOS)**
- Swift + SwiftUI
- AWS Amplify SDK (Cognito, Storage, GraphQL API)
- AsyncImage, NavigationStack, Custom swipe cards

### **Backend (AWS)**
- **Amazon Cognito** – user authentication
- **API Gateway + Lambda** – API endpoints (Node.js)
- **DynamoDB** – store users, swipes, matches, messages
- **Amazon S3** – store images (nail designs, profile pics)
- **AppSync (GraphQL)** – real-time chat (optional)
- **SNS + APNs** – push notifications

---

## 🧱 Project Structure
nail-app/
├── ios-app/ # SwiftUI frontend
├── backend/ # AWS Lambda functions
├── infra/ # Infrastructure-as-Code (CDK/Amplify)
├── data-models/ # Database schema
├── docs/ # MVP plan, architecture diagrams
├── scripts/ # Helper scripts (e.g., deploy.sh)
├── tests/ # Test files (Lambda, etc.)
├── .env.example # Environment variable template
├── .gitignore
└── README.md # You are here

## To do (MVP Tracker)
[ ] Authentication (Cognito)
[ ] Upload nail design to S3
[ ] Swipe UI and backend logic
[ ] Match system (DynamoDB)
[ ] Chat UI and AppSync backend
[ ]Push notifications

## License
MIT License – feel free to use, contribute, and remix.
