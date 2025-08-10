# alx-project-0x14
# MoviesDatabase Project

## API Overview
The MoviesDatabase API (also referred to as TMDb API) offers a rich, community-driven database for movies, TV shows, and celebrity information. It includes metadata, images, videos, search capabilities, trending content, and more—ideal for building entertainment-focused applications. :contentReference[oaicite:0]{index=0}

## Version
This project uses **TMDb API version 1, which is the current stable release with extensive documentation. 

## Available Endpoints
Here are some of the main endpoints available in the TMDb v1 API:
1- Titles - under this we have Titles - Multiple:,Titles - By List of Id's:, Title,Title Rating
 etc
 
2- Search

3-Actors
4-Utils


## Request and Response Format
Requests generally use standard RESTful HTTP with JSON responses.

example request 
const options = {
  method: 'GET',
  headers: {
    'X-RapidAPI-Key': 'YOUR_RAPIDAPI_KEY',
    'X-RapidAPI-Host': 'moviesdatabase.p.rapidapi.com'
  }
};

fetch('https://moviesdatabase.p.rapidapi.com/titles', options)
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(err => console.error(err));
  ## Authentication 
  The MoviesDatabase API on RapidAPI uses API key authentication via request headers.
You must sign up at RapidAPI and subscribe to the MoviesDatabase API to get your credentials.
X-RapidAPI-Key: YOUR_RAPIDAPI_KEY
X-RapidAPI-Host: moviesdatabase.p.rapidapi.com
const options = {
  method: 'GET',
  headers: {
    'X-RapidAPI-Key': 'YOUR_RAPIDAPI_KEY',
    'X-RapidAPI-Host': 'moviesdatabase.p.rapidapi.com'
  }
};

 ## Error Handling 
 When using the MoviesDatabase API via RapidAPI, errors are returned with standard HTTP status codes along with a JSON error message.

Common Error Codes
400 Bad Request – The request parameters are missing or invalid.
Example: Missing required query parameters such as title or id.

401 Unauthorized – Your X-RapidAPI-Key is missing, invalid, or expired.

403 Forbidden – Your account does not have access to this endpoint (e.g., due to subscription plan restrictions).

404 Not Found – The requested resource (movie, person, etc.) could not be found.

429 Too Many Requests – You have exceeded your plan's rate limit.

500 Internal Server Error – An unexpected issue occurred on the API server.


## Usage Limits and Best PracticesUsage Limits
Rate Limits: Your exact request limit depends on the subscription plan you select on RapidAPI. Free plans typically allow fewer requests per day/month, while paid plans have higher or unlimited quotas.

Burst Limits: There may also be a per-second/minute limit to prevent abuse (e.g., 5–10 requests/second).

Quota Overages: If you exceed your plan’s limits, RapidAPI will return a 429 Too Many Requests response and may block further requests until your quota resets or you upgrade your plan.


