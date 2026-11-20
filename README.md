# 🎯 AI Support Ticket Router

### An AI-powered customer support automation system

AI Support Ticket Router is a full-stack application that helps businesses automatically classify customer support tickets, detect their priority, assign them to the right department, and generate suggested responses using AI.

Instead of manually reviewing every customer complaint, the system automates the initial support workflow and helps teams respond faster.

## 🚀 Problem Statement

Businesses receive hundreds of customer support requests every day.

Manually reviewing and assigning these tickets creates several problems:

- Slow response times.
- Incorrect ticket assignments.
- Difficulty identifying urgent issues.
- Repetitive manual work for support teams.

## 💡 Our Solution

AI Support Ticket Router uses AI to understand incoming customer messages and automate ticket management.

When a customer submits a ticket, the system:

1. Reads and understands the customer's message.
2. Identifies the ticket category.
3. Detects its priority (Low, Medium, High).
4. Assigns it to the appropriate department.
5. Generates an AI-powered response suggestion.
6. Saves the ticket and its processing history.

## ✨ Key Features

- **AI Ticket Classification:** Automatically categorizes customer complaints.
- **Priority Detection:** Identifies urgent customer issues.
- **Smart Ticket Routing:** Assigns tickets to the appropriate support department.
- **AI Response Generation:** Creates suggested replies for support agents.
- **Ticket Management Dashboard:** View, filter and manage all tickets.
- **Human-in-the-Loop:** Support agents can review and edit AI suggestions.
- **Ticket History:** Track ticket status and previous actions.

## 🏗️ System Architecture

```text
       Customer
           |
           v
    Submit Support Ticket
           |
           v
      React Frontend
           |
           v
     FastAPI Backend
           |
           v
       AI Engine
           |
     +-----+------+
     |     |      |
     v     v      v
  Category Priority Department
  Detection Detection Routing
     |     |      |
     +-----+------+
           |
           v
   Generate Response
           |
           v
     Supabase Database
           |
           v
    Support Dashboard
           |
           v
    Human Agent Review
```

## 🛠️ Tech Stack

| Technology   | Purpose         |
| ------------ | --------------- |
| React        | Frontend        |
| Tailwind CSS | UI Styling      |
| Python       | Backend logic   |
| FastAPI      | REST APIs       |
| Gemini API   | AI integration  |
| Supabase     | Database        |
| PostgreSQL   | Data storage    |
| Git & GitHub | Version control |

## 📂 Project Structure

```text
ai-support-ticket-router/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   └── App.jsx
│   └── package.json
│
├── backend/
│   ├── app/
│   │   ├── main.py
│   │   ├── routes/
│   │   ├── services/
│   │   ├── models/
│   │   └── database/
│   ├── requirements.txt
│   └── .env.example
│
├── screenshots/
│
└── README.md
```

## ⚙️ How It Works

**Step 1:** A customer submits a support ticket.

**Step 2:** FastAPI receives the request.

**Step 3:** The AI analyzes the message and returns structured information.

**Step 4:** The backend validates the AI output and determines the appropriate department.

**Step 5:** The ticket and AI-generated response are stored in Supabase.

**Step 6:** A support agent reviews the suggested response and manages the ticket.

## 🔌 API Endpoints

| Method | Endpoint                    | Description             |
| ------ | --------------------------- | ----------------------- |
| POST   | `/api/tickets`              | Create a ticket         |
| GET    | `/api/tickets`              | Get all tickets         |
| GET    | `/api/tickets/{id}`         | Get ticket details      |
| PATCH  | `/api/tickets/{id}`         | Update ticket           |
| POST   | `/api/tickets/{id}/analyze` | Analyze ticket using AI |

## 🔐 Environment Variables

Create a `.env` file inside the backend directory.

```env
GEMINI_API_KEY=your_api_key
SUPABASE_URL=your_supabase_url
SUPABASE_KEY=your_supabase_key
```

Never commit API keys or secret credentials to GitHub.

## 💻 Local Development

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/ai-support-ticket-router.git

cd ai-support-ticket-router
```

### 2. Start the backend

```bash
cd backend

python -m venv venv

pip install -r requirements.txt

uvicorn app.main:app --reload
```

### 3. Start the frontend

```bash
cd frontend

npm install

npm run dev
```

## 🧪 Testing

The project should be tested with different customer scenarios:

- Payment failure.
- Refund request.
- Login problems.
- Account access issues.
- Technical errors.
- Urgent service complaints.

Check whether the AI correctly identifies categories, priorities and departments.

## 🔮 Future Improvements

- Email notifications.
- Real-time ticket updates.
- Analytics and reporting.
- AI accuracy evaluation.
- Multi-language ticket support.
- Integration with external CRM platforms.

## 🎯 Project Objective

The objective of this project is to demonstrate how AI can solve a real business problem through automation, API integration, backend development and database management.

This project focuses on building a practical AI-powered business workflow rather than just another chatbot.

---

**Built with ❤️ to solve real-world customer support problems.**
