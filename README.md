Weekday & Weekend Advice App

A simple web application built with Node.js, Express.js, and EJS that determines whether the current day is a weekday or a weekend and displays a corresponding message.

🚀 Features
Detects the current day of the week
Determines whether it is a weekday or weekend
Uses Express.js to handle HTTP requests
Uses EJS for dynamic page rendering
Passes data from the server to an EJS template
Runs locally on port 3000
🛠️ Technologies
Node.js
Express.js
EJS
JavaScript
HTML
📦 Installation

Clone the repository:

git clone <your-repository-url>

Navigate to the project directory:

cd <project-folder>

Install the dependencies:

npm install
▶️ Running the App

Start the application:

node index.js

The server will run at:

http://localhost:3000

Open this address in your browser to view the application.

📁 Project Structure
project/
├── index.js
├── package.json
├── package-lock.json
└── views/
    └── index.ejs
⚙️ How It Works

The application creates an Express server:

import express from "express";

const app = express();
const port = 3000;

When the user visits the home page, the application gets the current date:

const today = new Date();
const day = today.getDay();

The getDay() method returns a number between 0 and 6.

Value	Day
0	Sunday
1	Monday
2	Tuesday
3	Wednesday
4	Thursday
5	Friday
6	Saturday

The application checks whether the current day is Saturday or Sunday:

if (day === 0 || day === 6) {
    type = "weekend";
    adv = "Enjoy your weekend!";
} else {
    type = "weekday";
    adv = "It's time to work hard!";
}

The values are then passed to the EJS template:

res.render("index.ejs", {
    dayType: type,
    advice: adv
});

EJS uses these variables to dynamically render the page.

💡 Example Output
Weekday
It's a weekday.
It's time to work hard!
Weekend
It's the weekend.
Enjoy your weekend!
🎯 What I Learned

This project helped me practice:

Creating a server with Express.js
Working with Express routes
Using JavaScript's Date object
Writing conditional logic
Using EJS templates
Passing data from Express to EJS
Rendering dynamic web pages
📄 License

This project is created for educational purposes.
