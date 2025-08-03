🔐 Authentication API
This is a simple backend API that handles user authentication using JWT (JSON Web Tokens), cookies, and secure token-based mechanisms. The API supports:
✅ User Registration
🔑 User Login
🔁 Get Current Logged-in User
🚪 Logout

🛠 Tech Stack
Node.js,
Express.js,
JWT (jsonwebtoken),
Cookies (cookie-parser),
bcrypt (for password hashing)

📦 Features
🔐 Register – Create a new user account securely
🔑 Login – Authenticate user and generate a token
👤 Get User – Access current user's data via token from cookie
🚪 Logout – Clear cookie and securely logout the user

📬 API Endpoints

Method	Endpoint	Description	Auth Required

POST	/auth/register	Register new user	
POST	/auth/login	Login existing user
GET	 /auth/user	Get current user info	
POST	/auth/logout	Logout user

🔒 Authentication Flow
1. On login, a JWT is created and sent via HTTP-only cookie.
2. The cookie is automatically attached in future requests.
3. On get user, the JWT from the cookie is verified to identify the user.
4. On logout, the cookie is cleared, ending the session.
