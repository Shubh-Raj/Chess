# Chess Game (Node.js, Express, Socket.io, Chess.js)

This is a real-time multiplayer Chess Game built using **Node.js, Express, Socket.io, and Chess.js**. Players can play against each other with real-time updates.

---

## **🚀 Features**
- **Real-time multiplayer gameplay** using WebSockets (Socket.io).
- **Drag-and-drop chess pieces** with valid move enforcement.
- **Board synchronization** between players.
- **Spectator mode** for additional users.
- **Turn-based system** with automatic role assignment (White/Black).

---

## **📌 Technologies Used**
- **Frontend**: HTML, CSS, JavaScript
- **Backend**: Node.js, Express (Deployed on Render)
- **WebSockets**: Socket.io
- **Chess Logic**: Chess.js
- **Hosting**: Render (Backend)

---

## **💻 How to Run Locally**
### **1️⃣ Clone the Repository**
```sh
git clone https://github.com/yourusername/chess-game.git
cd chess-game
```

### **2️⃣ Install Dependencies**
```sh
npm install
```

### **3️⃣ Update Socket Connection (if needed)**
If your frontend uses a deployed backend URL, modify `chessgame.js` to use localhost:
```js
const socket = io("http://localhost:3000");
```
Or use a dynamic approach:
```js
const socket = io(
  window.location.hostname === "localhost"
    ? "http://localhost:3000"
    : "https://your-render-backend-url.com"
);
```

### **4️⃣ Start the Server**
```sh
npm start
```

The server will run at: **`http://localhost:3000`**

### **5️⃣ Open in Browser**
Visit **`http://localhost:3000`** in your browser.
- Open two tabs to test multiplayer functionality.
- The first player gets **White**, and the second player gets **Black**.
- Additional players will join as **spectators**.

---

## **🔧 Troubleshooting**
### **1️⃣ WebSockets Not Working?**
- Make sure the **backend is running** (`npm start`).
- Check browser console (`F12 → Console`) for errors.
- Ensure **CORS is enabled** in `app.js`:
  ```js
  const cors = require("cors");
  app.use(cors());
  ```
- Restart server after changes: `Ctrl + C`, then `npm start`.

### **2️⃣ 404 Not Found on Render?**
- Ensure your **Render deployment** is successful.
- Check your **Render logs** for errors.
- Redeploy if necessary.

---

## **🛠️ Future Improvements**
- **Add AI Bot for Single Player Mode** 🎯
- **Improve UI with Chess Piece Animations** 🎨
- **Implement Player Chat System** 💬

---

🚀 **Happy Chess Playing!** ♟️🔥

