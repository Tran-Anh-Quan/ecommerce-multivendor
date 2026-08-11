# Cấu trúc dự án (Project Structure)

Bước 1
↓
Build Spring Boot project
↓
Bước 2
↓
Kết nối MySQL
↓
Bước 3
↓
Thiết kế Entity + Database
↓
Bước 4
↓
Repository
↓
Bước 5
↓
Service
↓
Bước 6
↓
Spring Security
↓
Bước 7
↓
Đăng ký / Đăng nhập
↓
Bước 8
↓
Phân quyền Admin / Seller / Customer
↓
Bước 9
↓
Quản lý sản phẩm
↓
Bước 10
↓
Giỏ hàng + Đặt hàng
↓
Bước 11
↓
Quản lý Seller
↓
Bước 12
↓
Admin Dashboard

ecommerce-multivendor/
│
├── pom.xml
│
├── mvnw
├── mvnw.cmd
│
└── src/
    │
    ├── main/
    │   │
    │   ├── java/
    │   │   └── vn/
    │   │       └── edu/
    │   │           └── eaut/
    │   │               └── ecommerce/
    │   │
    │   │                   ├── EcommerceMultivendorApplication.java
    │   │                   │
    │   │                   ├── config/
    │   │                   │   ├── SecurityConfig.java
    │   │                   │   ├── JpaConfig.java
    │   │                   │   └── DataInitializer.java
    │   │                   │
    │   │                   ├── security/
    │   │                   │   ├── CustomUserDetails.java
    │   │                   │   ├── CustomUserDetailsService.java
    │   │                   │   └── CustomAuthenticationSuccessHandler.java
    │   │                   │
    │   │                   ├── controller/
    │   │                   │   ├── HomeController.java
    │   │                   │   ├── AuthController.java
    │   │                   │   ├── ProductController.java
    │   │                   │   ├── CategoryController.java
    │   │                   │   ├── CartController.java
    │   │                   │   ├── OrderController.java
    │   │                   │   ├── ReviewController.java
    │   │                   │   │
    │   │                   │   ├── admin/
    │   │                   │   │   ├── AdminDashboardController.java
    │   │                   │   │   ├── AdminAccountController.java
    │   │                   │   │   ├── AdminSellerController.java
    │   │                   │   │   ├── AdminProductController.java
    │   │                   │   │   ├── AdminCategoryController.java
    │   │                   │   │   ├── AdminOrderController.java
    │   │                   │   │   └── AdminReportController.java
    │   │                   │   │
    │   │                   │   ├── seller/
    │   │                   │   │   ├── SellerDashboardController.java
    │   │                   │   │   ├── SellerProductController.java
    │   │                   │   │   ├── SellerOrderController.java
    │   │                   │   │   ├── SellerInventoryController.java
    │   │                   │   │   ├── SellerReportController.java
    │   │                   │   │   └── SellerProfileController.java
    │   │                   │   │
    │   │                   │   └── customer/
    │   │                   │       ├── CustomerController.java
    │   │                   │       ├── CustomerOrderController.java
    │   │                   │       └── CustomerProfileController.java
    │   │                   │
    │   │                   ├── entity/
    │   │                   │   ├── Account.java
    │   │                   │   ├── Role.java
    │   │                   │   ├── Seller.java
    │   │                   │   ├── SellerApplication.java
    │   │                   │   │
    │   │                   │   ├── Category.java
    │   │                   │   ├── Product.java
    │   │                   │   ├── ProductImage.java
    │   │                   │   ├── ProductVariant.java
    │   │                   │   │
    │   │                   │   ├── Inventory.java
    │   │                   │   ├── InventoryTransaction.java
    │   │                   │   │
    │   │                   │   ├── Cart.java
    │   │                   │   ├── CartItem.java
    │   │                   │   │
    │   │                   │   ├── Order.java
    │   │                   │   ├── OrderItem.java
    │   │                   │   ├── Payment.java
    │   │                   │   ├── Shipment.java
    │   │                   │   │
    │   │                   │   ├── Review.java
    │   │                   │   ├── Wishlist.java
    │   │                   │   └── WishlistItem.java
    │   │                   │
    │   │                   ├── repository/
    │   │                   │   ├── AccountRepository.java
    │   │                   │   ├── RoleRepository.java
    │   │                   │   ├── SellerRepository.java
    │   │                   │   ├── SellerApplicationRepository.java
    │   │                   │   │
    │   │                   │   ├── CategoryRepository.java
    │   │                   │   ├── ProductRepository.java
    │   │                   │   ├── ProductImageRepository.java
    │   │                   │   ├── ProductVariantRepository.java
    │   │                   │   │
    │   │                   │   ├── InventoryRepository.java
    │   │                   │   ├── InventoryTransactionRepository.java
    │   │                   │   │
    │   │                   │   ├── CartRepository.java
    │   │                   │   ├── CartItemRepository.java
    │   │                   │   │
    │   │                   │   ├── OrderRepository.java
    │   │                   │   ├── OrderItemRepository.java
    │   │                   │   ├── PaymentRepository.java
    │   │                   │   ├── ShipmentRepository.java
    │   │                   │   │
    │   │                   │   ├── ReviewRepository.java
    │   │                   │   ├── WishlistRepository.java
    │   │                   │   └── WishlistItemRepository.java
    │   │                   │
    │   │                   ├── service/
    │   │                   │   ├── AccountService.java
    │   │                   │   ├── RoleService.java
    │   │                   │   ├── SellerService.java
    │   │                   │   ├── SellerApplicationService.java
    │   │                   │   │
    │   │                   │   ├── CategoryService.java
    │   │                   │   ├── ProductService.java
    │   │                   │   ├── ProductImageService.java
    │   │                   │   ├── ProductVariantService.java
    │   │                   │   │
    │   │                   │   ├── InventoryService.java
    │   │                   │   ├── CartService.java
    │   │                   │   ├── OrderService.java
    │   │                   │   ├── PaymentService.java
    │   │                   │   ├── ShipmentService.java
    │   │                   │   │
    │   │                   │   ├── ReviewService.java
    │   │                   │   └── WishlistService.java
    │   │                   │
    │   │                   ├── dto/
    │   │                   │   ├── auth/
    │   │                   │   │   ├── LoginRequest.java
    │   │                   │   │   └── RegisterRequest.java
    │   │                   │   │
    │   │                   │   ├── account/
    │   │                   │   │   └── AccountDTO.java
    │   │                   │   │
    │   │                   │   ├── product/
    │   │                   │   │   ├── ProductRequest.java
    │   │                   │   │   ├── ProductResponse.java
    │   │                   │   │   └── ProductSearchRequest.java
    │   │                   │   │
    │   │                   │   ├── seller/
    │   │                   │   │   ├── SellerRequest.java
    │   │                   │   │   └── SellerResponse.java
    │   │                   │   │
    │   │                   │   └── order/
    │   │                   │       ├── OrderRequest.java
    │   │                   │       └── OrderResponse.java
    │   │                   │
    │   │                   ├── exception/
    │   │                   │   ├── ResourceNotFoundException.java
    │   │                   │   ├── UnauthorizedException.java
    │   │                   │   ├── BusinessException.java
    │   │                   │   └── GlobalExceptionHandler.java
    │   │                   │
    │   │                   ├── mapper/
    │   │                   │   ├── ProductMapper.java
    │   │                   │   ├── AccountMapper.java
    │   │                   │   └── OrderMapper.java
    │   │                   │
    │   │                   └── util/
    │   │                       ├── SecurityUtils.java
    │   │                       ├── FileUploadUtils.java
    │   │                       └── Constants.java
    │   │
    │   └── resources/
    │       │
    │       ├── templates/
    │       │   │
    │       │   ├── fragments/
    │       │   │   ├── header.html
    │       │   │   ├── navbar.html
    │       │   │   ├── footer.html
    │       │   │   ├── sidebar.html
    │       │   │   └── alerts.html
    │       │   │
    │       │   ├── auth/
    │       │   │   ├── login.html
    │       │   │   ├── register.html
    │       │   │   └── forgot-password.html
    │       │   │
    │       │   ├── customer/
    │       │   │   ├── profile.html
    │       │   │   ├── orders.html
    │       │   │   ├── order-detail.html
    │       │   │   └── wishlist.html
    │       │   │
    │       │   ├── product/
    │       │   │   ├── list.html
    │       │   │   ├── detail.html
    │       │   │   └── search.html
    │       │   │
    │       │   ├── cart/
    │       │   │   ├── cart.html
    │       │   │   └── checkout.html
    │       │   │
    │       │   ├── seller/
    │       │   │   ├── dashboard.html
    │       │   │   ├── products.html
    │       │   │   ├── product-form.html
    │       │   │   ├── orders.html
    │       │   │   ├── inventory.html
    │       │   │   ├── reports.html
    │       │   │   └── profile.html
    │       │   │
    │       │   ├── admin/
    │       │   │   ├── dashboard.html
    │       │   │   ├── accounts.html
    │       │   │   ├── sellers.html
    │       │   │   ├── seller-detail.html
    │       │   │   ├── products.html
    │       │   │   ├── categories.html
    │       │   │   ├── orders.html
    │       │   │   └── reports.html
    │       │   │
    │       │   ├── error/
    │       │   │   ├── 403.html
    │       │   │   ├── 404.html
    │       │   │   └── 500.html
    │       │   │
    │       │   └── index.html
    │       │
    │       ├── static/
    │       │   │
    │       │   ├── css/
    │       │   │   ├── style.css
    │       │   │   ├── auth.css
    │       │   │   ├── customer.css
    │       │   │   ├── seller.css
    │       │   │   └── admin.css
    │       │   │
    │       │   ├── js/
    │       │   │   ├── main.js
    │       │   │   ├── cart.js
    │       │   │   ├── product.js
    │       │   │   ├── seller.js
    │       │   │   └── admin.js
    │       │   │
    │       │   └── images/
    │       │       ├── products/
    │       │       ├── avatars/
    │       │       └── banners/
    │       │
    │       └── application.properties
    │
    └── test/
        └── java/
            └── vn/
                └── edu/
                    └── eaut/
                        └── ecommerce/
                            ├── controller/
                            ├── service/
                            └── repository/
```
