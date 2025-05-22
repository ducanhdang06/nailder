# 🧩 MVP Breakdown – Nail Design App

This file outlines the **Minimum Viable Product (MVP)** features for a Tinder-style nail design app where customers swipe designs from technicians, match, and chat.

---

## 🧑‍🎨 User Roles

### 1. Customer
- Browse/swipe nail designs
- Favorite/save designs
- Chat with technician after mutual interest

### 2. Technician
- Upload designs (image + tags)
- View matches
- Chat with customers

---

## 🗂 Feature Categories

### 🔐 Authentication
- Sign up / Login with email (Cognito)
- Role selection: Customer or Technician
- Optional: Social login (Apple, Google)

### 🖼 Nail Design Management
- Technicians upload designs with tags (e.g. “almond”, “pink”, “floral”)
- Images stored in S3
- Metadata stored in DynamoDB

### 💅 Swipe/Explore
- Swipe-style browsing for customers
- Favorite/save nail designs
- Record swipes for match logic

### 💘 Match System
- Backend checks for mutual interaction
- If matched, both users can chat
- Store matches in DynamoDB

### 💬 Real-Time Chat
- Simple chat UI
- Real-time messages using AWS AppSync (GraphQL + Subscriptions)
- Push notification for new messages

---

## 🧭 MVP Roadmap (By Phase)

### ✅ Phase 1: Core MVP (0–2 months)
- [ ] Set up AWS Cognito for auth
- [ ] Build signup/login UI in SwiftUI
- [ ] Build upload form + integrate S3 upload
- [ ] Create backend Lambda to store design info
- [ ] Display design cards with swipe/favorite
- [ ] Build match logic with DynamoDB
- [ ] Implement basic chat UI using AppSync
- [ ] Push notification for new match

### 🧪 Phase 2: Beta Testing (2–3 months)
- [ ] Internal test with 5–10 users
- [ ] Feedback collection
- [ ] Block/report feature
- [ ] Improve filters (by tag, shape, etc.)
- [ ] Add loading states and error handling

### ✨ Phase 3: Post-MVP (3–6 months)
- [ ] Appointment request system
- [ ] Technician availability calendar
- [ ] Customer reviews for techs
- [ ] Admin dashboard for analytics
- [ ] AI suggestions (e.g., "you might also like")

---

## 🗃 Database Tables (DynamoDB)

| Table         | Keys                      | Purpose                           |
|---------------|---------------------------|-----------------------------------|
| `users`       | `user_id`                 | Store profile info and role       |
| `designs`     | `design_id`, `tech_id`    | Nail design metadata              |
| `swipes`      | `user_id`, `target_id`    | Stores swipe interactions         |
| `matches`     | `match_id`                | Stores mutual matches             |
| `messages`    | `chat_id`, `timestamp`    | Chat history                      |

---

## 🧰 Tools Used

- **Swift + SwiftUI** – Frontend iOS app
- **AWS Cognito** – Auth
- **Amazon S3** – Media storage
- **AWS Lambda + API Gateway** – Backend logic
- **DynamoDB** – NoSQL database
- **AWS AppSync** – Real-time chat
- **SNS + APNs** – Notifications

---

## 📌 Notes

- MVP should be usable with no admin interface.
- Focus is on smooth design experience + messaging.
- Booking/review features can wait until Phase 3.

