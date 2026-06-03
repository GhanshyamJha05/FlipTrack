# FlipTrack 🎯
**Your Reselling Empire, Tracked in Real Time.**

An open-source SaaS platform designed specifically for sneaker, streetwear, and collectibles resellers to manage their inventory, track market prices, and analyze their business using AI.

Built for the **Open Source Hackathon by Elite Coders**.

---

## 🚀 Vision

The reselling market is booming, but resellers often rely on messy spreadsheets and fragmented tools to manage thousands of dollars in inventory. **FlipTrack** unifies the entire workflow. It is a feature-complete, modern alternative to existing premium trackers, fully open-sourced for the community. 

Whether you are flipping 10 pairs a month or running a massive consignment operation, FlipTrack scales with you.

---

## 🌟 Key Features

- **Inventory Management**: Track every item with granular details (SKU, size, condition, purchase price, status).
- **Market Price Intelligence**: Automated background scraping (via cron jobs) of real-time market prices across secondary platforms.
- **AI Insights**: LLM-powered (Groq + Vercel AI SDK) insights to tell you exactly *when* to hold and *when* to sell based on market trends.
- **Sales & Expense Tracking**: Log sales, track shipping/platform fees, and generate detailed P&L (Profit & Loss) statements.
- **Secure Authentication**: Enterprise-grade secure authentication via Supabase (SSR Cookies).
- **Beautiful Dashboard**: A premium, glassmorphic UI built from scratch using custom CSS properties, ensuring blazing fast performance without heavy UI libraries.

---

## 🛠️ Tech Stack

FlipTrack is built using a modern, scalable, and fully type-safe stack:

- **Framework**: React Router v7 (SSR & Data Loaders)
- **Database**: PostgreSQL (via Supabase)
- **ORM**: Prisma Client v5
- **Authentication**: Supabase Auth (Server-Side Rendering setup)
- **AI Integration**: Vercel AI SDK + Groq API (Llama 3)
- **Styling**: Vanilla CSS with comprehensive CSS Custom Properties for theming
- **Deployment**: Ready for Vercel & Supabase
- **Language**: TypeScript (Strict Mode)

---

## 🏃 Getting Started (Local Setup)

To get a local copy of FlipTrack running on your machine:

### 1. Prerequisites
- **Node.js** (v18+)
- **Git**
- A **Supabase** account (for Database and Auth)
- A **Groq** API key (for AI features)

### 2. Clone the Repository
```bash
git clone https://github.com/rushikesh-bobade/FlipTrack.git
cd FlipTrack
```

### 3. Install Dependencies
```bash
npm install
```

### 4. Environment Variables
Create a `.env` file in the root directory. You can use `.env.example` as a base (if provided), or fill in the following:

```env
# Supabase Configuration
NEXT_PUBLIC_SUPABASE_URL=your_supabase_project_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
DATABASE_URL=your_supabase_transaction_pooler_url
DIRECT_URL=your_supabase_session_url

# Groq AI
GROQ_API_KEY=your_groq_api_key
```

### 5. Database Setup (Prisma)
Push the Prisma schema to your Supabase Postgres database:
```bash
npx prisma db push
npx prisma generate
```

### 6. Start the Development Server
```bash
npm run dev
```
The application will be running on `http://localhost:5173`. 

---

## 💡 Demo Setup

Want to see it in action without manually creating data? We have included a demo script that provisions a test user and sample sneaker inventory.

1. Start the server: `npm run dev`
2. Run the seed script:
   ```bash
   npx tsx scripts/create-demo-user.ts
   ```
3. Navigate to `http://localhost:5173/auth/login`.
4. Click **"Use Demo Credentials"** to instantly log into the populated dashboard.

---

## 🛡️ License

Distributed under the **MIT License**. See `LICENSE` for more information.

---

*Made with ❤️ for the Open Source Hackathon.*
