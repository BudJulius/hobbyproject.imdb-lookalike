# hobbyproject.imdb-lookalike

Skriver på engelsk da det er enklere å forklare ting og tang :D

## Project: IMBD look-alike (except not)
### Keywords
N-tier architecture, function app endpoints, API, EF Core, LINQ, SQL/Postgres DB, relational DB tables, simple frontend, Docker, run locally.

## Description
The purpose of this project is to develop a simple frontend that would provide the user with the ability to retrieve movies from the database, search for movies, retrieve top 10-20-30 movies from a category or by year, and display the movie poster and some other basic information. It doesn't really matter that much, as long as it somewhat works and you feel that you have learned something, or maybe even learned something new. As for the frontend, you can just use simple HTML/CSS/Javascript, or any other framework of your liking. Bring this up with me if you want so we can discuss it further. 

So here in this project, the API (the backend) is the most important. Since both of you said that you wanted to give this a project a try, I will divide it in 2 parts - for Agnar - a .NET application, and for Juozas - python application (or try .NET if you want, though it's a little more complex and you might not have the time to learn it. But once you have the basic down, it's very easy to develop applications). 

Anyways, what I want the backend to do is to connect to the "The movie DB" API (create an user, request an API key, use it for making API calls - or ask me and I will provide my API key, doesn't matter). Then you should connect to a database of your choosing (host it locally, maybe in Docker container or something. Use SQL database, as it will teach you a lot about LINQ, EF Core, creating and managing tables, creating tables with primary and foreign keys, relationships and querying in general. Once you have that down, you can create a some endpoints that you frontend would call to retrieve information - but what I would love to is if I for example make a GET movie call, the backend checks the database first, if the movie exists, then return it, if not - call the movieDB API, retrieve the movie and save it in DB for next time, thus limiting the need to call the movieDB multiple times for the same request.

Ask many questions, I'm here to help, but not to hold your hand. Also for each new implementation, create an issue first in Github, then from that issue create a new branch, and work on that branch. After you are done, create a Pull request so I can review it and merge to main (I won't limit what you can do, but it helps learning). We can also meet some days and work on this together. No pressure though, just focus on learning. And don't overcomplicate things, just get it to work :D that’s the most important thing. 

I will try to host a database in cloud, so you can connect to it, but I can't promise anything. Will let you know. 

There is a lot of documentation (check resources) and try to limit your usage of AI as much as possible - for best possible learning outcome.
Remember, the most important thing is functionality over looks! It may look like shit, doesn't matter, as long as it somewhat works. Again, it doesn’t have to be perfect, the code can look like like shit as well. I'm looking for functionality there - I want to see that it works and how it works, not why it works.

So the plan is simple (but the implementation might be a pain in the ass :D).
    1. Retrieve a movieDB API key.
    2. Test it using the documentation and Bruno or Postman to make a call and retrieve a movie. For example if you use the /search endpoint, can you retrieve the information for "Finding Nemo"?
    3. Create a single endpoint that you could test locally - to retrieve a movie (like in step 2. for example), and display that in the console or in debug mode (just to confirm that your implementation is working.
    4. Make a database integration. Create tables, relationships etc.
    5. Expand on the endpoints.
    6. Create a simple frontend page that would be able to call the endpoints. See if you can connect them together.
        a. If you want an extra challenge, we can discuss implementing authentication here as well.
    7. Develop whatever you want further.
    

You can send me a message whenever you want.
## Resources:
[Getting Started](https://developer.themoviedb.org/docs/getting-started) - The movie DB
[Technical documentation | Microsoft Learn](https://learn.microsoft.com/en-us/docs/)
[Docker Docs](https://docs.docker.com/)

### Endpoints (suggestions):
GET first 10 elements:
GET: /api/movie/{name}
GET: /api/movie/{year}
GET: /api/movie/{genre} (start with just a few genres first, expand later)
GET: /api/movie/search/{name}
GET: /api/movie/top (not sure if the movieDB API has and endpoint for that. Can you come up with a solution yourself? ;) )
(any other you come up with)