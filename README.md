# Fitness Tracker: Personal Fitness and Sports Tracker

FitTrack is a Java-based web application designed to help users log, monitor, and analyze their fitness activities and sports performance. It provides tools to set fitness goals, track progress, and visualize performance trends, making it an excellent companion for athletes and fitness enthusiasts alike.

------------------------------

## Main Features
- **User Management**: Create and manage user profiles with personal details and fitness goals.
- **Activity Tracking**: Log activities such as running, cycling, swimming, or gym workouts, with data on distance, duration, and calories burned.
- **Goal Setting**: Set fitness goals (e.g., "Run a marathon in 6 months") and track progress.
- **Reports and Analytics**: Generate reports on performance trends and visualize progress with charts.

------------------------------

## Stack

### Backend
- **Programming Language**: Java
- **Framework**: Spring Boot (REST API development)
- **Database**: PostgreSQL/MySQL (using Spring Data JPA for ORM)
- **Authentication**: JWT-based authentication for user security

### Frontend
- **Framework**: React.js 
- **Visualization**: Chart.js for reports and graphs
- **Styling**: Tailwind CSS 

### DevOps
- **Version Control**: Git and GitHub
- **Deployment**: Dockerized setup for local development and deployment

------------------------------

## API Endpoints

### User Management
| Method | Endpoint        | Description                  |
|--------|-----------------|------------------------------|
| POST   | `/users`        | Create a new user            |
| GET    | `/users/{id}`   | Retrieve user details        |
| PUT    | `/users/{id}`   | Update user information      |
| DELETE | `/users/{id}`   | Delete user profile          |

### Activity Management
| Method | Endpoint         | Description                   |
|--------|------------------|-------------------------------|
| POST   | `/activities`    | Log a new activity            |
| GET    | `/activities`    | Get all logged activities     |
| PUT    | `/activities/{id}`| Update a specific activity    |
| DELETE | `/activities/{id}`| Delete a specific activity    |

### Goal Management
| Method | Endpoint        | Description                  |
|--------|-----------------|------------------------------|
| POST   | `/goals`        | Set a new fitness goal       |
| GET    | `/goals`        | View all goals               |
| PUT    | `/goals/{id}`   | Update a specific goal       |
| DELETE | `/goals/{id}`   | Delete a specific goal       |

------------------------------

## Database Schema

### Users Table
| Column   | Type    | Description              |
|----------|---------|--------------------------|
| `id`     | Integer | Primary key              |
| `name`   | String  | User's name              |
| `email`  | String  | User's email (unique)    |
| `height` | Float   | User's height (cm)       |
| `weight` | Float   | User's weight (kg)       |
| `goal`   | String  | Fitness goal description |

### Activities Table
| Column            | Type    | Description                   |
|--------------------|---------|-------------------------------|
| `id`              | Integer | Primary key                   |
| `user_id`         | Integer | Foreign key referencing users |
| `type`            | String  | Activity type (e.g., running) |
| `duration`        | Float   | Activity duration (minutes)   |
| `distance`        | Float   | Distance covered (km)         |
| `calories_burned` | Float   | Calories burned during activity |
| `date`            | Date    | Date of activity              |

------------------------------

## Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/sruthidacherla/FitnessTracker.git
   cd fittrack
