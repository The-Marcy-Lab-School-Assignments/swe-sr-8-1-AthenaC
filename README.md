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
> 2. Think of Instagram like a restaurant.
>
> - The frontend would be the dining area and this is where the users would interact with the service, such as read the menu (your feed), place orders (likes, comments, uploads), and get your food served (photos, videos).
> - The backend would be the waitstaff and kitchen. The waitstaff (Express server) takes your order from the frontend and brings it to the kitchen. They also bring back your food and updates, making sure everything runs smoothly and respond to customer needs.
> - The database would be the pantry and recipe book, where all the ingredients (data) are stored. The kitchen (backend) goes here to fetch what it needs or add new supplies. It keeps everything organized and consistent.
>
> 3. Separation of concerns—keeping the frontend, backend, and database distinct—makes everything easier to build, manage, and scale.
>
> - Frontend developers can focus on user experience and design without worrying about data storage.
> - Backend developers can manage logic and security without fussing over layout or styling.
> - Database administrators can structure and optimize data without writing app interfaces.
>
> If we tried to cram everything into one layer, things would get messy fast. Imagine a restaurant where the chef also serves customers and takes orders—mistakes would pile up, the workflow would be chaotic, and it would be impossible to grow. With clear separation, each part can evolve independently, making our apps more efficient, secure, and maintainable.
