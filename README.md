# 🌍 **Agentic Travel Planner — LangChain + Groq + External APIs**

An intelligent travel assistant that uses **LangChain agents**, **tool calling**, and **multiple real APIs** to autonomously gather weather, hotels, attractions, and flight data — then creates a **3-day travel itinerary**.

---

# 🚀 **1. Installation Guide**

## ✅ **Step 1 — Clone the repository**

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
```

## ✅ **Step 2 — Create a virtual environment (optional but recommended)**

```bash
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows
```

## ✅ **Step 3 — Install dependencies**

Install everything needed to run the agent:

```bash
pip install -r requirements.txt
```

If you don’t have a `requirements.txt` yet, use the one below:

```
langchain
langchain-core
langchain-community
langchain-openai
langchain-groq
openai
requests
python-dotenv
pydantic
gradio
groq
tavily-python
```

---

# 🔑 **2. API Keys Configuration**

Create a `.env` file in the project root:

```bash
touch .env
```

Add all your API keys (without exposing real values):

```
GROQ_API_KEY=your_key_here
WEATHER_API_KEY=your_key_here
HOTEL_API_KEY=your_key_here
PLACES_API_KEY=your_key_here
FLIGHTS_API_KEY=your_key_here
```

➡️ **Do NOT upload your actual keys to GitHub.**
➡️ Add `.env` to `.gitignore`.

---

# 🧠 **3. How to Run the Agent**

## ▶️ **Option 1 — Run From Terminal (CLI Mode)**

```bash
python app.py
```

You will see:

```
Enter your travel query:
```

Example:

```
Plan a 3-day trip to London including weather, hotels, flights, and attractions.
```

The agent will automatically:

* Call weather API
* Call hotels API
* Call attractions API
* Call flights API
* Merge all data
* Return a formatted 3-day itinerary

---

## ▶️ **Option 2 — Run the Gradio Web App**

```bash
python gradio_app.py
```

You will get a local URL like:

```
Running on http://127.0.0.1:7860/
```

Open in your browser and chat with the travel agent.

---

# 💬 **4. Example Queries You Can Try**

Try these:

### **Basic**

```
Plan a 3-day trip to Dubai.
```

### **Detailed**

```
Plan a 3-day trip to Istanbul including weather, hotels, flight cost, attractions, and budget estimation.
```

### **Different Cities**

```
What are the hotel options, weather, and attractions in Kuala Lumpur?
```

### **Flight-focused**

```
Find flight prices from Pakistan to Toronto and give suggestions.
```

### **Full Travel Plan**

```
Give me weather, hotels, flight prices, attractions, and a full itinerary for Paris.
```

---

# 🧩 **5. Tools Used by the Agent**

Your LangChain agent uses these APIs wrapped as tools:

| Tool Name         | Description                       | API Source            |
| ----------------- | --------------------------------- | --------------------- |
| `get_weather`     | Gets weather for a city           | OpenWeather RapidAPI  |
| `get_hotel`       | Searches hotel locations & prices | Tripadvisor RapidAPI  |
| `get_places`      | Shows top attractions             | Foursquare Places API |
| `get_flights`     | Gets flight prices                | Kiwi Flights RapidAPI |
| `estimate_budget` | Simple trip cost calculator       | Local tool            |

The agent automatically decides which tools to call and in what order.

---

# 🔍 **6. Project Flow (Simplified)**

```
User Query →
Agent Planning →
Weather Tool →  
Hotel Tool →  
Places Tool →  
Flights Tool →  
Budget Tool (optional) →
Agent Merges All Data →
Final 3-Day Itinerary
```

# 📦 **8. Folder Structure**

```
project/
│── app.py
│── tools.py
│── agent_setup.py
│── gradio_app.py
│── .env
│── requirements.txt
│── README.md
└── .gitignore
```

---

