# Hi, I'm Vlad Sakharov 👋
I'm a Data Analyst / Full-stack Developer with over two years of professional experience at **Ozon Fintech** and **Karpov Courses**, where I designed production data pipelines, conducted in-depth analyses, and delivered actionable insights to stakeholders.
I've been passionate about data since I was 17 — turning raw information into clear answers through queries, automation, or visualization has always excited me.
Currently studying **Computer Programming** at **Georgian College** (Ontario, Canada) to strengthen my full-stack development skills. Combining a strong analytical background with hands-on programming allows me to build complete, end-to-end solutions — from data ingestion to interactive web applications.

## 🔧 Technologies & Tools
![Swift](https://img.shields.io/badge/swift-F54A2A?style=for-the-badge&logo=swift&logoColor=white) 
![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white) 
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black) 
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white) 
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white) 
![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) 
![SQL](https://img.shields.io/badge/SQL-006488?style=for-the-badge&logo=mysql&logoColor=white) 
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white)

**Data & Orchestration Tools**  
![Apache Airflow](https://img.shields.io/badge/Apache%20Airflow-017CEE?style=for-the-badge&logo=Apache%20Airflow&logoColor=white) 
![ClickHouse](https://img.shields.io/badge/ClickHouse-FFCC00?style=for-the-badge&logo=clickhouse&logoColor=black) 
![Apache Superset](https://img.shields.io/badge/Apache%20Superset-66CED6?style=for-the-badge&logo=apache-superset&logoColor=white) 
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white) 
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white) 
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

## 🚀 Featured Projects

### Data Engineering & Analytics

___

**Statify — Personal Spotify Analytics Platform**

[![Live](https://img.shields.io/badge/Live-statify.one-1DB954?style=flat-square&logo=railway&logoColor=white)](https://statify.one/)
[![Repo](https://img.shields.io/badge/GitHub-SpotifyStatistics-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/0n1xx/SpotifyStatistics)
[![Platform](https://img.shields.io/badge/Platform-Web%20%7C%20iOS-1DB954?style=flat-square)](#)

End-to-end analytics platform that continuously ingests Spotify listening history, enriches each track with geographic artist metadata via MusicBrainz, and surfaces insights across a web dashboard and a native iOS app.

- **Data pipeline** — Apache Airflow DAG runs every 3 minutes: fetches last 50 played tracks per user, resolves artist country/city via MusicBrainz, deduplicates by `played_at + user_id`, writes to ClickHouse (analytics) and SQL Server (web app)
- **Web app** — ASP.NET Core 10 + Razor Pages: Dashboard, Recently Played (paginated), World Map (D3.js), full account management, Spotify/Google/GitHub OAuth, transactional email via Resend on `statify.one`
- **iOS app** — Native SwiftUI companion with full feature parity: Dashboard, History, World Map (MapKit), Settings — connects to the same ASP.NET backend via JWT REST API
- **Admin dashboard** — Apache Superset connected directly to ClickHouse: KPI cards, activity charts, top artists/albums/songs, word cloud, raw history table
- **Infrastructure** — All services deployed on Railway; Airflow and Superset run on custom Docker images purpose-built for Railway's environment

**Stack:** Python · Apache Airflow · ClickHouse · SQL Server · ASP.NET Core C# · Vanilla JS · D3.js · Swift · SwiftUI · Docker · Railway

### Web Development

___

**SecretAgentGadgetLab**  
- ASP.NET Core MVC secret agent marketplace with Stripe payments, Cloudinary image storage, OAuth (Google & GitHub), role-based authorization, and full shopping cart. Deployed on Railway. [Live Demo](https://secret-agent-lab.up.railway.app)

**iPod Marketplace**  
- Full-stack PHP/MySQL e-commerce platform with admin CRUD panel, user authentication, image uploads, and bilingual (English/French) interface. Deployed on Railway. [Live Demo](https://ipod-marketplace.up.railway.app)

**Business Lead Finder**
- A tool to find local businesses without websites for outreach. Built with FastAPI + React + Google Places API. Deployed on Railway. [Live Demo](https://businessleadfinderfrontend-production.up.railway.app)

### 📢 Content & Community
- YouTube: [How Requirements for Junior Data Analysts Changed](https://www.youtube.com/watch?v=l23LHX4G5iM&t=2s)

### 🌐 Connect with Me
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/vladislav-sakharov-8191b2242/)

### 📊 GitHub Stats
<img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=0n1xx&theme=monokai" alt="Profile Details" />
<img src="https://komarev.com/ghpvc/?username=0n1xx&color=blueviolet" alt="Profile Views" />

Thanks for visiting! I'm always open to discussing data engineering, web development, or potential opportunities.

— Vlad
