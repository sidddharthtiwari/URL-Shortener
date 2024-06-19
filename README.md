# URL Shortener Web Application

This project implements a URL Shortener, which takes long URLs and converts them into shorter, more manageable links. It provides a RESTful API backend built with Node.js and Express, utilizing both SQL and NoSQL databases for storage.

## Table of Contents

- [Introduction](#introduction)
- [How It Works](#how-it-works)
- [Technologies Used](#technologies-used)
- [API Endpoints](#api-endpoints)
- [Setup and Installation](#setup-and-installation)
- [Deployment](#deployment)
- [Database Options](#database-options)
- [Middleware](#middleware)
- [Contributing](#contributing)

## Introduction

URL Shortener is a web application designed to create shortened URLs from long ones, making it easier to share links. It employs a backend API that handles URL shortening and retrieval operations. The project is structured using the MVC (Model-View-Controller) architecture, separating concerns between data (Model), presentation (View), and logic (Controller).

## How It Works

When a user submits a long URL to the API endpoint `/shorten`, the backend generates a unique short URL and stores the mapping between the short URL and the long URL in a database. Subsequently, when someone accesses the shortened URL, the API endpoint `/retrieveLongUrl` retrieves the corresponding long URL from the database and performs a redirection.

## Technologies Used

- **Backend**: Node.js, Express.js
- **Databases**: SQL (MySQL) for structured data storage, NoSQL (MongoDB) for unstructured data storage
- **Middleware**: Implemented for input sanitization and validation
- **Deployment**: AWS (EC2) used for hosting the application

## API Endpoints

- **POST /shorten**: Takes `long_url` as input and returns `short_url`.
- **GET /retrieveLongUrl**: Takes `short_url` as input and returns `long_url`.

## Setup and Installation

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Configure your database settings in `config/db.js`.
5. Start the server using `node index.js`.

## Deployment

The application is deployed on an AWS EC2 instance. Ensure your instance is properly configured with Node.js and necessary security settings.

## Database Options

### SQL

Used for structured data where data is stored in tabular format. Suitable for scenarios like managing user data where attributes are uniform across entities.

### NoSQL (MongoDB)

Ideal for unstructured data where flexibility is required, such as storing variable product attributes or timeline-based data.

## Middleware

Middleware is implemented to handle input sanitization and validation, ensuring secure communication between the client and server.

## Contributing

Feel free to contribute to this project by forking the repository, making your changes, and submitting a pull request. Please follow the code style and structure already in place.
