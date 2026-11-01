# Hi, I'm Vlad Sakharov 👋
I'm a Data Analyst / Full-stack Developer with over two years of professional experience at **Ozon Fintech** and **Karpov Courses**, where I designed production data pipelines, conducted in-depth analyses, and delivered actionable insights to stakeholders.
I've been passionate about data since I was 17 — turning raw information into clear answers through queries, automation, or visualization has always excited me.
Currently studying **Computer Programming** at **Georgian College** (Ontario, Canada) to strengthen my full-stack development skills. Combining a strong analytical background with hands-on programming allows me to build complete, end-to-end solutions — from data ingestion to interactive web applications. Most recently I picked up **Go** and built [Soundcheck](https://getsoundcheck.cc), a concert-alert service, in a week.

## 🔧 Technologies & Tools
![Swift](https://img.shields.io/badge/swift-F54A2A?style=for-the-badge&logo=swift&logoColor=white) 
![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white) 
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black) 
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white) 
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB) 
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white) 
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white) 
![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) 
![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white) 
![SQL](https://img.shields.io/badge/SQL-006488?style=for-the-badge&logo=mysql&logoColor=white) 
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white)
![ASP.NET](https://img.shields.io/badge/ASP.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)

**Data & Orchestration Tools**  
![Apache Airflow](https://img.shields.io/badge/Apache%20Airflow-017CEE?style=for-the-badge&logo=Apache%20Airflow&logoColor=white) 
![ClickHouse](https://img.shields.io/badge/ClickHouse-FFCC00?style=for-the-badge&logo=clickhouse&logoColor=black) 
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white) 
![Apache Superset](https://img.shields.io/badge/Apache%20Superset-66CED6?style=for-the-badge&logo=apache-superset&logoColor=white) 
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white) 
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white) 
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

## 🚀 Featured Projects

### Data Engineering & Analytics

___

**Jobs Canada — Canadian Labour Market Dashboard**

[![Tableau](https://img.shields.io/badge/Tableau%20Public-Jobs%20Canada-E97627?style=flat-square&logo=tableau&logoColor=white)](https://public.tableau.com/app/profile/YOUR_PROFILE/viz/JobsCanada/JobsCanada)
[![Repo](https://img.shields.io/badge/GitHub-CanadaJobsPipeline-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/vladsakharov/CanadaJobsPipeline)
[![Data](https://img.shields.io/badge/Data-Job%20Bank%20Open%20Data-006488?style=flat-square)](#)

End-to-end analytics project on the Canadian labour market: monthly Job Bank open data is ingested via an Airflow DAG into PostgreSQL, then visualized in an interactive Tableau Public dashboard covering **423K+ vacancies** (Jan–May 2026).

- **Data pipeline** — Airflow DAG `jobbank_vacancies` runs monthly: resolves the current CSV URL via CKAN API, downloads UTF-16LE tab-separated files (~30–40 MB), cleans 14 fields from 65 columns, upserts into PostgreSQL with `ON CONFLICT DO UPDATE`
- **Tableau dashboard** — KPI cards with sparklines (total vacancies, latest month + MoM, median pay, on-site %), monthly trend with dual axis (bars + MoM %), Top 20 NOC bar chart, province map with Wikipedia drill-down, paginated detail table with Job Bank links
- **Analytics layer** — Calculated fields (salary normalization, smart K/M labels), LOD expressions for filter-responsive KPIs, table calculations for MoM and pagination, parameters, dashboard URL actions
- **Guided flow** — Overview KPIs → monthly trend → top occupations → regional map → job-level detail table with external links

**Stack:** Python · Apache Airflow · PostgreSQL · Pandas · Tableau Public · Job Bank Open Data (open.canada.ca)

___

**Statify — Personal Spotify Analytics Platform**

[![Live](https://img.shields.io/badge/Live-statify.one-1DB954?style=flat-square&logo=railway&logoColor=white)](https://spotifystatistics-production.up.railway.app/)
[![Repo](https://img.shields.io/badge/GitHub-SpotifyStatistics-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/0n1xx/SpotifyStatistics)
[![Platform](https://img.shields.io/badge/Platform-Web%20%7C%20iOS-1DB954?style=flat-square)](#)

End-to-end analytics platform that continuously ingests Spotify listening history, enriches each track with geographic artist metadata via MusicBrainz, and surfaces insights across a web dashboard and a native iOS app.

- **Data pipeline** — Apache Airflow DAG runs every 3 minutes: fetches last 50 played tracks per user, resolves artist country/city via MusicBrainz, deduplicates by `played_at + user_id`, writes to PostgreSQL (analytics) and SQL Server (web app)
- **Web app** — ASP.NET Core 10 + Razor Pages: Dashboard, Recently Played (paginated), World Map (D3.js), full account management, Spotify/Google/GitHub OAuth, transactional email via Resend on `statify.one`
- **iOS app** — Native SwiftUI companion with full feature parity: Dashboard, History, World Map (MapKit), Settings — connects to the same ASP.NET backend via JWT REST API
- **Admin dashboard** — Apache Superset connected directly to PostgreSQL: KPI cards, activity charts, top artists/albums/songs, word cloud, raw history table
- **Infrastructure** — All services deployed on Railway; Airflow and Superset run on custom Docker images purpose-built for Railway's environment

**Stack:** Python · Apache Airflow · PostgreSQL · SQL Server · ASP.NET Core C# · Vanilla JS · D3.js · Swift · SwiftUI · Docker · Railway

### Full-Stack & Backend Development

___

**Soundcheck — Concert Alerts for Your Favourite Artists**

[![Live](https://img.shields.io/badge/Live-getsoundcheck.cc-3A7BD5?style=flat-square&logo=railway&logoColor=white)](https://getsoundcheck.cc)
[![Repo](https://img.shields.io/badge/GitHub-Soundcheck-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/0n1xx/Soundcheck)
[![Go](https://img.shields.io/badge/Built%20with-Go-00ADD8?style=flat-square&logo=go&logoColor=white)](#)

Go web service that tracks concerts for the artists you follow and alerts you by email or Telegram when they announce a show in your city. Built in a week to learn Go.

- **Background worker** — runs every 3 hours: checks every followed artist on Ticketmaster in parallel, saves each concert once and detects new shows, cancellations and new dates
- **Alerts** — email via Resend on `getsoundcheck.cc` and a Telegram bot, with reminders 24 h and 15 min before tickets go on sale; every alert is sent only once
- **Web app** — Upcoming shows, Artists and Settings pages in a classic Mac OS X Finder style, email/password and Google sign-in, full account management, works on phones
- **Infrastructure** — one Go program runs the website, the worker and the Telegram bot side by side; PostgreSQL, Docker, deployed on Railway with a custom domain

**Stack:** Go · net/http · html/template · pgx · PostgreSQL · errgroup · Ticketmaster API · Telegram Bot API · Resend · Google OAuth · Docker · Railway

___

**SecretAgentGadgetLab — Spy Gadget Marketplace**

[![Live](https://img.shields.io/badge/Live-secret--agent--lab-512BD4?style=flat-square&logo=railway&logoColor=white)](https://secret-agent-lab.up.railway.app)

ASP.NET Core MVC marketplace for a fictional secret-agent gadget shop.

- **Payments** — Stripe checkout with a full shopping cart
- **Auth** — Google & GitHub OAuth with role-based authorization
- **Media** — product images stored in Cloudinary
- Deployed on Railway

**Stack:** C# · ASP.NET Core MVC · Stripe · Cloudinary · OAuth · Railway

___

**iPod Marketplace — E-commerce Platform**

[![Live](https://img.shields.io/badge/Live-ipod--marketplace-777BB4?style=flat-square&logo=railway&logoColor=white)](https://ipod-marketplace.up.railway.app)

Full-stack PHP/MySQL e-commerce store.

- **Admin panel** — CRUD for products with image uploads
- **Users** — registration and authentication
- **Bilingual** — English and French interface
- Deployed on Railway

**Stack:** PHP · MySQL · HTML · CSS · JavaScript · Railway

### 📢 Content & Community
- YouTube: [How Requirements for Junior Data Analysts Changed](https://www.youtube.com/watch?v=l23LHX4G5iM&t=2s)

### 🌐 Connect with Me
[![Portfolio](https://img.shields.io/badge/Portfolio-vladislavsakharov.com-000000?style=for-the-badge&logo=safari&logoColor=white)](https://vladislavsakharov.com/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/vladislav-sakharov-8191b2242/)

### 📊 GitHub Stats
<img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=0n1xx&theme=monokai" alt="Profile Details" />

Thanks for visiting! I'm always open to discussing data engineering, web development, or potential opportunities.

— Vlad
