# 🏡 Wanderlust — Airbnb-Inspired Rental Platform

> A full-stack accommodation listing platform inspired by Airbnb, built from scratch using **Node.js, Express.js, MongoDB, and EJS**.

Wanderlust allows users to **explore properties, create and manage listings, upload images, leave reviews, and discover locations through interactive maps**.

The project follows a structured **MVC architecture** and integrates several modern backend technologies for authentication, validation, cloud image storage, sessions, and geolocation.

---

## ✨ Features

* 🔐 User authentication & authorization
* 🏠 Create, view, edit & delete property listings
* 🖼️ Cloud-based image uploads with Cloudinary
* ⭐ Reviews & ratings
* 🗺️ Interactive location maps with MapTiler
* 🔎 Property exploration
* 👤 User-specific listing management
* ✅ Server-side data validation
* 💬 Flash messages
* 🔒 Session-based authentication
* 📱 Responsive user interface

---

## 🛠️ Tech Stack

### Frontend

* HTML5
* CSS3
* JavaScript
* EJS
* EJS-Mate
* Bootstrap

### Backend

* Node.js
* Express.js
* MVC Architecture

### Database

* MongoDB
* Mongoose

### Authentication & Security

* Passport.js
* Passport-Local
* Passport-Local-Mongoose
* Express Session
* Connect-Mongo

### Cloud & APIs

* Cloudinary
* Multer
* MapTiler

### Validation & Utilities

* Joi
* Connect-Flash
* Method-Override
* dotenv

The project's dependency configuration confirms these technologies, including Express 5, Mongoose 9, EJS 5, Cloudinary, MapTiler SDK, Passport, Joi, Multer, and Mongo-backed sessions.

---

## 🏗️ Architecture

Wanderlust follows the **Model-View-Controller (MVC)** pattern to keep the application organized and maintainable.

```text
                    ┌───────────────────┐
                    │       User        │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │      Routes       │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │    Controllers    │
                    └───────┬─────┬─────┘
                            │     │
                    ┌───────┘     └────────┐
                    ▼                       ▼
             ┌──────────────┐       ┌──────────────┐
             │    Models    │       │    Views     │
             │   MongoDB    │       │     EJS      │
             └──────────────┘       └──────────────┘
                    │
                    ▼
             ┌──────────────┐
             │  Cloudinary  │
             │    Images    │
             └──────────────┘
```

---

## 📂 Project Structure

```text
Wanderlust-MERN-Stack-Airbnb-Clone/
│
├── api/
├── controllers/
├── init/
├── models/
├── public/
├── routes/
├── utils/
├── views/
│
├── cloudConfig.js
├── middleware.js
├── schema.js
├── package.json
├── vercel.json
│
└── README.md
```

The repository currently follows this modular structure, separating controllers, models, routes, views, utilities, public assets, and initialization logic.

---

## 🔄 Application Flow

```text
User
 │
 ▼
EJS Interface
 │
 ▼
Express Routes
 │
 ▼
Controllers
 │
 ├──────────────► Authentication
 │
 ├──────────────► Validation
 │
 ├──────────────► CRUD Operations
 │
 ▼
MongoDB
 │
 └──────────────► Persistent Data


Image Upload
 │
 ▼
Multer
 │
 ▼
Cloudinary
 │
 ▼
Cloud Image URL
```

---

## 🗺️ Interactive Maps

Wanderlust integrates **MapTiler** to provide location-based map functionality for property listings.

This allows listings to be associated with geographic locations and displayed through an interactive map interface.

---

## ☁️ Image Upload Pipeline

Property images are handled through **Multer** and stored using **Cloudinary**.

```text
Select Image
     │
     ▼
   Multer
     │
     ▼
   Backend
     │
     ▼
 Cloudinary
     │
     ▼
 Image URL
     │
     ▼
   MongoDB
```

This keeps uploaded media in dedicated cloud storage instead of storing image files directly inside the application.

---

## 🔐 Authentication

The application uses **Passport.js** with **Passport-Local** and **Passport-Local-Mongoose** for user authentication.

Sessions are persisted using:

* Express Session
* Connect-Mongo

This provides authenticated sessions while keeping session data stored in MongoDB.

---

## ✅ Validation

User-submitted data is validated using **Joi** before being processed by the application.

This helps ensure that listing and other submitted data follows the expected schema and reduces invalid requests reaching the database.

---

## 🚀 Getting Started

### Prerequisites

Make sure you have installed:

* Node.js
* npm
* MongoDB / MongoDB Atlas
* Git

You will also need a **Cloudinary** account and a **MapTiler** API key.

---

### 1. Clone the Repository

```bash
git clone https://github.com/Tayyab-Yahya/Wanderlust-MERN-Stack-Airbnb-Clone.git

cd Wanderlust-MERN-Stack-Airbnb-Clone
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment Variables

Create a `.env` file and add the required credentials:

```env
ATLASDB_URL=your_mongodb_connection_string
SECRET=your_session_secret

CLOUD_NAME=your_cloudinary_cloud_name
CLOUD_API_KEY=your_cloudinary_api_key
CLOUD_API_SECRET=your_cloudinary_api_secret

MAP_TOKEN=your_maptiler_api_key
```

> ⚠️ Never commit your `.env` file or expose private API credentials.

### 4. Start the Application

Run the application using Node.js according to the project's entry configuration.

```bash
node app.js
```

For development, you can also use a tool such as Nodemon.

---

## 🌐 Live Demo

🚀 **Try Wanderlust:**
[Live Application](https://delta-major-project-airbnb.vercel.app/)

---

## 📸 Screenshots

Add screenshots of the application here to showcase the UI.

Recommended sections:

* 🏠 Home Page
* 🔎 Listings
* 🏡 Listing Details
* 🗺️ Interactive Map
* ✏️ Edit Listing
* ⭐ Reviews
* 🔐 Login / Signup

---

## 🎯 What I Learned

Building Wanderlust helped me gain practical experience with:

* Full-stack web development
* MVC architecture
* RESTful routing
* MongoDB & Mongoose
* Authentication & authorization
* CRUD operations
* Session management
* Cloudinary image storage
* File uploads with Multer
* Server-side validation
* Interactive maps
* EJS templating
* Express middleware
* Deployment

---

## 🔮 Future Improvements

Possible future additions include:

* 💳 Online booking & payment system
* ❤️ Wishlist functionality
* 🔍 Advanced search & filtering
* 📅 Availability management
* 📧 Email notifications
* 📱 Improved mobile experience
* 🧑‍💼 Host dashboard
* 📊 Listing analytics

---

## ⚠️ Disclaimer

Wanderlust is an **educational project inspired by Airbnb** and is not affiliated with or endorsed by Airbnb.

---

## 👨‍💻 Author

### Tayyab Yahya

**BS Computer Science Student | MERN Stack Developer | AI/ML Enthusiast**

[GitHub](https://github.com/Tayyab-Yahya)

---

## ⭐ Support

If you like this project, consider giving it a ⭐ on GitHub!

It helps support my learning journey and encourages me to build more projects.

---

> **Built with ☕ JavaScript, Node.js, MongoDB & a lot of debugging.**
