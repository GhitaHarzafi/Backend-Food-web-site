# Food Website Backend

A complete PHP-based food ordering website backend with user authentication, product management, shopping cart functionality, and admin panel.

## 🍕 Features

### User Features
- **User Registration & Login**: Secure user authentication system
- **Product Browsing**: View products by categories (Pizza, Burger, Dessert, Drinks, etc.)
- **Shopping Cart**: Add/remove items, update quantities
- **Order Management**: Place orders with delivery address
- **Profile Management**: Update personal information and addresses
- **Search Functionality**: Search products by name
- **Contact Form**: Send messages to admin

### Admin Features
- **Admin Dashboard**: Overview of orders, users, and products
- **Product Management**: Add, edit, and delete products
- **Order Management**: View and manage customer orders
- **User Management**: View and manage user accounts
- **Message Center**: View customer messages
- **Admin Authentication**: Secure admin login system

## 🛠️ Technology Stack

- **Backend**: PHP 8.1+
- **Database**: MySQL/MariaDB
- **Frontend**: HTML, CSS, JavaScript
- **Database Connection**: PDO
- **Server**: Apache/Nginx (XAMPP/WAMP recommended)

## 📋 Prerequisites

Before running this project, make sure you have:

- PHP 8.1 or higher
- MySQL/MariaDB database server
- Web server (Apache/Nginx)
- XAMPP, WAMP, or similar local development environment

## 🚀 Installation

### 1. Clone or Download the Project
```bash
# If using git
git clone <repository-url>
# Or download and extract the ZIP file
```

### 2. Set Up Database
1. Start your MySQL server
2. Create a new database named `food_db`
3. Import the database schema:
   ```bash
   mysql -u root -p food_db < food_db.sql
   ```
   Or use phpMyAdmin to import the `food_db.sql` file

### 3. Configure Database Connection
Edit `components/connect.php` with your database credentials:
```php
$db_name = 'mysql:host=localhost;dbname=food_db';
$user_name = 'your_username';
$user_password = 'your_password';
```

### 4. Set Up Web Server
1. Place the project files in your web server's document root
   - For XAMPP: `htdocs/food-website-backend/`
   - For WAMP: `www/food-website-backend/`
2. Start your web server and MySQL services

### 5. Access the Application
- **User Interface**: `http://localhost/food-website-backend/`
- **Admin Panel**: `http://localhost/food-website-backend/admin/`

## 👤 Default Admin Credentials

- **Username**: admin
- **Password**: admin123

**⚠️ Important**: Change the default admin password after first login for security.

## 📁 Project Structure

```
food-website-backend/
├── admin/                 # Admin panel files
│   ├── dashboard.php     # Admin dashboard
│   ├── products.php      # Product management
│   ├── orders.php        # Order management
│   └── ...
├── components/           # Reusable components
│   ├── connect.php      # Database connection
│   ├── header.php       # Common header
│   └── footer.php       # Common footer
├── css/                 # Stylesheets
│   ├── style.css        # User interface styles
│   └── admin_style.css  # Admin panel styles
├── js/                  # JavaScript files
│   ├── script.js        # User interface scripts
│   └── admin_script.js  # Admin panel scripts
├── images/              # Static images
├── uploaded_img/        # Product images upload directory
├── food_db.sql          # Database schema
└── README.md           # This file
```

## 🗄️ Database Schema

The application uses the following main tables:

- **users**: Customer account information
- **admin**: Admin user credentials
- **products**: Product catalog with categories
- **cart**: Shopping cart items
- **orders**: Customer orders
- **messages**: Customer contact messages

## 🔧 Configuration

### File Permissions
Ensure the `uploaded_img/` directory has write permissions for image uploads:
```bash
chmod 755 uploaded_img/
```

### Security Considerations
1. Change default admin credentials
2. Use strong passwords for database
3. Enable HTTPS in production
4. Regularly backup your database
5. Keep PHP and MySQL updated

## 🚀 Usage

### For Users
1. Register a new account or login
2. Browse products by category
3. Add items to cart
4. Proceed to checkout
5. Place order with delivery details

### For Admins
1. Login to admin panel
2. Manage products (add/edit/delete)
3. View and process orders
4. Monitor user accounts
5. Respond to customer messages

## 🐛 Troubleshooting

### Common Issues

1. **Database Connection Error**
   - Verify MySQL service is running
   - Check database credentials in `components/connect.php`
   - Ensure database `food_db` exists

2. **Image Upload Issues**
   - Check `uploaded_img/` directory permissions
   - Verify PHP upload settings in `php.ini`

3. **Page Not Found**
   - Ensure web server is running
   - Check file paths and URL configuration
   - Verify `.htaccess` settings (if using Apache)

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📞 Support

For support and questions:
- Create an issue in the repository
- Contact the development team
- Check the troubleshooting section above

## 🔄 Updates

Stay updated with the latest features and security patches by regularly checking for updates.

---

**Happy Coding! 🍕🍔🍰** 