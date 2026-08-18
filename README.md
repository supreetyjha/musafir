# 🌍 Musafir

> **Don't just visit a city. Discover its story.**

Musafir is a smart travel discovery platform that helps users explore a destination through **weather, places, culture, and books**.

Instead of simply answering *"Where should I go?"*, Musafir aims to answer:

> **"What can I discover about this city before I visit it?"**

The core idea is to connect **travel discovery with literature**, allowing users to find books, stories, historical works, travel guides, and authors associated with the city they search for.

---

## ✨ Features

### 📍 Smart City Search

Search for a city and get a centralized destination overview.

- City-based travel discovery
- Destination information
- Current weather
- Places and attractions
- Books related to the destination
- Cultural and historical information
- Personalized recommendations

---

### 🌦️ Real-Time Weather

Musafir integrates weather services to provide useful information about a searched destination.

Users can discover:

- 🌡️ Current temperature
- ☁️ Weather conditions
- 💧 Humidity
- 💨 Wind information
- 🌤️ Other relevant weather data

This helps travelers understand the conditions of a destination before planning activities.

---

# 📚 City-Based Book Recommendations

## ⭐ The Core Feature

One of Musafir's main differentiators is its **city-aware book recommendation system**.

When a user searches for a city, Musafir doesn't only recommend places to visit.

It also recommends **books connected to that city**.

For example:

```text
User searches for:

        PARIS
          │
          ▼
 ┌──────────────────────┐
 │ Destination Analysis │
 └──────────┬───────────┘
            │
     ┌──────┼──────┐
     ▼      ▼      ▼
  Weather Places  Books
                   │
                   ▼
        ┌───────────────────┐
        │ Books related to  │
        │      Paris        │
        └───────────────────┘
````

The recommendation system is intended to surface different types of literature, including:

* 📖 Books set in the city
* ✈️ Travel literature
* 🏛️ Historical books
* 🗺️ Destination guides
* 📚 Cultural literature
* ✍️ Stories connected to the location
* 👤 Works by authors associated with the city

### Example

A search for **Paris** could lead to recommendations involving:

```text
Paris
 ├── Fiction set in Paris
 ├── Historical books about Paris
 ├── Travel guides
 ├── Cultural literature
 └── Books by authors connected to Paris
```

The goal is to allow users to **experience a destination through literature before physically visiting it**.

---

# 🗺️ Place Discovery

Musafir aims to help users discover interesting locations within a searched destination.

Potential categories include:

* 🏛️ Historical landmarks
* 🖼️ Museums
* 🌳 Parks
* ⛪ Cultural locations
* 📸 Tourist attractions
* 🍽️ Restaurants
* 💎 Hidden or lesser-known places

The place discovery system will eventually work together with the book recommendation system.

For example:

```text
Search: Rome

Places
 ├── Colosseum
 ├── Pantheon
 └── Roman Forum

Books
 ├── Books about Ancient Rome
 ├── Historical fiction
 └── Travel literature
```

This creates a more immersive destination experience.

---

# 🔎 Unified Destination Experience

Musafir aims to bring multiple aspects of destination discovery into one platform.

```text
                       CITY SEARCH
                           │
                           ▼
                ┌─────────────────────┐
                │ Destination Engine  │
                └──────────┬──────────┘
                           │
          ┌────────────────┼────────────────┐
          │                │                │
          ▼                ▼                ▼
      🌦️ Weather       📍 Places        📚 Books
          │                │                │
          └────────────────┼────────────────┘
                           │
                           ▼
                  🌍 Travel Experience
```

Instead of switching between multiple platforms, users can explore:

**Weather + Places + Books + Culture**

from one destination-focused interface.

---

# 🧠 Recommendation Concept

The long-term goal is to make recommendations increasingly relevant to the searched destination.

A simplified recommendation flow:

```text
User searches for a city
          │
          ▼
Extract destination
          │
          ▼
Find books connected to destination
          │
          ▼
Filter / rank results
          │
          ▼
Display recommendations
```

Future versions can consider factors such as:

* City relevance
* Genre
* Publication information
* Author association
* Historical relevance
* User interests
* User's previous searches
* Saved books
* Ratings and reviews

This can eventually evolve into a more personalized recommendation engine.

---

# 🏗️ Architecture

Musafir follows a modular full-stack architecture.

```text
                         ┌───────────────────┐
                         │     FRONTEND      │
                         │                   │
                         │  Travel Discovery │
                         │        UI         │
                         └─────────┬─────────┘
                                   │
                                   │ REST API
                                   ▼
                         ┌───────────────────┐
                         │    SPRING BOOT    │
                         │      BACKEND      │
                         └─────────┬─────────┘
                                   │
                ┌──────────────────┼──────────────────┐
                │                  │                  │
                ▼                  ▼                  ▼
        ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
        │   Weather    │   │    Places    │   │    Books     │
        │     API      │   │     API      │   │     API      │
        └──────────────┘   └──────────────┘   └──────────────┘
                │                  │                  │
                └──────────────────┼──────────────────┘
                                   ▼
                         Destination Results
