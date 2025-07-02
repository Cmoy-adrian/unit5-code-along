# Movies API Example
This repository demonstrates a complete RESTful API built with Express.js for managing a movie collection.

## Getting Started
1. Clone this repository to your local machine
2. Navigate to the project directory
3. Install dependencies:
   ```bash
   npm install
   ```

## Project Overview
This is a complete CRUD API that demonstrates:
- **server.js** - Express.js server with full CRUD operations for movie management
- **tests/api.test.js** - Comprehensive Jest tests for all API endpoints

## Pre-installed Dependencies
This repository comes with the following packages:
- `express` - Web framework for Node.js
- `jest` - Testing framework
- `supertest` - HTTP assertion library for testing APIs

## Sample Data
The server includes a starter movie collection:
```javascript
const movies = [
  { id: 1, title: "The Shawshank Redemption", director: "Frank Darabont", year: 1994, genre: "Drama" },
  { id: 2, title: "The Godfather", director: "Francis Ford Coppola", year: 1972, genre: "Crime" },
  { id: 3, title: "Pulp Fiction", director: "Quentin Tarantino", year: 1994, genre: "Crime" },
  { id: 4, title: "The Dark Knight", director: "Christopher Nolan", year: 2008, genre: "Action" }
];
```

## API Endpoints
- `GET /` - API homepage with endpoint documentation
- `GET /movies` - Retrieve all movies
- `GET /movies/:id` - Retrieve a specific movie by ID
- `POST /movies` - Add a new movie
- `PUT /movies/:id` - Update an existing movie
- `DELETE /movies/:id` - Remove a movie

## Running the Server
Start your development server:
```bash
npm start
```
Your API will be available at `http://localhost:3000`

## Testing
Run the automated test suite:
```bash
npm test
```

## File Structure
```
server.js
tests/
└── api.test.js
package.json
README.md
```

## Example API Usage
### Get all movies
```bash
GET http://localhost:3000/movies
```

### Create a new movie
```bash
POST http://localhost:3000/movies
Content-Type: application/json

{
  "title": "Inception",
  "director": "Christopher Nolan",
  "year": 2010,
  "genre": "Sci-Fi"
}
```

### Update a movie
```bash
PUT http://localhost:3000/movies/1
Content-Type: application/json

{
  "title": "The Shawshank Redemption",
  "director": "Frank Darabont",
  "year": 1994,
  "genre": "Drama/Hope"
}
```

### Delete a movie
```bash
DELETE http://localhost:3000/movies/1
```