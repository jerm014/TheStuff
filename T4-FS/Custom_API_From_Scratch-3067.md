# Project 3067: Custom API From Scratch
----

### Project Context

Using all of the skills you’ve developed over the last two trimesters, you’re going to team up with a partner in creating your very own API from start to finish. You’ll develop a design, narrow down what should be in your MVP (minimum viable product), and work together as a team to bring your idea to life. You have a limited number of days to work on this project, so be sure to keep your scope reasonable for you and your team.

### Challenge

There is one rule that must be followed…your application must follow the theme,***“Around the World!”.***You and your team are free to interpret that in any way you see fit (keep it Safe For Work, though)! If you are interested in continuing where you left off on your Bob Ross API, feel free to use that as the starting point for this project and expand upon it with new features!

### Manual Review

When manually reviewing your peers, have them share with you (on their local computer) the API that they built. This will make reviewing easier than trying to set up their database and API on your local system. What this means when developing your API/database is to make sure that everything runs locally so that the manual review process is straightforward.

### Final Note

You are expected to have this project run locally on your machine (or sandbox environment), but you are welcome to find a way to host this online for your own purposes (especially if you wish to share this with others). If you choose to host this online, there is definitely a free/cheap way to do so, so be sure to look at the tools you are interested in using and verify their functionality as well as pricing model. Many tools online have a free tier that would be more than sufficient for this project.


----
## Tasks
---
### 0. Project Proposal

Every great project starts with the design phase. For your application revolving around this theme, create your design documents that lay out what you and your team will build together. You should expect to spend about 1 day or less designing your application before starting on the implementation. <!--plain-NL-->

Please store in your git repository a directory named “Design Documents” with the following:<!--plain-NL-->

- Writeups of the design


What is it your are going to build and how does it fit the theme?
What tools will you use?
How long do you expect to spend on development of each part?
etc.
- What is it your are going to build and how does it fit the theme?
- What tools will you use?
- How long do you expect to spend on development of each part?
- etc.
- API documentation
- Database documentation (UML or similar)
- Wireframes for any implemented UI portions of your application

- What is it your are going to build and how does it fit the theme?
- What tools will you use?
- How long do you expect to spend on development of each part?
- etc.


---
### 1. The Backend

Now that you and your team have a design in place, it is time to start implementing that design. Begin collecting the data you need, set up your database based on your design docs, build an ETL process (if necessary) to populate the database. Even if you (and your users) are manually inputting data into your database instead of collecting data from other sources, you do need to set up a database for this project for your API to interact with.<!--plain-NL-->

Once your database is in place and populated with data, it will be time to consider how you build your API to interact with your data. In this project, your API <!--plain-NL-->**must retrieve data from a database**<!--code-NL-->.  You may then map the database data to more useful models (if necessary).  Finally, you <!--plain-NL-->**must send it back in an http response using the correct status codes**<!--code-NL-->.  <!--plain-NL-->

Additionally, you must implement <!--plain-NL-->**3 of the following**<!--code-NL-->:<!--plain-NL-->

- Include a logger
- use a tool and associated comment syntax to auto generate API docs (Sphynx for python, swagger-jsdoc for Javascript , or other)
- Include unittests (at least one)
- Authenticate users of your API
- Allow for pagination of data
- Allow for caching of data to reduce hits to your database when possible and improve responsiveness to your users
- Queuing systems (for long-running process on your server)
- Web sockets (two-way communication between client and server)

You can have many users for your application, but at a minimum make sure that there is a test user available so that if you do not implement a user-creation process, you (and your reviewer) can test your API with this test user.<!--plain-NL-->

While building your API, it is highly recommended that you use a tool, like <!--plain-->[Postman](https://www.postman.com/) <!--link--> during development. With this tool you can hit your API without needing to write code to see that it is working properly. It is also recommended that you build tests for your API using Postman so that you can ensure that you do not break any of your functionality during development (something which is easy to do when tweaking API endpoints or changing the structure of your database during development). Postman can save you a lot of time and headache here.<!--plain-->