```

---

# 🛠️ Tech Stack

## Backend

* Java
* Spring Boot
* Spring Web
* Spring WebFlux
* Maven
* REST APIs

## Frontend

* React
* Vite
* JavaScript
* CSS

## External Services

* Weather API
* Book / Literature APIs
* Places / Location APIs

## Development

* Git
* GitHub
* VS Code

---

# 📂 Project Structure

```text
musafir/
│
├── backend/
│   │
│   ├── .mvn/
│   ├── mvnw
│   ├── mvnw.cmd
│   ├── pom.xml
│   │
│   └── src/
│       └── main/
│           │
│           ├── java/
│           │   └── com/
│           │       └── aphrodite/
│           │           └── travelapp/
│           │               │
│           │               ├── TravelAppApplication.java
│           │               │
│           │               ├── config/
│           │               │
│           │               ├── controller/
│           │               │
│           │               ├── dto/
│           │               │
│           │               ├── model/
│           │               │
│           │               ├── repository/
│           │               │
│           │               └── service/
│           │
│           └── resources/
│
└── frontend/
```

---

# 🔌 API Architecture

The backend exposes REST endpoints for the frontend.

Example:

```http
GET /api/weather?city=Bhopal
```

Request flow:

```text
Frontend
   │
   ▼
GET /api/weather?city=Bhopal
   │
   ▼
TravelController
   │
   ▼
WeatherService
   │
   ▼
External Weather API
   │
   ▼
Weather Response
   │
   ▼
Frontend
```

Similar endpoints will eventually be introduced for books and places.

Possible future API structure:

```text
/api
 ├── /weather
 ├── /places
 ├── /books
 ├── /recommendations
 └── /reviews
```

---

# 📚 Book Recommendation Architecture

The book recommendation system is planned as a dedicated part of the backend.

```text
                    City Search
                        │
                        ▼
                ┌───────────────┐
                │ Book Service  │
                └───────┬───────┘
                        │
                        ▼
                  Book API/Data
                        │
                        ▼
                Relevant Books
                        │
                        ▼
              Recommendation Logic
                        │
                        ▼
                 Ranked Results
                        │
                        ▼
                    Frontend
```

The system can eventually support multiple recommendation categories:

```text
                 BOOKS
                   │
        ┌──────────┼──────────┐
        │          │          │
        ▼          ▼          ▼
     Fiction    History     Travel
        │          │          │
        └──────────┼──────────┘
                   │
                   ▼
            City Relevance
                   │
                   ▼
             Recommendations
```

---

# 🚀 Development Roadmap

## Phase 1 — Project Foundation

* [x] Repository setup
* [x] Frontend structure
* [x] Spring Boot backend
* [x] Maven configuration
* [x] REST API structure
* [x] Service architecture

## Phase 2 — Weather

* [x] Weather service foundation
* [x] Weather controller
* [x] External API communication
* [ ] Secure API key configuration
* [ ] Error handling
* [ ] Weather response DTO
* [ ] Input validation

## Phase 3 — Books

* [ ] Book API integration
* [ ] City-based book search
* [ ] Book response DTO
* [ ] Book recommendation service
* [ ] Relevance ranking
* [ ] Book recommendation UI

## Phase 4 — Places

* [ ] Places API integration
* [ ] Attraction search
* [ ] Location-based results
* [ ] Place categories
* [ ] Place details

## Phase 5 — Frontend Integration

* [ ] Connect frontend with backend
* [ ] City search interface
* [ ] Weather cards
* [ ] Places section
* [ ] Book recommendation section
* [ ] Loading states
* [ ] Error states
* [ ] Responsive design

## Phase 6 — Personalization

* [ ] User accounts
* [ ] Saved destinations
* [ ] Saved books
* [ ] Favorite places
* [ ] User preferences
* [ ] Personalized recommendations

## Phase 7 — Security

* [ ] Environment-based secrets
* [ ] Input validation
* [ ] Authentication
* [ ] Authorization
* [ ] Secure API communication
* [ ] CORS configuration
* [ ] Rate limiting
* [ ] Dependency security checks
* [ ] Security testing
* [ ] VAPT
* [ ] Production security review

## Phase 8 — Deployment

* [ ] Production configuration
* [ ] Backend deployment
* [ ] Frontend deployment
* [ ] Environment configuration
* [ ] Monitoring
* [ ] Final security review

---

# 🔐 Security

Security is intended to be an integral part of Musafir's development rather than something added only before deployment.

Planned practices include:

### 🔑 Secret Management

API keys and other secrets will be stored using environment variables.

```text
Environment Variable
        ↓
