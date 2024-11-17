# Zekrom

A simple, elegant e-shopping website built using **PHP**, **MySQL**, and **plain CSS**. This project is designed to provide a straightforward e-commerce experience. Users can browse products, view details, and navigate seamlessly across pages. The backend database is managed using **MySQL**, running through the **XAMPP suite**, which provides an easy way to test and develop the project locally.

---

## 📖 Features
- **Homepage**: Displays the most recently added products.
- **Shop Page**: Shows all available products with their details.
- **Product Navigation**: Simple and intuitive, similar to any other e-commerce website.
- **Backend**: Manages products with MySQL, including product details like price, description, and stock quantity.

---

## 🛠️ Tech Stack
- **PHP**: Handles backend logic and server-side scripting.
- **CSS**: Implements the styling and layout.
- **MySQL**: Manages the product database.
- **XAMPP Suite**: Provides an easy way to host and run the application locally.

---

## 🚀 Getting Started

### Prerequisites
1. **XAMPP Suite**: Ensure XAMPP is installed and running on your system.
2. **PDO Extension**: Make sure the **PDO extension** is enabled (it should be included and enabled by default in PHP).

---

### 📂 Cloning the Repository
Clone this repository into the correct directory for XAMPP:
- **Linux**: `/opt/lampp/htdocs/`
- **Windows**: `C:\xampp\htdocs\`

```bash
# Navigate to the htdocs directory
cd /opt/lampp/htdocs    # Linux
cd C:\xampp\htdocs      # Windows

# Clone the repository
git clone https://github.com/your-repo/shopping-cart.git
```

---

### 🛠️ Setting up the Database
After starting XAMPP (ensure Apache and MySQL are running), follow these steps to set up the database:

1. Open phpMyAdmin by navigating to:  
   **[http://localhost/phpmyadmin/](http://localhost/phpmyadmin/)**

2. Create the database:
   - Click the **Databases** tab at the top.
   - Under **Create database**, type `shoppingcart` in the text box.
   - Select `utf8_general_ci` as the collation.
   - Click **Create**.

3. Use the following SQL command to create the `products` table:

```sql
CREATE TABLE IF NOT EXISTS `products` (
    `id` int(11) NOT NULL AUTO_INCREMENT,
    `title` varchar(200) NOT NULL,
    `description` text NOT NULL,
    `price` decimal(7,2) NOT NULL,
    `rrp` decimal(7,2) NOT NULL DEFAULT '0.00',
    `quantity` int(11) NOT NULL,
    `img` text NOT NULL,
    `date_added` datetime NOT NULL DEFAULT CURRENT_TIMESTAMP,
    PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=6 DEFAULT CHARSET=utf8;
```

---

### 🌐 Running the Application
1. Open your browser and navigate to **[http://localhost/shopping-cart/](http://localhost/shoppingcart/)**.

2. Explore:
   - **Homepage**: Displays the recently added products with a sleek design.
   - **Shop Page**: Lists all the products in the database with detailed information, including prices, descriptions, and images.

---

### 🗒️ Notes
- **Navigation**: The website provides a clean and simple navigation experience, ensuring users can easily browse products and access pages like the shop or homepage.
- **Styling**: The layout is styled using plain CSS for a lightweight and responsive design.

---

## 🤝 Contributing
Feel free to submit pull requests, suggest enhancements, or report issues.

1. Fork the repository.
2. Create your feature branch: `git checkout -b feature/YourFeature`.
3. Commit your changes: `git commit -m "Add your message here"`.
4. Push to the branch: `git push origin feature/YourFeature`.
5. Open a pull request.

---

Happy Coding! 🚀
