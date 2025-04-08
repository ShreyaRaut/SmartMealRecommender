# Smart Meal Recommender App

The Smart Meal Recommender is an Android-based application that leverages distributed systems principles to deliver real-time, personalized meal suggestions to users based on ingredients, available cooking time, and meal preferences. The system integrates multiple distributed components: a native mobile frontend, an intermediate servlet layer deployed on a cloud-based platform, a third-party API (Tasty API) for fetching recipe and nutritional data, and a MongoDB Atlas cloud database for operational analytics and user logs.

The architecture follows the Model-View-Controller (MVC) design, where:

The Model handles structured recipe information;

The View (mobile app and dashboard) presents interactive interfaces;

The Controller (servlets) orchestrates API communication, data parsing, and logging.

The backend servlet acts as a stateless microservice that performs GET requests to the Tasty API, processes JSON responses, and routes the structured data to the client while logging both request metadata and recipe results into MongoDB. MongoDB supports fault tolerance and scalability, making it ideal for storing high-volume app usage and recipe data. The system also includes a dynamic web-based dashboard that visualizes key operational metrics like peak usage hours, cuisine preferences, response times, and device/OS breakdowns using pre-aggregated Mongo queries.

Overall, this project demonstrates real-world distributed system concepts such as RESTful communication, asynchronous data handling, stateless service architecture, cloud database integration, and operational analytics—tailored for a personalized user experience in meal planning.
