# Fantasy Premier League Application

A full-stack fantasy football application inspired by the official Premier League Fantasy Football game. This project allows users to create teams, select players, view fixtures, track statistics, and compete in a leaderboard.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Setup Instructions](#setup-instructions)
- [API Endpoints](#api-endpoints)
- [Authentication](#authentication)
- [Future Enhancements](#future-enhancements)


## Overview

This application is a full-stack fantasy football manager that fetches real-time data from the Premier League API. Users can sign up, create teams, add/remove players, view upcoming fixtures, track player statistics, and compete with other users on a leaderboard.

## Features

- **User Authentication**: Sign up, login, and JWT-based authentication
- **Team Management**: Create teams and manage players
- **Player Market**: Browse and add players to your team
- **Transfer Budget System**: Manage your transfer budget when adding/removing players
- **Fixtures**: View upcoming and past fixtures with results
- **Statistics**: Track player performance metrics (goals, assists, saves)
- **Leaderboard**: Compete with other users based on player performance
- **Responsive Design**: Mobile-friendly user interface

## Technology Stack

### Backend
- Java
- Spring Boot
- Spring Security
- Spring Data JPA
- JWT Authentication
- RESTful API
- PostgreSQL (or your chosen database)

### Frontend
- React.js
- React Router
- Axios for API requests
- CSS for styling
- React Pagination
- Local Storage for user sessions

## Project Structure

### Backend Components
- **Models**: User, Player
- **Controllers**: User, Player, Auth, Data
- **Repositories**: User, Player
- **Services**: User, Player
- **Security**: JWT implementation

### Frontend Components
- **Components**: Team, Player, Fixtures, Stats, LeaderBoard
- **Containers**: HomeContainer
- **Services**: auth.service.js
- **Styles**: CSS files for components

## Setup Instructions

### Prerequisites
- Java JDK 11+
- Node.js and npm
- Maven
- PostgreSQL (or your preferred database)

### Backend Setup
1. Clone the repository
   ```
   git clone https://github.com/shashank_njr10/fantasy-league-api.git
   ```

2. Configure database
   - Create a PostgreSQL database
   - Update `application.properties` with your database credentials

3. Build and run the Spring Boot application
   ```
   mvn clean install
   mvn spring-boot:run
   ```
   The backend will run on http://localhost:8080

### Frontend Setup
1. Navigate to the frontend directory
   ```
   cd fantasy-league-frontend
   ```

2. Install dependencies
   ```
   npm install
   ```

3. Start the React application
   ```
   npm start
   ```
   The frontend will run on http://localhost:3000

## API Endpoints

### Authentication
- `POST /auth/login` - User login
- `POST /user` - Register new user

### Users
- `GET /user` - Get all users
- `POST /user` - Create new user
- `PUT /user/addPlayer` - Add player to user team
- `PUT /user/removePlayer` - Remove player from user team

### Players
- `GET /players` - Get all players
- `POST /players` - Add new player
- `GET /players/{id}` - Get player by ID

### Data
- `GET /data/players` - Get Premier League players data
- `GET /data/fixtures` - Get Premier League fixtures data

## Authentication

The application uses JWT (JSON Web Token) for authentication:
1. User logs in with email/password
2. Server validates credentials and returns a JWT token
3. Client stores token in localStorage
4. Token is included in Authorization header for protected requests

## Future Enhancements

- Player substitution system
- Live score updates
- Chat functionality between users
- Advanced statistics and visualizations
- Mobile app version
