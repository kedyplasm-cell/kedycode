# 🖥️ KEDYCODE // SYSTEM_LOG

A high-end, minimalist tech blog and community guestbook built with **Google Sans Flex** and **Firebase Firestore**. 

---

## 🚀 Features
* **KEDYCODE Aesthetic**: High-contrast dark mode with aggressive typography.
* **Giant Hero**: The latest post is automatically featured as a massive, full-screen headline.
* **Real-time Guestbook**: A "Community Log" where users can transmit messages instantly.
* **NoSQL Backend**: Powered by Firebase for instant data syncing without a server.
* **Responsive**: Designed to scale from mobile screens to ultra-wide monitors.

---

## 🛠️ Setup & Deployment

### 1. Firebase Configuration
Ensure your `index.html` contains your specific Firebase API keys. The database structure requires two collections:
* `posts`: For your blog articles (Fields: `title`, `content`, `imageUrl`, `createdAt`).
* `guestbook`: For user comments (Fields: `username`, `message`, `createdAt`).

### 2. Security Rules
Set your Firestore rules to the following to ensure the blog remains read-only for the public:
```javascript
match /posts/{post} {
  allow read: if true;
  allow write: if false;
}
