# StreamKeeper - Full Stack Media Application

## Overview
StreamKeeper is a full-stack application designed for movie and TV show enthusiasts to explore, search, and learn about their favorite content using The Movie Database (TMDb) API. The solution combines a Node.js backend API and a React frontend interface to deliver a seamless and dynamic user experience with robust functionality for discovering movies, TV shows, and related content.

## Key Features

### Backend (Node.js API)
- **Multi-Server Architecture**: Separate endpoints for movies, TV shows, persons, and general TMDb queries, enhancing modularity and scalability.
- **Swagger-Documented Endpoints**: Provides user-friendly documentation for exploring and testing available routes.
- **Flexible Search**: Powerful search functionality to query movies, TV shows, and persons with optimized query handling.
- **Comprehensive Error Handling**: Ensures seamless API responses and user experience.
- **Health Check Routes**: Easy monitoring and validation of API status.

### Frontend (React)
- **Responsive Design**: Adapts gracefully to desktops, tablets, and mobile devices, offering a consistent user experience.
- **Real-Time Search**: Interactive search bar to quickly find movies, TV shows, and people, providing instant results.
- **Detailed Media Pages**: Access in-depth information, ratings, reviews, trailers, and related content for each movie and show.
- **Efficient Caching Mechanism**: Reduces redundant API calls, improving load times and user experience.
- **User-Friendly Navigation**: Intuitive design with clear navigation links for browsing content, searching, and viewing specific details.

## Technology Stack
- **Backend**: Node.js, Express.js, Axios for API requests, and Swagger for API documentation.
- **Frontend**: React with Context API for state management, Axios for API calls, Jest, and React Testing Library for testing.
- **Additional Tools**: dotenv for environment variables (backend) and modern CSS for styling (frontend).

## Project Structure

### Backend Structure
- `controllers/`: Handles request logic for movies, TV shows, persons, etc.
- `helpers/`: Utility functions for TMDb API interactions.
- `models/`: Data models for Media, Movie, TVShow, Person, and Review.
- `routes/`: Route definitions for different API functionalities.
- `swagger/`: Configuration for generating Swagger documentation.

### Frontend Structure
- `components/`: Reusable React components like Navbar, SearchBar, DisplayCards, etc.
- `pages/`: Page components for Home, Browse, Movie/TV Details, etc.
- `services/`: Handles API calls and data fetching.
- `cache/`: Implements caching for improved performance.

## Getting Started

### Prerequisites
- Node.js (version >= 12.x recommended)
- npm (Node Package Manager)

### Installation

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   ```
2. **Navigate to project directories and install dependencies:**
   - **Backend:**
     ```bash
     cd streamkeeper-node-backend
     npm install
     ```
   - **Frontend:**
     ```bash
     cd streamkeeper-react
     npm install
     ```
3. **Set up environment variables (Backend):**
   Create a `.env` file:
   ```plaintext
   TMDB_API_KEY=your_tmdb_api_key
   TMDB_BASE_URL=https://api.themoviedb.org/3
   ```
   Replace `your_tmdb_api_key` with a valid TMDb API key.

4. **Run the applications:**
   - **Backend:**
     ```bash
     node index.js
     ```
   - **Frontend:**
     ```bash
     npm start
     ```
   Access the frontend at `http://localhost:3000`.

## Available Routes

### Backend Routes
- **General TMDb Routes** (`/api`): Health checks, API key validation, etc.
- **TV Show Routes** (`/api/tv`): Popular shows, search, details, etc.
- **Movie Routes** (`/api/movies`): Popular movies, search, details, etc.
- **Person Routes** (`/api/person`): Popular persons, search, details, etc.

### Frontend Routes
- `/`: Home Page
- `/browse`: Browse Page
- `/movie/:id`: Movie Detail Page
- `/tv/:id`: TV Show Detail Page
- `/search`: Search Results Page

## Testing
- **Backend**: Use Jest for testing API routes and business logic.
- **Frontend**: Jest and React Testing Library for component and UI testing.

