# 📊 OpenInsights - Open Source Dashboard for Power BI Backends

**OpenInsights** is an open-source, real-time business intelligence dashboard developed as an industry project at **e-Zest (An Accion Labs Company), Pune**. It acts as an alternative to proprietary BI tools like Power BI and Tableau by using the **Power BI REST API** to fetch data and render dynamic visualizations via modern web technologies.

---

## 🚀 Key Features

- 🔌 **Power BI Integration** — Fetches datasets via Power BI REST API (JSON format)
- 📈 **Interactive Visualizations** — Bar, Line, Pie, and Scatter charts using Chart.js & Apache ECharts
- 🔄 **Real-Time Updates** — Live data streaming with WebSockets (Socket.IO)
- 🌗 **Light/Dark Mode**, Full/Single chart toggling, Manual testing mode
- 🧠 **Future Scope** — Integration with Retrieval-Augmented Generation (RAG) for AI-powered Q&A

---

## 🛠️ Tech Stack

| Category       | Technology Used                              |
|----------------|-----------------------------------------------|
| Frontend       | React, Chart.js, Apache ECharts, Tailwind CSS |
| Backend        | Node.js, Express.js                           |
| Real-Time Data | WebSockets (Socket.IO)                        |
| Data Source    | Power BI REST API (JSON)                      |
| AI Integration (Planned) | OpenAI, Hugging Face, FAISS, Pinecone       |

---

## 🧱 Architecture Overview

```plaintext
Power BI API --> Node.js/Express --> React Frontend
      ▲                ▲                 ▲
Real-time Data     WebSocket         Chart.js, ECharts
(Backend Push)     (Socket.IO)       Dynamic UI
```

📂 Implementation
Backend (Node.js + Express)
/api/data – Fetch Power BI JSON data

/api/simulate-update – Manually trigger updates for testing

/health – Server status check

WebSocket server for broadcasting real-time updates

Frontend (React)
Real-time chart updates via WebSocket

UI includes toggle for dark/light mode

Charts built using Chart.js, Apache ECharts

"Simulate Update" button for testing live changes

🔮 Future Enhancements
💬 Natural Language Q&A (RAG):

Users ask: “Show sales for Q2 2024”

System fetches relevant Power BI data and generates a textual/visual response

📊 Advanced Analytics:

Forecasting sales trends

Anomaly/outlier detection

👥 Multi-Tenant Support:

Role-based access (Admin, Analyst, Viewer)

Custom dashboards per user

⚠️ Challenges & Solutions
Challenge	Solution
Power BI API rate limiting	Implemented caching and batch fetches
Real-time sync delays	Optimized WebSocket payloads
Large data lag	Used React-Window for virtual scrolling
Chart inconsistency across browsers	Unified with Apache ECharts

👥 Team: [Omkar More], [Prathamesh Medage,Sanika Maind,Aditi Mali,Janhavi Maske] (e-Zest / Accion Labs)

🙌 Contributions
We welcome pull requests and feature suggestions!
Fork the repo, create a branch, and submit your improvements.

📬 Contact
For any queries or feedback, feel free to open an issue or reach out via GitHub.