Spring Configuration
        ↓
Service Layer
        ↓
External API
```

Secrets should never be committed to GitHub.

### 🛡️ Application Security

Planned security measures include:

* Input validation
* Secure API communication
* Proper error handling
* CORS configuration
* Authentication
* Authorization
* Rate limiting
* Dependency vulnerability checks
* Secure secret management
* VAPT
* Security testing before deployment

---

# 🧪 Development Status

Musafir is currently under active development.

### Current milestone

**Backend Foundation + External API Integration**

The Spring Boot backend is operational locally.

Current backend functionality includes the foundation for:

```text
City Search
     │
     ▼
Weather Service
     │
     ▼
External Weather API
```

The next major development milestone is the **city-based book recommendation system**.

---

# 🎯 Project Vision

Traditional travel applications primarily focus on:

> **Where to go and what to do.**

Musafir aims to explore another question:

> **How can you understand a place before you visit it?**

A destination isn't just a collection of tourist attractions.

It has:

* Stories
* History
* Literature
* Culture
* People
* Weather
* Places
* Experiences

Musafir aims to connect these elements into a single destination discovery experience.

---

# 💡 What Makes Musafir Different?

The central idea behind Musafir is the connection between:

```text
        TRAVEL
          │
          ├──────── Weather
          │
          ├──────── Places
          │
          ├──────── Culture
          │
          └──────── Literature
                       │
                       ▼
                BOOK DISCOVERY
```

The **city-based book recommendation feature** is especially important because it transforms travel planning from simply finding locations into discovering the **identity and stories of a destination**.

Instead of:

> "Here are 10 places to visit in Paris."

Musafir aims to eventually provide:

> "You're interested in Paris. Here are places to explore, today's weather, and books that can help you understand the city before you arrive."

---

# 📈 Future Possibilities

The platform can eventually evolve toward a more intelligent travel recommendation system.

Potential future capabilities include:

* AI-powered destination recommendations
* Personalized book recommendations
* Context-aware travel suggestions
* User preference learning
* Itinerary generation
* Book-to-place connections
* Place-to-book recommendations
* Cultural exploration
* Natural-language travel search

For example:

```text
User:

"I want to visit a historical city in winter
and read something related to its culture."

                         ↓

                Musafir Recommendation
                         ↓
              ┌──────────────────────┐
              │ Destination          │
              │ Weather              │
              │ Places               │
              │ Historical sites     │
              │ Related books        │
              └──────────────────────┘
```

---

# 💻 Running Locally

## Backend

Navigate to the backend:

```bash
cd backend
```

Build the project:

```bash
./mvnw clean package
```

Run Spring Boot:

```bash
./mvnw spring-boot:run
```

The backend runs on:

```text
http://localhost:8080
```

Example endpoint:

```text
http://localhost:8080/api/weather?city=Bhopal
```

---

# ⚙️ Environment Variables

API keys should be provided through environment variables.

Example:

```bash
export WEATHER_API_KEY="your-api-key"
```

Never commit actual API keys to the repository.

For Windows PowerShell:

```powershell
$env:WEATHER_API_KEY="your-api-key"
```

For Windows Command Prompt:

```cmd
set WEATHER_API_KEY=your-api-key
```

---

# 🤝 Contributing

Musafir is currently a personal development project, but contributions, suggestions, and ideas are welcome.

If contributing:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test the changes
5. Commit your work
6. Open a pull request

Example:

```bash
git checkout -b feature/book-recommendations
```

---

# 📌 Current Focus

The immediate development priorities are:

```text
1. Secure Weather Integration
          ↓
2. Book API Integration
          ↓
3. City-Based Book Recommendations
          ↓
4. Places Integration
          ↓
5. Frontend Integration
          ↓
6. Personalization
          ↓
7. Security Testing
          ↓
8. Deployment
```

---

# 👩‍💻 Author

## Supreety Jha

Cybersecurity & Software Engineering Student

Interested in:

* Cybersecurity
* Secure Software Development
* Cryptography
* Artificial Intelligence & Machine Learning
* Full-Stack Development
* Security Engineering

---

# ⭐ Musafir

**Travel is more than a destination.
It's the stories, places, people, and ideas connected to it.**

> **Don't just visit a city. Discover its story.**

```
```
