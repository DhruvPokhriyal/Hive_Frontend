
# Social Garbage – Frontend

This is the frontend of **Social Garbage**, a Flutter-based social platform that integrates real-time backend APIs, Google Sign-In authentication, content creation, notifications, and moderation features.  

---

## 📖 Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Setup Instructions](#setup-instructions)
- [Folder Structure](#folder-structure)
- [Contributions](#contributions)
- [Screenshots](#screenshots)

---

## Project Overview
Social Garbage is designed as a modern social platform with integrated content safety checks. The frontend is built using **Flutter**, with seamless API integration for posts, user profiles, authentication, notifications, and search functionality.  

---

## Features
- Google Sign-In authentication with Supabase integration  
- Create, like, dislike, and comment on posts  
- Search posts with filters (Safe / Under Review / Flagged)  
- Notifications with swipe-to-dismiss support  
- Bottom navigation bar and state preservation  
- API integration with backend services for real-time data  

---

## Setup Instructions

### 1. Prerequisites
- [Flutter SDK](https://docs.flutter.dev/get-started/install) installed  
- Android Studio / VS Code with Flutter extensions  
- Backend server running (update the `baseUrl` in `lib/api_client.dart`)  

### 2. Clone the Repository
```bash
git clone https://github.com/shivam-purve/social_garbage.git
cd social_garbage

###3.) Install Dependencies
flutter pub get

###4.) Configure Base URL

In lib/api_client.dart, update the kBaseUrl constant with your backend API URL:

const String kBaseUrl = 'http://10.0.2.2:8000'; // Android Emulator
// or
const String kBaseUrl = '(https://hive-backend-tnmw.onrender.com)'; // Localhost (desktop/web)

5.) Run the App
  flutter run

Folder Structure

Folder Structure
 lib/
├──
│   └── api_client.dart        # Base API client
├── services/
│   ├── auth_service.dart          # Authentication API integration
│   ├── post_service.dart          # Posts API (fetch, like, comment, create)
│   ├── search_service.dart        # Search API integration
│   ├── user_service.dart          # User profile API
│   └── notification_service.dart  # Local notifications
├── widgets/
│   ├── post_card.dart             # Post UI component
│   └── notification_widget.dart   # Notification UI component
├── screens/
│   ├── home_screen.dart           # Home feed
│   ├── user.dart                  # User profile screen
│   ├── notifs.dart                # Notifications screen
│   ├── search.dart                # Search screen
│   ├── create.dart                # Create post screen
│   └── login.dart                 # Google Sign-In
└── main.dart                      # App entry point
```
# Contributions
## Mritunjay Tiwari

Designed UI Design in Figma<br>
Developed UI Screens:
Create Screen
Added Bottom Navigation Bar and App Bar with design and logic<br>
Implemented API integration for authentication (Google Sign-In with Supabase)<br>
Integrated User Profile screen API<br>
API Integration:
Posts (fetch, like, dislike, comment)<br>
Implemented and Configured Function to Integrate the All the Endpoints in the App<br>
Added Notifications screen with local notification support<br>
Implemented route management for multiple screens<br>
Added state persistence for Bottom Navigation Bar<br>
Fixed several routing and connection bugs<br>


## Shivam Purve
Developed UI Screens:
Home Screen
Comment Screen
Search Screen
Post Card Widget,
Search functionality with filters,
Create post with content analysis support


##  Screenshots of different pages:-

social_garbage/
├── lib/
├── screenshots/
│   ├── login.png
│   ├── home.png
│   ├── create.png
│   ├── search.png
│   └── notifs.png


## Screenshots

### Home Screen
![Screenshot_20250906_233745](https://github.com/user-attachments/assets/6e695e4b-54cf-4d5b-aaa3-083925df428f)

### Login with Google
![Screenshot_20250906_233940](https://github.com/user-attachments/assets/1ab2420c-3d0b-4c62-ab9e-ad75668fa934)

### Create Post
![Screenshot_20250906_233602](https://github.com/user-attachments/assets/317ea7f1-f3d8-4508-9829-3f67edb23767)

### Notification
![Screenshot_20250906_233615](https://github.com/user-attachments/assets/76441ab8-4fa1-43c8-94dd-dc3fd4f1e041)

### Search
![Screenshot_20250906_233552](https://github.com/user-attachments/assets/5685a766-f69b-4db1-8ac0-fb10e5e51947)

### Logout
![Screenshot_20250906_233626](https://github.com/user-attachments/assets/975768a6-c0d9-4a5d-a947-d57c48815693)


## Tech Stack

Clearly listing  the technologies and tools used. Example:

Tech Stack used 
- **Framework:** Flutter (Dart)  
- **State Management:** Flutter's Stateful Widgets  
- **Routing:** go_router  
- **Backend Integration:** REST APIs  
- **Authentication:** Supabase (Google Sign-In)  
- **Local Storage:** SharedPreferences  
- **Notifications:** flutter_local_notifications  
- **HTTP Client:** http package

## API Endpoints Used

Document the endpoints you integrated with. Example:

## API Endpoints
- **Auth**
  - `POST /auth/google` → Sign in with Google
- **Posts**
  - `GET /posts` → Fetch all posts
  - `POST /posts` → Create a new post
  - `POST /posts/:id/like` → Like a post
  - `POST /posts/:id/dislike` → Dislike a post
  - `POST /posts/:id/comments` → Add comment
- **User**
  - `GET /user/me` → Fetch current user profile
  - `GET /user/:id/posts` → Fetch posts by user
- **Search**
  - `GET /posts?q=term&status=flagged` → Search posts with filters




## Known Issues

Be transparent about current bugs or limitations. Example:

  Known Issues
- API sometimes returns `401 Unauthorized` if access token expires.  
- Search filtering is partially handled on client-side due to backend limitations.

 ## Support the Project

## Support

If you find this project useful, please consider giving it a on GitHub.  
Your feedback and contributions are always welcome!


## Acknowledgments

We would like to thank:  
- [Flutter](https://flutter.dev) for the cross-platform framework  
- [Supabase](https://supabase.com) for authentication and backend support  
- [Google Cloud](https://cloud.google.com) for OAuth and API integrations  

This project was developed as part of a collaborative effort to explore real-time content safety and moderation in social platforms.


























