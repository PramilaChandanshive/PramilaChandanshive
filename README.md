# 🌾 AgroMarket



---

# 📂 Project Structure

```text
AgroMarket
│
├── 📁 src
│   │
│   ├── 📁 main
│   │   │
│   │   ├── 📁 java
│   │   │   └── 📁 com
│   │   │       └── 📁 agromarket
│   │   │           │
│   │   │           ├── 🚀 AgroMarketApplication.java
│   │   │           │
│   │   │           ├── 📁 controller
│   │   │           │   ├── PageController.java
│   │   │           │   ├── ProductController.java
│   │   │           │   ├── FarmerController.java
│   │   │           │   ├── CustomerController.java
│   │   │           │   ├── CartController.java
│   │   │           │   ├── OrderController.java
│   │   │           │   ├── ReviewController.java
│   │   │           │   └── AdminController.java
│   │   │           │
│   │   │           ├── 📁 service
│   │   │           │   ├── ProductService.java
│   │   │           │   ├── FarmerService.java
│   │   │           │   ├── CustomerService.java
│   │   │           │   ├── CartService.java
│   │   │           │   ├── OrderService.java
│   │   │           │   ├── ReviewService.java
│   │   │           │   └── AdminService.java
│   │   │           │
│   │   │           ├── 📁 repository
│   │   │           │   ├── UserRepository.java
│   │   │           │   ├── FarmerRepository.java
│   │   │           │   ├── CustomerRepository.java
│   │   │           │   ├── ProductRepository.java
│   │   │           │   ├── CartRepository.java
│   │   │           │   ├── OrderRepository.java
│   │   │           │   ├── OrderItemRepository.java
│   │   │           │   └── ReviewRepository.java
│   │   │           │
│   │   │           ├── 📁 entity
│   │   │           │   ├── User.java
│   │   │           │   ├── Farmer.java
│   │   │           │   ├── Customer.java
│   │   │           │   ├── Product.java
│   │   │           │   ├── Cart.java
│   │   │           │   ├── Order.java
│   │   │           │   ├── OrderItem.java
│   │   │           │   └── Review.java
│   │   │           │
│   │   │           ├── 📁 dto
│   │   │           │   ├── ProductRequest.java
│   │   │           │   ├── OrderRequest.java
│   │   │           │   └── LoginRequest.java
│   │   │           │
│   │   │           └── 📁 exception
│   │   │               ├── ResourceNotFoundException.java
│   │   │               └── GlobalExceptionHandler.java
│   │   │
│   │   └── 📁 resources
│   │       │
│   │       ├── 📁 templates
│   │       │   ├── index.html
│   │       │   ├── login.html
│   │       │   ├── register.html
│   │       │   ├── products.html
│   │       │   ├── product-details.html
│   │       │   ├── cart.html
│   │       │   ├── checkout.html
│   │       │   ├── orders.html
│   │       │   ├── farmer-dashboard.html
│   │       │   └── admin-dashboard.html
│   │       │
│   │       ├── 📁 static
│   │       │   │
│   │       │   ├── 📁 css
│   │       │   │   ├── style.css
│   │       │   │   ├── login.css
│   │       │   │   ├── products.css
│   │       │   │   ├── cart.css
│   │       │   │   └── dashboard.css
│   │       │   │
│   │       │   ├── 📁 js
│   │       │   │   ├── script.js
│   │       │   │   ├── products.js
│   │       │   │   ├── cart.js
│   │       │   │   └── dashboard.js
│   │       │   │
│   │       │   └── 📁 images
│   │       │       ├── logo.png
│   │       │       └── products/
│   │       │
│   │       └── application.properties
│   │
│   └── 📁 test
│
├── 📦 pom.xml
└── 📄 README.md
```
