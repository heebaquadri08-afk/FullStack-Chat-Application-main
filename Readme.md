# Fullstack Chat Application

## Overview
This is a fullstack real-time chat application that allows users to communicate instantly. It includes user authentication, real-time messaging, theme customization, and profile management. The application is built using modern web technologies and provides a seamless user experience.

## Features
- **User Authentication :** Login/Signup functionality with secure authentication.
- **Real-Time Chat :** Instant messaging between users using Socket.io.
- **Theme Customization :** Users can switch between different themes for a personalized experience.
- **Profile Management :** Users can upload and update their profile pictures.
- **Responsive UI :** Designed with React and Tailwind CSS for a smooth and modern interface.

## Tech Stack

### **Frontend**

- **React.js -** For building the user interface.
- **Tailwind CSS -** For responsive and customizable styling.

### **Backend**
- **Node.js -** JavaScript runtime for server-side development.
- **Express.js -** Lightweight and fast backend framework.
- **MongoDB -** NoSQL database for storing user data and messages.

### **Real-Time Communication**
- **Socket.io -** Enables real-time bi-directional communication between users.

## Installation & Setup

### Prerequisites
Make sure you have the following installed:

- Node.js (Latest version)
- MongoDB (Local or cloud instance)
- npm or yarn

## Steps to run the Application
### Backend setup

1. Clone the repository:
```
git clone https://github.com/your-repo/chat-app.git
cd chat-app/backend
```

2. Install dependencies:
```
npm install
```

3. Start the backend server:
```
npm run dev
```

### Frontend Setup

1. Navigate to the frontend directory:
```
cd ../frontend
```
2. Install dependencies:
```
npm install
```
3. Start the frontend server:
```
npm run dev -- --host
```

## Usage
- Sign up or log in to your account.
- Select a user from the available chat list.
- Start real-time messaging with instant updates.
- Change themes from the settings panel.
- Update your profile image from the profile page.

## Future Enhancements
- Functionality to update profile.
- Editing and deleting messages.
- Being able to upload documents and videos as currently only images can be sent.
- A search bar to search for users.
- Using Amazon S3 instead of Cloudinary to support sending large files.

## Accessing via Wi-Fi (Multi-Device Setup)

To use the chat application across different devices (e.g., two laptops on the same Wi-Fi):

### 1. Find Your Local IP Address
On the machine running the backend:
- **Mac/Linux:** Open terminal and run `ifconfig` or `ip addr`. Look for `inet` under `en0` or `wlan0` (e.g., `192.168.1.10`).
- **Windows:** Open CMD and run `ipconfig`. Look for `IPv4 Address`.

### 2. Update Backend Configuration
In `backend/.env`, update the `FRONTEND_URL` to include your local IP:
```env
FRONTEND_URL=http://<YOUR_LOCAL_IP>:5173
```
*Example: `FRONTEND_URL=http://192.168.1.10:5173`*

### 3. Update Frontend Configuration
In `frontend/.env`, update the `VITE_BACKEND_URL` to include your local IP:
```env
VITE_BACKEND_URL=http://<YOUR_LOCAL_IP>:5000
```
*Example: `VITE_BACKEND_URL=http://192.168.1.10:5000`*

### 4. Restart Both Servers
- Restart the backend: `npm start` (in `backend` folder)
- Restart the frontend: `npm run dev` (in `frontend` folder)

### 5. Access from Another Device
1. Ensure both devices are on the **same Wi-Fi**.
2. On the second device, open a browser and navigate to:
   `http://<YOUR_LOCAL_IP>:5173`

---

## Contributions
Contributions are welcome! Feel free to fork this repository and submit a pull request.

## License
This project is licensed under the MIT License.


