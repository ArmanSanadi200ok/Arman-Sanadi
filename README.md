<h1 align="center">Hi there, I'm Arman 👋</h1>
<h3 align="center">🔥 Python Developer | Django | AI Integration | Backend Enthusiast</h3>

<p align="center">
  <img src="https://img.shields.io/badge/Python-Expert-blue?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Django-Learning-green?logo=django&logoColor=white" />
  <img src="https://img.shields.io/badge/AI%20Integration-OpenAI-orange?logo=openai&logoColor=white" />
  <img src="https://img.shields.io/badge/Backend%20Developer-Passionate-purple" />
</p>

---

## 🚀 About Me
- 👨‍💻 Founder at **Devloryx Technologies**  
- 🤖 Integrating **OpenAI API** into real-world applications  
- 📚 Learning **Django**, **Python Automation**, **REST APIs**, **AI Assistanted engg.**
- 🎯 Aspiring **Backend + AI Developer**  
- ☕ Code. Learn. Build. Repeat.  

---

## 🛠️ Tech Stack
### 🔥 Languages
- 🐍 Python  
- 🌐 JavaScript
- 💻 C / C++ (Basic)

### ⚙️ Backend
- 🧩 Django  
- 🌶️ Flask (Basics)

### 🎨 Frontend
- 🧱 HTML  
- 🎨 CSS  
- 💨 TailwindCSS  

### 🤖 AI & Automation
- ⚡ OpenAI API  
- 💬 Chatbot Development

### 🗄️ Databases
- 🛢️ MySQL  
- 🧩 SQLite  

---

## 📊 GitHub Stats

<div align="center">

![Stats](https://github-readme-stats.vercel.app/api?username=armansanadi200ok&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true&rank_icon=github)

![Streak](https://github-readme-streak-stats.herokuapp.com/?user=armansanadi200ok&theme=tokyonight&hide_border=true)

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=armansanadi200ok&layout=compact&theme=tokyonight&hide_border=true&langs_count=8)

</div>

---

## 🌐 Connect With Me
<p align="left">
<a href="https://instagram.com/mr_arman_____09" target="_blank">
  <img src="https://img.shields.io/badge/Instagram-Follow-red?logo=instagram" />
</a>

<a href="https://www.linkedin.com/in/armansanadi" target="_blank">
  <img src="https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin" />
</a>

<a href="https://arman-sanadi-portf.netlify.app" target="_blank">
  <img src="https://img.shields.io/badge/My-Portfolio-7F5AF0?style=for-the-badge&logo=netlify&logoColor=white" alt="Portfolio" />
</a>

<a href="https://devloryx.vercel.app" target="_blank">
  <img src="https://img.shields.io/badge/Founder-Arman%20Sanadi-purple?style=for-the-badge&logo=github&logoColor=white" />
</a>
</p>

---

## ⭐ Fun Quote
> *“Code is like humor — when you have to explain it, it’s bad.”*

---

## 🏆 Thanks for Visiting!
⭐ Don’t forget to **follow** if you like my work!



Viewed registry.ts:1-193
Viewed route.ts:1-98
Edited registry.ts
Edited route.ts
Ran command: `npx tsc --noEmit; npm run build`
Used tool: schedule
Used tool: manage_task
Used tool: schedule
Used tool: manage_task
Used tool: schedule
Used tool: manage_task
Used tool: schedule
Used tool: manage_task
Used tool: schedule

I have completed the targeted fix for the decommissioned Groq model issue exactly as requested.

### Files Changed:
1. **`src/lib/ai/registry.ts`**
   - Replaced `mixtral-8x7b-32768` with `openai/gpt-oss-20b` in the Groq provider's `defaultModels` array. This ensures that any newly created projects that select Groq will correctly receive the new supported model out-of-the-box.
   
2. **`src/app/api/generate/route.ts`**
   - Implemented an automatic server-side fallback condition: `if (providerId === "groq" && modelId === "mixtral-8x7b-32768")`. If a user launches the Workspace for an older existing project that still has the decommissioned Mixtral model stored in the database, the server will invisibly route their request through `openai/gpt-oss-20b` instead, completely avoiding a Provider Error.

### Verification:
- **Scope check**: No changes were made to authentication, API key storage/encryption, UI layouts, the database schema, or the underlying SSE streaming architecture.
- **Type check**: `npx tsc --noEmit` passed cleanly.
- **Production build**: `npm run build` compiled successfully without any errors. 

The fix is safe and ready to be committed!
