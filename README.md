# 🎯 Number Guessing Game

A command-line number guessing game built using **Bash** and **PostgreSQL** as part of the freeCodeCamp Relational Database Certification.

## 🚀 Project Overview

This application:

- Generates a random number between **1 and 1000**
- Prompts the user for a username
- Stores user data in a PostgreSQL database
- Tracks:
  - Total games played
  - Best game (fewest guesses)
- Validates integer input
- Provides hints (higher/lower) until correct guess

---

## 🛠 Tech Stack

- Bash (Shell scripting)
- PostgreSQL
- Git

---

## 🗄 Database Structure

### Users Table
| Column   | Type        | Constraints          |
|----------|------------|----------------------|
| user_id  | SERIAL     | Primary Key          |
| username | VARCHAR(22)| UNIQUE, NOT NULL     |

### Games Table
| Column   | Type   | Constraints                 |
|----------|--------|-----------------------------|
| game_id  | SERIAL | Primary Key                 |
| user_id  | INT    | References users(user_id)   |
| guesses  | INT    | NOT NULL                    |

---

## ▶️ How to Run

1. Clone the repository
2. Ensure PostgreSQL is installed
3. Restore the database:

```bash
psql -U postgres < number_guess.sql
```

4. Run the script:

```bash
./number_guess.sh
```

---

## 🧠 Features Implemented

- Random number generation (1–1000)
- Returning user detection
- Game statistics tracking
- Input validation for non-integer guesses
- Exact output formatting (FCC test compliant)
- Database dump included

---

## 📌 Certification Requirement Compliance

- Git repository with 5+ commits
- Proper commit message prefixes:
  - `feat:`
  - `fix:`
  - `refactor:`
  - `chore:`
  - `test:`
- Working tree clean
- Project completed on `main` branch

---

## 📄 Author

Built as part of the freeCodeCamp Relational Database Certification.
