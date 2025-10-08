# Travel-Tracker

Travel Tracker is a web app that lets users create profiles and record the countries they've visited using ISO country codes.

## Tech Stack

- **Frontend**: Bootstrap
- **Backend**: Node.js (Express.js)
- **Database**: PostgreSQL

## Setup Guide

### Prerequisites

- Node.js (>= 18.x)
- npm (>= 9.x)
- PostgreSQL running locally

### Clone the Repository

```bash
git clone https://github.com/yanicells/Travel-Tracker.git
cd Travel-Tracker
```

### Install Dependencies

```bash
npm install
```

(Optional) Install nodemon globally:

```bash
npm install -g nodemon
```

### Database Setup

Make sure PostgreSQL is running. [Install PostgreSQL](https://www.postgresql.org) if you haven't.
No need to create a table, just create a database, and make sure it connects to the terminal (or command prompt) once you have.

#### Create a database:

```sql
CREATE DATABASE World;
```

### Environment Variables

Create a `.env` file in the root directory.
Fill in the information. The port should be 5432 by default.

```env
DBUSER=""
DBHOST=""
DBNAME=""
DBPASS=""
DBPORT=5432
```

#### Initialize the Database:

```sql
INSERT INTO users (name, color)
VALUES ('Yani', 'teal');

INSERT INTO visited_countries (country_code, user_id)
VALUES ('FR', 1), ('GB', 1);
```

### Run the Project

```bash
# Start with nodemon
nodemon index.js
```

Project will be available at: http://localhost:3000

## Usage

1. Register or create a user profile.
2. Mark countries you have visited using ISO alpha-2 country codes (e.g., FR, GB).
3. View your visited countries list or map (if implemented).

## Notes
1. Ensure your database credentials in .env match your PostgreSQL setup.
2. Run the SQL commands in queries.sql to set up the database schema and initial data.
