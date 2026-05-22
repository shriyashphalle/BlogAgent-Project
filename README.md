# BlogAgent-Project
BlogAgent is an advanced multi-agent system built with LangGraph, LangChain, and Gemini Models that automates technical blog writing.
BlogAgent intelligently decides whether your topic requires real-time web research, drafts structural execution plans, branches out into parallel section-writing tasks, and automatically inserts custom AI-generated diagrams into the final text.

---

### Core Pipeline Execution Steps

1. **Dynamic Routing (`router`):** Evaluates the query scope and tags it under a specific mode: `closed_book` (evergreen topics), `hybrid` (concepts needing recent examples), or `open_book` (highly volatile, timely news).
2. **Autonomous Research (`research`):** Orchestrates deep web scraping queries via the Tavily Search API. It extracts and filters relevant evidence relative to a context time-window set up by the router.
3. **Logistical Planning (`orchestrator`):** Structures a serialized `Plan` layout mapping out targeted word counts, structural configurations, and technical dependencies.
4. **Asynchronous Section Composition (`worker`):** Triggers a map-reduce style scatter-gather fan-out pattern. Parallel tasks compile each dedicated section independently while strictly honoring factual evidence constraints and citation hyperlinks.
5. **Image Composition Engine (`reducer`):** Passes the consolidated markdown layout to a media sub-graph node that plans functional, explanatory diagrams and provisions imagery generation using `gemini-2.5-flash-image`.

---

## ✨ Features

* **Multi-Agent Coordination:** Complete asynchronous parallel processing natively driven by LangGraph state machines.
* **Smart Citations:** Automatically applies inline source links back to scraped reference domains during factual composition.
* **Integrated Media Pipeline:** Proposes relevant visual diagram descriptions, embeds positional anchors, generates high-fidelity illustrations, and serves complete local rendering paths.
* **Production Workspace Interface:** A sleek Streamlit UI mapping operational logs, live state variables, and execution analytics across tabular panels.
* **Persistent Markdown Cache:** Instantly scans workspace directories for old files to let you browse or re-load previous outputs with a single click.
* **Dynamic Bundling Export:** Package down your completed articles along with all localized PNG assets directly into a singular, structured `.zip` deployment archive.


