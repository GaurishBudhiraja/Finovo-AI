# 🚀 FinovoAI

### Investment Advice That Thinks Before It Recommends.

# 🌟 Overview

**FinovoAI** is an intelligent, real-time investment advisor built to help users make smarter financial decisions.

Unlike traditional financial chatbots that rely on static templates and predefined responses, FinovoAI uses a **LangGraph ReAct (Reason + Act) Agent** that:

* Understands user goals
* Retrieves live financial data
* Performs reasoning
* Builds investment recommendations dynamically
* Explains its decisions transparently

Whether you're exploring mutual funds, crypto investments, or seeking portfolio guidance, FinovoAI provides data-driven insights through a premium AI-powered experience.

---

# ✨ Key Features

## 📈 Mutual Fund Advisor

Generate personalized mutual fund portfolios based on:

* Age
* Investment Amount
* Risk Appetite
* Investment Duration

### Provides
✅ Asset Allocation
✅ Top Fund Recommendations
✅ CAGR Analysis
✅ Future Value Projection
✅ Rebalancing Strategy
✅ AI Explanations
---

## ₿ Crypto Portfolio Advisor

Build crypto portfolios using:

* Investment Amount
* Investment Horizon
* Drawdown Tolerance

### Provides

✅ Crypto Allocation
✅ Risk Assessment
✅ Volatility Analysis
✅ Portfolio Simulations
✅ Return Projections
✅ Market Insights
---

## 🤖 AI Investment Advisor

Conversational investment assistant powered by:

* LangGraph
* Groq Llama 3.3 70B
* CoinGecko
* MFAPI

### Capabilities

* SIP Planning
* Portfolio Review
* Fund Research
* Crypto Analysis
* Risk Assessment
* Asset Comparison
* Market Insights

### Supports

* Markdown Responses
* Tables
* Financial Comparisons
* Live Data Retrieval

---

## 📊 Investment Dashboard

Unified analytics dashboard featuring:

* Portfolio Overview
* Asset Allocation
* Performance Analytics
* Portfolio Health
* Market Sentiment
* AI Confidence Indicators
* Investment Insights

---

# 🧠 True Agentic AI

FinovoAI does not simply generate responses.

The AI agent follows a ReAct workflow:

```
User Query
    ↓
Reason
    ↓
Fetch Live Data
    ↓
Analyze Results
    ↓
Reason Again
    ↓
Generate Final Recommendation

```

This allows FinovoAI to:

* Retrieve real market information
* Avoid static recommendations
* Minimize hallucinations
* Provide transparent reasoning

---

# 🏗 Architecture

```
                    ┌─────────────────┐
                    │      User       │
                    └────────┬────────┘
                             │
                             ▼
                 ┌─────────────────────┐
                 │      FinovoAI       │
                 │      Frontend       │
                 └────────┬────────────┘
                          │
                          ▼
                 ┌─────────────────────┐
                 │      FastAPI        │
                 │      Backend        │
                 └────────┬────────────┘
                          │
      ┌───────────────────┼───────────────────┐
      ▼                   ▼                   ▼

┌──────────────┐  ┌──────────────┐  ┌──────────────┐
│ Mutual Fund  │  │    Crypto    │  │ AI Advisor   │
│ Recommendation│ │ Recommendation│ │ LangGraph    │
└───────┬──────┘  └───────┬──────┘  └───────┬──────┘
        │                 │                 │
        ▼                 ▼                 ▼

┌──────────────┐  ┌──────────────┐  ┌──────────────┐
│    MFAPI     │  │ CoinGecko    │  │ Groq LLM     │
└──────────────┘  └──────────────┘  └──────────────┘

```

---

# ⚙️ Tech Stack

## 🎨 Frontend

* Next.js 15
* React
* TypeScript
* Tailwind CSS
* shadcn/ui
* Framer Motion
* React Query
* React Hook Form
* Zod
* Recharts
* React Markdown
* Lucide Icons

