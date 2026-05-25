📊 Real-Time Sales Operations Dashboard — Automated Control Desk
Eliminated the need for a manual control desk operator by building a real-time dashboard that automatically reroutes agents across campaigns based on live performance metrics.

🧩 The Problem
A telecom outbound sales operation running 17,000+ daily calls across multiple supervisors and campaigns required constant manual intervention:

Operators had to monitor conversion rates, queue size, occupancy, and pause time hourly
Rerouting decisions (moving agents between campaigns or VPL routes) were made manually by a control desk team
Delays in rerouting meant wasted capacity and lost revenue
The goal: automate all of this so the operation runs itself.

⚙️ Solution Overview
A real-time HTML dashboard that:

Pulls live data from SQL databases and an internal Google Sheets
Displays KPIs per supervisor, per hour, with conversion rates and call volume
Projects end-of-day closing numbers based on historical and current pace
Triggers automatic rerouting of agents across campaigns when metrics fall below defined thresholds
SQL Database ──────────┐
                        ├──→ Python backend → HTML Dashboard (real-time)
Google Sheets API ─────┘          ↓
                           Rerouting Engine
                                  ↓
                      Automatic campaign/VPL reassignment
🛠️ Tech Stack
Layer	Tool
Frontend	HTML, CSS, JavaScript
Data Sources	SQL (live queries) + Google Sheets API
Backend	Python
Automation	Claude Code (AI-assisted development in VSCode)
Hosting	Internal network
📊 Dashboard Features
KPI Cards (real-time)
Tabuladas — confirmed sales from SQL
Não Tabuladas — pending sales from Forms
Total Vendas — combined with conversion rate
Chamadas Atendidas — live call volume with hours remaining
Projeção Fechamento — end-of-day forecast vs. historical baseline
Supervisor × Hour Grid
Each cell shows sales count + conversion rate per hour
Color-coded by performance (green = strong, yellow = average, red = underperforming)
Campaign filter to isolate individual operations
Auto-Refresh
One-click refresh pulling latest SQL and Sheets data
Designed for continuous display on operations floor screens
🤖 Rerouting Automation
The system monitors the following metrics in real time and triggers agent reassignment automatically:

Metric	Threshold Action
Low conversion rate	Move agents to higher-performing campaign
Low occupancy	Redistribute to busier queues
Excessive pause time	Flag supervisor + rebalance load
Queue buildup	Pull agents from low-volume campaigns
VPL route underperformance	Switch to alternative paid route
This replaced the work of a dedicated control desk operator monitoring these metrics manually throughout the day.

📈 Results
Metric	Value
Daily calls monitored	17,000+
Supervisors tracked	6+
Manual control desk replaced	1 full-time operator
Rerouting decisions automated	Continuous throughout 9h–21h shift
Data sources integrated	SQL + Google Sheets (real-time)
💡 Key Takeaways
SQL + Sheets in one view — bridging structured DB data with operational spreadsheets is a common enterprise pain point, solved here cleanly
Projection engine — forecasting end-of-day numbers from current pace + historical conversion is directly applicable to any sales operation
AI-assisted development — built using Claude Code integrated with VSCode, accelerating development without compromising on functionality or reliability
📬 Contact
Built by [Your Name] · [LinkedIn] · [Email]
Open to remote opportunities in Revenue Operations, Sales Analytics, and Data Engineering.
