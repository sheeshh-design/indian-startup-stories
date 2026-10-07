# Indian Startup Stories (ISS)

> **Real Founders. Real Journeys. Real Stories.**  
> An editorial case study & media platform documenting the pivotal turning points, business models, funding journeys, and growth playbooks of India's startup ecosystem.

---

## 🚀 Overview

**Indian Startup Stories** is a curated editorial web application showcasing deep dives into Indian startups and visionary entrepreneurs (Zerodha, Zomato, Freshworks, Meesho, Swiggy, Nykaa, Razorpay, etc.). 

### ✨ Key Features
- **Featured & Deep-Dive Stories**: Complete timelines, breakdown of unit economics, challenges, pivots, and pivotal growth moments.
- **Founder Profiles**: Background, education, philosophy, and founder wisdom.
- **Funding & Valuation Trackers**: Stage-by-stage funding breakdowns (Bootstrapped, Seed to Series G, IPO).
- **Growth & Marketing Breakdowns**: Viral loops, CAC optimization, product-led growth (PLG), and consumer insights.
- **Failures & Hard Lessons Post-Mortems**: Honest retrospectives on fallen ventures and critical lessons for modern entrepreneurs.
- **Interactive Bookmarks & Reading List**: Client-side persisted reading queue for case studies.
- **Instant Search & Industry Filtering**: Quick access by sector (Fintech, FoodTech, SaaS, E-Commerce, Logistics, etc.).

---

## 🛠️ Tech Stack

- **Framework**: [React 19](https://react.dev/) + [TypeScript](https://www.typescriptlang.org/)
- **Bundler & Dev Server**: [Vite 6+](https://vite.dev/)
- **Styling**: [Tailwind CSS v4](https://tailwindcss.com/)
- **Animations**: [Motion](https://motion.dev/) (Framer Motion)
- **Icons**: [Lucide React](https://lucide.dev/)
- **Fonts**: Manrope (Headlines), Inter (Body), Newsreader (Editorial accents)

---

## 📦 Getting Started

### Prerequisites
Make sure you have [Node.js](https://nodejs.org/) (v18 or v20+) installed on your machine.

### Installation

1. **Clone or Download the Repository**:
   ```bash
   git clone https://github.com/<your-username>/indian-startup-stories.git
   cd indian-startup-stories
   ```

2. **Install Dependencies**:
   ```bash
   npm install
   ```

3. **Configure Environment Variables (Optional)**:
   Copy `.env.example` to `.env`:
   ```bash
   cp .env.example .env
   ```

4. **Start the Development Server**:
   ```bash
   npm run dev
   ```
   Open [http://localhost:3000](http://localhost:3000) (or the URL shown in your terminal) in your browser.

5. **Build for Production**:
   ```bash
   npm run build
   ```
   This generates optimized static files in the `dist/` directory.

6. **Preview Production Build**:
   ```bash
   npm run preview
   ```

---

## 🌐 Deploying to the Web

### Option A: Vercel (Recommended)
1. Push this repository to GitHub.
2. Sign in to [Vercel](https://vercel.com/) and click **"Add New Project"**.
3. Import your GitHub repository.
4. Framework Preset will automatically detect **Vite**.
5. Click **Deploy**.

### Option B: Netlify
1. Connect your repository on [Netlify](https://www.netlify.com/).
2. Set Build Command: `npm run build`
3. Set Publish Directory: `dist`
4. Click **Deploy Site**.

### Option C: GitHub Pages
1. In `vite.config.ts`, set the base path if your repository is a subpath:
   ```typescript
   export default defineConfig({
     base: '/<repository-name>/',
     // ... rest of config
   });
   ```
2. Build and publish the `dist` directory using `gh-pages` or a GitHub Actions workflow.

---

## 📁 Project Structure

```text
├── index.html               # Main HTML entrypoint with metadata & fonts
├── package.json             # NPM package scripts and dependencies
├── vite.config.ts           # Vite configuration
├── tsconfig.json            # TypeScript configuration
├── src/
│   ├── main.tsx             # React root mount
│   ├── App.tsx              # Application layout, state, routing & drawers
│   ├── index.css            # Tailwind CSS styling and global typography
│   ├── components/          # Reusable UI views & editorial components
│   │   ├── Navbar.tsx       # Header with bookmarks count & navigation
│   │   ├── Hero.tsx         # Editorial masthead hero section
│   │   ├── StoryView.tsx    # Comprehensive deep-dive case study reader
│   │   ├── StoryCard.tsx    # Card representation of individual stories
│   │   ├── StoryGridView.tsx# Searchable and filterable archive
│   │   ├── FoundersView.tsx # Founder wisdom and bios
│   │   ├── FundingView.tsx  # Investment rounds & stages
│   │   ├── MarketingView.tsx# Growth marketing teardowns
│   │   ├── FailuresView.tsx # Startup post-mortems and lessons
│   │   ├── IndustriesView.tsx # Industry taxonomy breakdown
│   │   ├── BookmarkDrawer.tsx # Slide-out reading queue
│   │   ├── SearchModal.tsx  # Fast full-text search
│   │   └── Footer.tsx       # Masthead footer
│   └── data/                # Structured case study & editorial datasets
│       ├── stories.ts       # Full company profiles, timelines & lessons
│       ├── founders.ts      # Founder quotes & backgrounds
│       ├── funding.ts       # Investment teardowns
│       ├── marketing.ts     # Growth strategies & tactics
│       ├── failures.ts      # Post-mortems
│       └── industries.ts    # Sector classifications
```

---

## 📄 License
This project is open source and available under the [MIT License](LICENSE).
