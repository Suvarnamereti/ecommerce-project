# 🛒 AI-Enabled E-Commerce Web Application

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Flask](https://img.shields.io/badge/Flask-2.x-black?style=for-the-badge&logo=flask)
![SQLite](https://img.shields.io/badge/SQLite-Database-lightblue?style=for-the-badge&logo=sqlite)
![HTML CSS](https://img.shields.io/badge/HTML%2FCSS-Frontend-orange?style=for-the-badge&logo=html5)
![AI](https://img.shields.io/badge/AI-Recommendation-green?style=for-the-badge&logo=artificial-intelligence)

> A full-stack e-commerce web application built with Python (Flask) and SQLite, featuring an AI-based product recommendation system.

---

## 📌 Table of Contents

- [About the Project](#about-the-project)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [AI Recommendation Logic](#ai-recommendation-logic)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Screenshots](#screenshots)
- [Database Design](#database-design)
- [Resume Description](#resume-description)
- [Future Enhancements](#future-enhancements)
- [Author](#author)

---

## 📖 About the Project

This project is an **AI-Enabled E-Commerce Web Application** that simulates a real-world online shopping platform. It allows users to browse products, add them to a cart, search for items, and receive **AI-powered product recommendations** based on their selections.

Built as a full-stack project, it demonstrates:
- Backend development with Python & Flask
- Database management with SQLite
- Frontend design with HTML & CSS
- Basic Artificial Intelligence / recommendation logic

---

## ✨ Features

| Feature | Description |
|---|---|
| 🛍️ Product Browsing | View all available products with name, price, and image |
| 🔍 Search Products | Search products by name or keyword |
| 🛒 Add to Cart | Add/remove products from shopping cart |
| 🤖 AI Recommendations | Get smart product suggestions based on selected items |
| 👤 User Login/Signup | Secure user authentication system |
| 💳 Payment Simulation | Fake checkout flow for demo purposes |
| 🏷️ Product Filtering | Filter by price range or category |
| 🔧 Admin Panel | Admin interface to add/manage products |

---

## 🛠️ Tech Stack

### Frontend
- **HTML5** — Structure and layout
- **CSS3** — Styling and responsive design

### Backend
- **Python 3.x** — Core programming language
- **Flask** — Lightweight web framework

### Database
- **SQLite** — Lightweight relational database

### AI / Logic
- **Rule-based Recommendation Engine** — Python logic for product suggestions

---

## 🤖 AI Recommendation Logic

The recommendation engine uses a **rule-based AI approach** to suggest related products based on the user's current selection.

```python
def recommend(product):
    """
    AI-based product recommendation function.
    Returns a list of suggested products based on the input product name.
    """
    if "dress" in product.lower():
        return ["Kurti", "Leggings", "Handbag", "Sandals"]
    elif "laptop" in product.lower():
        return ["Mouse", "Keyboard", "Laptop Bag", "USB Hub"]
    elif "phone" in product.lower():
        return ["Phone Cover", "Earphones", "Charger", "Screen Guard"]
    elif "shoes" in product.lower():
        return ["Socks", "Shoe Rack", "Insoles", "Laces"]
    else:
        return ["Popular Item 1", "Popular Item 2", "Best Seller"]
```

> 💡 **How it works:** When a user views a product, the `recommend()` function checks the product category and returns a list of complementary products — similar to how Amazon's "Customers also bought" feature works.

---

## 📁 Project Structure

```
ai-ecommerce/
│
├── app.py                  # Main Flask application
├── database.py             # Database setup and queries
├── recommend.py            # AI recommendation logic
├── requirements.txt        # Python dependencies
├── README.md               # Project documentation
│
├── templates/              # HTML templates (Jinja2)
│   ├── index.html          # Home / Product listing page
│   ├── product.html        # Individual product page
│   ├── cart.html           # Shopping cart page
│   ├── search.html         # Search results page
│   ├── login.html          # User login page
│   ├── signup.html         # User registration page
│   └── checkout.html       # Checkout / payment simulation
│
├── static/                 # Static files
│   ├── css/
│   │   └── style.css       # Main stylesheet
│   ├── js/
│   │   └── main.js         # JavaScript (optional)
│   └── images/             # Product images
│
└── ecommerce.db            # SQLite database file
```

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:
- Python 3.x
- pip (Python package manager)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/ai-ecommerce.git
   cd ai-ecommerce
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate        # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Initialize the database**
   ```bash
   python database.py
   ```

5. **Run the application**
   ```bash
   python app.py
   ```

6. **Open in browser**
   ```
   http://127.0.0.1:5000
   ```

### Requirements (requirements.txt)

```
Flask==2.3.0
Werkzeug==2.3.0
```

---

## 🗄️ Database Design

### Tables

**`users` Table**
| Column | Type | Description |
|---|---|---|
| id | INTEGER | Primary key |
| username | TEXT | User's name |
| email | TEXT | User's email |
| password | TEXT | Hashed password |

**`products` Table**
| Column | Type | Description |
|---|---|---|
| id | INTEGER | Primary key |
| name | TEXT | Product name |
| price | REAL | Product price |
| category | TEXT | Product category |
| image | TEXT | Image filename |
| description | TEXT | Product description |

**`cart` Table**
| Column | Type | Description |
|---|---|---|
| id | INTEGER | Primary key |
| user_id | INTEGER | Foreign key → users |
| product_id | INTEGER | Foreign key → products |
| quantity | INTEGER | Number of items |

---

## 📸 Screenshots

> 📷 Add screenshots of your project here after running it locally.

| Page | Screenshot |
|---|---|
| Home / Product Listing | *(Add screenshot)* |
| Product Detail + AI Recommendations | *(Add screenshot)* |
| Shopping Cart | *(Add screenshot)* |
| Login / Signup | *(Add screenshot)* |

---

## 📄 Resume Description

```
Project: AI-Enabled E-Commerce Web Application
• Developed a full-stack e-commerce website using Python (Flask) and SQLite
• Implemented product browsing, cart management, and search functionality
• Integrated a basic AI-based recommendation system for personalized product suggestions
• Designed a responsive user interface using HTML and CSS for improved user experience
• Built user authentication (login/signup) and a simulated payment/checkout module
```

---

## 🔮 Future Enhancements

- [ ] Machine Learning-based recommendation (collaborative filtering)
- [ ] Payment gateway integration (Razorpay / Stripe)
- [ ] Product reviews and ratings system
- [ ] Order history and tracking
- [ ] REST API for mobile app support
- [ ] Email notifications for orders

---

## 🎤 Viva / Interview Q&A

**Q1: What is an e-commerce system?**
> A platform that allows buying and selling products online.

**Q2: Where is AI used in your project?**
> In the product recommendation module — it suggests related products based on the user's selected item category.

**Q3: What is Flask?**
> Flask is a lightweight Python web framework used to build web applications quickly with minimal boilerplate code.

**Q4: Why SQLite?**
> SQLite is a serverless, file-based database — ideal for small projects and development environments. No setup required.

**Q5: How does your recommendation system work?**
> It uses rule-based logic — when a user selects a product, the system checks the product category and returns a predefined list of complementary products.

---

## 👩‍💻 Author

**Your Name**
- GitHub: [@your-username](https://github.com/your-username)
- LinkedIn: [your-linkedin](https://linkedin.com/in/your-profile)
- Email: your.email@example.com

---

## 📃 License

This project is open source and available under the [MIT License](LICENSE).

---

⭐ **If you found this project helpful, please give it a star!** ⭐
