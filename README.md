# User-Reg-Api

Project Setup: Initialize a Node.js project and install necessary packages.

Run npm init -y in your project directory.
Install dependencies: npm install express mongoose bcrypt jsonwebtoken dotenv.

Database Connection: Set up a connection to your MongoDB database (e.g., using MongoDB Atlas for a cloud-hosted solution) with Mongoose.

User Model: Define the Mongoose schema for the User collection. This model specifies fields like username, email, and password.

Registration Logic (Signup):
Create a POST route (/api/auth/signup) to receive user credentials.
Validate user input (e.g., check if email already exists, password length).
Hash the user's password using Bcrypt before saving it to the database.

Login Logic (Signin):
Create a POST route (/api/auth/signin) to handle login requests.
Find the user in the database by their username or email.
Compare the provided password with the stored hashed password using Bcrypt's comparison function.
If credentials are valid, generate a JWT token and send it to the client.

Authentication Middleware: Implement middleware to verify the JWT on protected routes. This ensures only authenticated users can access specific resources. 
