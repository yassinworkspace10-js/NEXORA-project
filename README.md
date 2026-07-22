# 🚀 NEXORA - Modern Web Agency Website

NEXORA is a modern web agency website built with **Node.js**, **Express.js**, **EJS**, and **CSS**. The platform showcases agency services, pricing packages, portfolio projects, and a contact system for collecting client inquiries.

## ✨ Features

* Responsive modern UI
* Dynamic pages using EJS templates
* Portfolio showcase
* Pricing packages page
* About page
* Contact form with Formspree integration
* Custom 404 page
* Draft-saving API for contact forms
* Environment variable support with dotenv
* Static assets support (images, CSS, JS)

---

## 🛠️ Tech Stack

### Backend

* Node.js
* Express.js
* EJS
* dotenv
* body-parser

### Frontend

* HTML5
* CSS3
* JavaScript (Vanilla JS)
* EJS Templates

### External Services

* Formspree (Contact Form Handling)
* Nodemailer (Optional Email Integration)

---

## 📂 Project Structure

```text
NEXORA
│
├── public/
│   ├── css/
│   ├── js/
│   └── images/
│
├── src/
│   └── views/
│       ├── pages/
│       │   ├── home.ejs
│       │   ├── about.ejs
│       │   ├── portfolio.ejs
│       │   ├── packages.ejs
│       │   ├── contact.ejs
│       │   └── 404.ejs
│       │
│       └── partials/
│           ├── header.ejs
│           └── footer.ejs
│
├── .env
├── app.js
├── package.json
└── README.md
```

---

## ⚙️ Installation

### Clone Repository

```bash
git clone https://github.com/your-username/nexora.git
cd nexora
```

### Install Dependencies

```bash
npm install
```

### Create Environment Variables

Create a `.env` file:

```env
PORT=3000

EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password
```

### Run Development Server

```bash
npm start
```

or

```bash
node app.js
```

---

## 🌐 Available Routes

| Route      | Description        |
| ---------- | ------------------ |
| /          | Home Page          |
| /about     | About Us           |
| /portfolio | Portfolio          |
| /packages  | Packages & Pricing |
| /contact   | Contact Page       |
| *          | Custom 404 Page    |

---

## 📬 Contact Form

The contact form is connected to Formspree and supports:

* Client name
* Email address
* Project type
* Package selection
* Budget range
* Deadline
* Project description

After submission, users receive instant feedback without reloading the page.

---

## 💾 Draft API

Save user progress while filling the contact form.

### Save Draft

```http
POST /save-draft
```

Request Body:

```json
{
  "userId": "123",
  "name": "John Doe",
  "email": "john@example.com",
  "package": "Premium",
  "message": "Project details..."
}
```

### Get Draft

```http
GET /draft/:userId
```

Response:

```json
{
  "draft": {
    "name": "John Doe",
    "email": "john@example.com",
    "package": "Premium",
    "message": "Project details..."
  }
}
```

---

## 📧 Optional Email Integration

The project includes a Nodemailer controller that can send messages directly to your email account.

Required environment variables:

```env
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password
```

---

## 🎨 Design Goals

* Modern agency branding
* Fast loading performance
* Mobile-first responsiveness
* Conversion-focused layout
* Clean user experience

---

## 🚀 Future Improvements

* MongoDB integration
* Admin dashboard
* Authentication system
* Project management panel
* Blog section
* Testimonials system
* CMS integration

---

## 👨‍💻 Author

**Yassin Hassan**

Backend Developer (Node.js & MongoDB)

Building modern web experiences with performance, scalability, and clean design in mind.

---

## 📄 License

This project is open-source and available under the MIT License.
