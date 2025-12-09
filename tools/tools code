import os
import requests
from langchain.tools import tool
from dotenv import load_dotenv

load_dotenv()

# ------------------------
# WEATHER TOOL
# ------------------------
@tool
def get_weather(city: str):
    """Fetch weather information for a city."""
    url = "https://open-weather13.p.rapidapi.com/city/" + city

    headers = {
        "x-rapidapi-key": os.getenv("WEATHER_API_KEY"),
        "x-rapidapi-host": "open-weather13.p.rapidapi.com"
    }

    response = requests.get(url, headers=headers)
    return response.json()


# ------------------------
# HOTEL TOOL
# ------------------------
@tool
def get_hotels(city: str):
    """Fetch hotels for a given city."""
    url = "https://tripadvisor16.p.rapidapi.com/api/v1/hotels/searchHotels"

    querystring = {"query": city}

    headers = {
        "x-rapidapi-key": os.getenv("HOTEL_API_KEY"),
        "x-rapidapi-host": "tripadvisor16.p.rapidapi.com"
    }

    response = requests.get(url, headers=headers, params=querystring)
    return response.json()


# ------------------------
# ATTRACTIONS TOOL
# ------------------------
@tool
def get_attractions(city: str):
    """Fetch attractions for a city using Foursquare Places API."""
    url = "https://api.foursquare.com/v3/places/search"

    params = {
        "query": "attractions",
        "near": city,
        "limit": 5
    }

    headers = {
        "Accept": "application/json",
        "Authorization": os.getenv("PLACES_API_KEY")
    }

    response = requests.get(url, headers=headers, params=params)
    return response.json()


# ------------------------
# FLIGHTS TOOL
# ------------------------
@tool
def get_flights(city: str):
    """Fetch flights to a destination city."""
    url = "https://kiwi-flight-search.p.rapidapi.com/flights"

    querystring = {"dest": city, "curr": "USD"}

    headers = {
        "x-rapidapi-key": os.getenv("FLIGHTS_API_KEY"),
        "x-rapidapi-host": "kiwi-flight-search.p.rapidapi.com"
    }

    response = requests.get(url, headers=headers, params=querystring)
    return response.json()


# ------------------------
# BUDGET TOOL
# ------------------------
@tool
def estimate_budget(amount: float):
    """Simple budgeting helper."""
    return f"Estimated trip cost is approximately ${amount:.2f}."
