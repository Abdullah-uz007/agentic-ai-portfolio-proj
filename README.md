# 🌍 **Agentic Travel Planner**

### *AI-powered multi-tool travel assistant using LangChain + Groq + real-world APIs*

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10%2B-blue?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/LangChain-Agentic-brightgreen?logo=chainlink" />
  <img src="https://img.shields.io/badge/Groq-UltraFastLLM-orange?logo=groq" />
  <img src="https://img.shields.io/badge/External_APIs-4-purple" />
  <img src="https://img.shields.io/badge/Interface-CLI%20%7C%20Gradio-ff69b4" />
  <img src="https://img.shields.io/badge/Status-Complete-success" />
  <img src="https://img.shields.io/badge/License-MIT-lightgrey" />
</p>

---

# ✨ **Overview**

The **Agentic Travel Planner** is an advanced AI assistant that uses **LangChain’s agent framework** and **Groq’s ultra-fast inference** to autonomously:

✔ Fetch weather data
✔ Retrieve hotel options
✔ Discover attractions
✔ Fetch flight details
✔ Estimate cost
✔ Produce a final **3-day beautifully formatted itinerary**

This project demonstrates **true agentic workflow** — planning, tool selection, multi-step API calling, reasoning, and final structured response generation.

---

# 🚀 **Features**

### 🧠 **Intelligent Agentic Reasoning**

* Dynamic planning
* Multi-step tool execution
* Autonomous decision-making

### 🌐 **Real External APIs**

| Feature     | API                      | Badge                                                     |
| ----------- | ------------------------ | --------------------------------------------------------- |
| Weather     | OpenWeather13 (RapidAPI) | ![](https://img.shields.io/badge/WeatherAPI-Active-blue)  |
| Hotels      | TripAdvisor (RapidAPI)   | ![](https://img.shields.io/badge/HotelsAPI-Active-orange) |
| Attractions | Foursquare Places API    | ![](https://img.shields.io/badge/PlacesAPI-Active-purple) |
| Flights     | Kiwi.com (RapidAPI)      | ![](https://img.shields.io/badge/FlightsAPI-Active-green) |

### ⚡ **Powered by Groq**

* Uses `openai/gpt-oss-20b` via Groq’s fast LPU engine
* Near-instant responses

### 💻 **Two Interfaces**

* 🖥 **CLI Mode**
* 🌐 **Gradio Web App**

### 📄 **Clean 3-Day Itinerary Output**

* Markdown formatted
* Hotels + weather + flights combined
* Day-by-day plan

---

# 📦 **Project Structure**

```
project/
│── app.py                 # CLI agent interface
│── gradio_app.py          # Optional Gradio UI
│── tools.py               # All tools (weather/hotel/flights/places/budget)
│── requirements.txt
│── README.md
│── .env.example
└── .gitignore
```

---

# 🔑 **API Keys Configuration**

Create a `.env` file:

```
GROQ_API_KEY=your_key_here
WEATHER_API_KEY=your_key_here
HOTEL_API_KEY=your_key_here
PLACES_API_KEY=your_key_here
FLIGHTS_API_KEY=your_key_here
```

⚠️ Do NOT upload real keys to GitHub.

---

# ⚙️ **Installation**

### 1️⃣ Clone the repository

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

### 2️⃣ Install requirements

```bash
pip install -r requirements.txt
```

### 3️⃣ Add your `.env` file

(Use `.env.example` as a template)

---

# ▶️ **Run the Travel Agent**

### **CLI Mode**

```bash
python app.py
```

Example prompt:

```
Plan a 3-day trip to London including weather, hotels, flights, and attractions.
```

---

### **Gradio Web App**

```bash
python gradio_app.py
```

Open the local URL shown in terminal.

---

# 💬 **Example Prompts**

Try these:

🌴 *“Plan a 3-day trip to Dubai with weather and hotel suggestions.”*
🛫 *“Find flights and budget for a 3-day trip to Toronto.”*
🎡 *“Get attractions, hotel prices, and a day-wise itinerary for Paris.”*
🌦 *“What is the weather and best hotels in Kuala Lumpur?”*

---

# 🎯 **Agent Workflow**

```
User Query →
Agent Planning →
Weather API →
Hotel API →
Places API →
Flights API →
(Optionally Budget Tool) →
Final Formatted 3-Day Itinerary
```

---

# 🏆 **Why This Project Stands Out**

* Uses **multiple API tools** (4 external APIs + 1 local tool)
* Demonstrates **LangChain agentic reasoning**
* Integrates **Groq LLM** for insane speed
* Includes both **CLI & UI**
* Professional structure suitable for assignment & portfolio