---

## 🔧 Backend

* FastAPI
* Python
* LangGraph
* Groq LLM
* MFAPI
* CoinGecko

---

## 🧠 AI Stack

* LangGraph ReAct Agent
* Groq Llama 3.3 70B
* Tool Calling Architecture
* Financial Knowledge Layer
* Live Market Intelligence

---

# 🌐 Pages

| RouteDescription |                          |
| ---------------- | ------------------------ |
| `/`              | Landing Page             |
| `/dashboard`     | Investment Dashboard     |
| `/mutual-funds`  | Mutual Fund Advisor      |
| `/crypto`        | Crypto Portfolio Advisor |
| `/advisor`       | AI Investment Advisor    |
| `/about`         | About Platform           |

---

# 🔌 API Endpoints

## Mutual Fund Recommendation

```
POST /api/mf/recommend

```

### Example Request

```
{
  "age": 25,
  "amount": 100000,
  "risk": "medium",
  "duration_years": 10
}

```

---

## Crypto Recommendation

```
POST /api/crypto/recommend

```

### Example Request

```
{
  "amount": 50000,
  "investment_horizon": "medium-term",
  "max_drawdown": 50
}

```

---

## AI Advisor

```
POST /api/agent/chat

```

### Example Request

```
{
  "query": "How should I invest ₹50,000?"
}

```

---

# 📂 Project Structure

```
FinovoAI
│
├── backend/
│   ├── app/
│   ├── api/
│   ├── agents/
│   ├── services/
│   └── core/
│
├── frontend/
│   ├── app/
│   ├── components/
│   ├── hooks/
│   ├── lib/
│   ├── public/
│   └── types/
│
└── README.md

```

---

# 🚀 Running Locally

## Backend Setup

```
cd backend

python -m venv .venv

# Windows
.venv\Scripts\activate

# Linux/Mac
source .venv/bin/activate

pip install -r requirements.txt

```

Create `.env`

```
GROQ_API_KEY=your_groq_api_key
COINGECKO_API_KEY=your_coingecko_api_key

```

Start Backend

```
uvicorn app.main:app --reload

```

Backend runs at:

```
http://localhost:8000

```

---

## Frontend Setup

```
cd frontend

npm install

```

Create:

```
.env.local

```

```
NEXT_PUBLIC_API_BASE_URL=http://localhost:8000

```

Start Frontend

```
npm run dev

```

Frontend runs at:

```
http://localhost:3000

```

---

# ☁️ Deployment

## Backend (Render)

Root Directory:

```
backend

```

Start Command:

```
uvicorn app.main:app --host 0.0.0.0 --port $PORT

```

---

## Frontend (Vercel)

Root Directory:

```
frontend

```

Environment Variable:

```
NEXT_PUBLIC_API_BASE_URL=https://your-backend-url.com

```

---

# 🎯 Design Philosophy

### 🧠 Intelligence First

Recommendations should be explainable, not black-box outputs.

### ⚖️ Risk-Aware Investing

Understanding downside risk is more important than chasing returns.

### ✨ Premium User Experience

Financial products should inspire trust, clarity, and confidence.

---

# 🔮 Future Enhancements

* User Authentication
* Portfolio Tracking
* SIP Automation
* Real-Time Alerts
* Brokerage Integration
* Watchlists
* Portfolio Backtesting
* Tax Optimization
* Multi-Agent Financial Analysis
* Personalized Financial Planning

---

# 👥 Team

**Gaurish Budhiraja**
**Abhinava K.**
**Chandramani Kumar**
**Atharv**

---

# ⚠️ Disclaimer

FinovoAI is developed for educational, research, and hackathon purposes.

The recommendations generated by this platform are AI-assisted insights and should not be considered professional financial advice.

Always consult a SEBI-registered financial advisor before making investment decisions.

---

# Our website:-- https://finovo-ai.vercel.app/
