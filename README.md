# swe-sr-8-1

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt

![Fullstack Diagram](./client-server-database-diagram.svg)

You’ve been given a diagram (see above) showing the three core layers of a fullstack application:

- Frontend – a React application that users interact with
- Backend – an Express server that handles logic and communication
- Database – a PostgreSQL database that stores persistent data

Imagine you’re explaining how these layers work together by using a real-world example: Instagram.

Your task:

1. Explain how Instagram works using the three-layer diagram.

   - What happens when a user opens the app, scrolls through their feed, likes a post, or uploads a new photo?
   - Walk through how data flows from the frontend to the backend and to the database—and back again.

2. Come up with an analogy to help someone new to coding understand these layers.

- You might compare the system to something like a restaurant, a library, or even a post office—anything that helps make the roles of each layer intuitive.
- Make sure your analogy maps clearly to the roles of the frontend, backend, and database.

3. Reflect on the value of this separation.

- Why do we separate concerns into these layers?
- What would go wrong if we tried to do everything in one layer?

Audience: Imagine you're writing this for someone who's just starting out in web development and wants to understand how modern apps work.

Length: Around 400–600 words.

> 1. When a user opens the app and interacts with the Graphical User Interface (GUI), the user is interacting with the frontend which is a React application that runs on your browser or mobile app. Let's go through step-by-step how the user's actions on the frontend interacts with the backend and database.
>
> While scrolling through the feed, the React frontend sends a request to the backend (an Express server) like, _"Hey, I need the latest posts for this user."_ The backend receives this request and interacts with the database (PostgreSQL), _"Give me the most recent posts from the people this user follows."_ The database send the data (post info, captions, images, etc.) back to the backend, and then the backend organizes that data and send it to the frontend, which displays it in your feed.
>
> When you tap the heart icon to "like" a post, the frontend sends a request to the backend, _"This user liked post #123."_ The backend updates the database to record that like and sends back a confirmation and update the number of likes which the frontend displays instantly.
>
> So when you choose a photo and hit upload, the frontend packages your photo, caption, and tags, and send them to the backend. The backend stores the image (oftern in cloud storage) and saves metadata (caption, user, timestamp) in the database. Once this is completed, the frontend updates your profile and followers' feeds.
>
> This cycle between the frontend to backend to database and back again is the foundation of most web apps.
>
> 2.
