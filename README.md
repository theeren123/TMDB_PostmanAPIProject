# 🎬 TMDB (The Movie Database) Postman API Manual Test Project

This project covers **manual API tests** conducted using **Postman**
for [TMDB (The Movie Database)](https://www.themoviedb.org/). The tests include core functionalities such as user
account operations, movie listings, adding to favorites, watchlist management, and rating movies.

## 🔧 Technologies Used

- [Postman](https://www.postman.com/) – For API testing and automation
- [TMDB REST API](https://developer.themoviedb.org/reference/intro/getting-started) – The APIs being tested

---

## 📌 API Basics

- **Base URL (API v3):** `https://api.themoviedb.org/3`
- **Authentication:** Requires Bearer Token
- **Content-Type:** `application/json`

<img src="TMDBPostmanAPIProject.gif" alt="403" width="800" height="500"/>

---

## ✅ Main Endpoints and Test Scenarios

### 🔐 Authentication

| Test Case     | Endpoint | Method | Description                              |
|---------------|----------|--------|------------------------------------------|
| Valid Login   | `/login` | POST   | Logs in with valid credentials           |
| Invalid Login | `/login` | POST   | Returns an error for invalid credentials |

### 👤 Account Operations

| Test Case              | Endpoint                                 | Method | Description                       |
|------------------------|------------------------------------------|--------|-----------------------------------|
| Get Account Details    | `/account`                               | GET    | Retrieves user account details    |
| Add Movie to Favorites | `/account/{account_id}/favorite`         | POST   | Adds specified movie to favorites |
| Add Movie to Watchlist | `/account/{account_id}/watchlist`        | POST   | Adds movie to the watchlist       |
| Get Favorite Movies    | `/account/{account_id}/favorite/movies`  | GET    | Lists user's favorite movies      |
| Get Rated Movies       | `/account/{account_id}/rated/movies`     | GET    | Lists user's rated movies         |
| Get Watchlist Movies   | `/account/{account_id}/watchlist/movies` | GET    | Lists user's watchlist            |

### 🎞️ Movie Information

| Test Case           | Endpoint                   | Method | Description                           |
|---------------------|----------------------------|--------|---------------------------------------|
| Get Movie Details   | `/movie/{movie_id}`        | GET    | Retrieves details of a specific movie |
| Add Movie Rating    | `/movie/{movie_id}/rating` | POST   | Submits a rating for the movie        |
| Delete Movie Rating | `/movie/{movie_id}/rating` | DELETE | Removes the user's rating             |

### 🔍 Search & Listings

| Test Case              | Endpoint                 | Method | Description                        |
|------------------------|--------------------------|--------|------------------------------------|
| Get Movie Genres       | `/genre/movie/list`      | GET    | Retrieves list of all movie genres |
| Get Now Playing Movies | `/movie/now_playing`     | GET    | Lists movies currently in theaters |
| Get Popular Movies     | `/movie/popular`         | GET    | Lists popular movies               |
| Get Top Rated Movies   | `/movie/top_rated`       | GET    | Lists top-rated movies             |
| Get Upcoming Movies    | `/movie/upcoming`        | GET    | Lists upcoming releases            |
| Search for Movies      | `/search/movie?query=`   | GET    | Searches for movies by keyword     |
| Search for Keywords    | `/search/keyword?query=` | GET    | Searches for matching keywords     |

### 🚫 Unauthorized Access Test

| Test Case           | Endpoint                   | Method | Description                                                |
|---------------------|----------------------------|--------|------------------------------------------------------------|
| Unauthorized Access | `/list/{list_id}/add_item` | POST   | Validates proper error handling with an invalid session ID |

---

## 🧪 Setting Up the Test Environment

1. Obtain your [TMDB API Key](https://developer.themoviedb.org/).
2. Create a Postman environment and add your authentication token.
3. Use Bearer Token authentication in the Authorization tab.
4. Run manual tests using the listed endpoints above.

---

## 📁 Project Structure

- `TMDB Test Case.pdf` → Detailed list of test scenarios
- `TMDB Endpoint.pdf` → Descriptions and parameters of tested endpoints

---

## 👨‍💻 Contributors

* [Zafer Ataklı](https://github.com/zaferatakli)
* [Rıfat Batır](https://github.com/rftbtr)
* [Tugba Kilic](https://github.com/TugbaKilic33)
* [Nuri Öztürk](https://github.com/NuriOzturk)
* [Azim Korkmaz](https://github.com/AzimKorkmaz)
* [Yigit Cam](https://github.com/Yigit-Cam)
* [Eren Icinozbebek](https://github.com/theeren123)

---

