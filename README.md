# InkLink - Graffiti Sharing App

## Note: This project is in development!

## What is InkLink?
**From Street to Screen - Share your Scene**
InkLink is a photo-sharing app, similar to Instagram. However, instead of sharing photos and videos of all categories, InkLink focuses on sharing photos of graffiti. Graffiti is a long-forgotten and under-appreciated form of art. It is rarely appreciated and frequently scrutinized. This app aims to change that by bringing people from different cultures and backgrounds together, into a community that celebrates graffiti as a legitimate and impactful form of art.

## Requirements:
### Functional Requirements:
**Graffiti Photo Sharing and Viewing:** Users should be able to upload photos of graffiti as posts. Posts will contain the image, relevant captions and tags, the location and artist (if known), as well as likes and comments.
**Liking and Commenting**: Users should be able to view other users' posts, like the post, and comment on the post. Users should also be able to reply to comments.
**Following:** Users should be able to follow each other.
**User Profile:** Users should be able to register an account and securely log in. In their profile, users can see their profile picture, username, name, bio, following, users they follow, and their posts. 
**Custom News Feed**: Each user should have a custom news feed that displays recent photos from the users they follow.
**Search**: There should be a search functionality where users can search for artists, locations, and tags.
**Map View**: Users should be able to view a map displaying their location and the locations of nearby or popular graffiti.
**Notifications**: Users should receive notifications for new likes, comments, follows, and posts from artists they follow.
### Nonfunctional Requirements:
**High Availability and Low Latency:** The system should prioritize high availability and low latency while viewing photos. We can trade off consistency to improve availability.
**Scalability and Read Optimization:** The system should be highly scalable and optimized for read-heavy workloads, with a high read-to-write ratio. 
**Reliability:** The system should be reliable, ensuring that no uploaded photos or videos are lost. This means that the system should be backed up somewhere.
**Compatibility and Performance:** The system should be compatible with a wide range of mobile and web devices. It should support multiple languages and perform across different internet bandwidths.
**Costs:** The system should be as cost-efficient as possible by balancing performance and resource usage. This includes optimizing cloud service expenses, reducing data transfer and storage costs, and ensuring scalability.
**Privacy and Security**: If deployed to customers, InkLink must ensure the privacy and security of user data. This includes account authentication and verification, data encryption in transit and storage, and content moderation to prevent the sharing of illegal or inappropriate content. Users must allow InkLink to access their location to enable Map View.

## Capacity Estimation:

InkLink is a simple project and not a startup; therefore, capacity will not be a major concern. However, we can make the following estimations:
- Read requests will be significantly more frequent than write requests. This is because the majority of users will spend their time browsing instead of posting. We can estimate that the read/write ratio will be 100:1. In an actual app delivered to customers, this read-heavy nature necessitates optimizations for read operations, such as caching strategies, optimized database queries, and the use of CDNs.
- If deployed to customers, we can assume a few things. The app will primarily attract casual users, tourists, or artists, who engage in light browsing and occasional interactions. We can estimate a total user base of around 10,000 to 100,000 active users initially, with potential for growth based on the app's popularity. If 500 images are posted daily, and the average photo size is 150 KB, then the daily storage usage data is 75 MB (500 * 150 KB). We can also assume storage for metadata, thumbnails, user data, and logs, although these will not require as much storage as posts.
