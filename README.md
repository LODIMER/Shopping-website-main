## TechParts Shopping Website

Single-page shopping website for PC components and gaming gear.  
Built with plain HTML, CSS, and JavaScript in one file (`index.html`), using browser `localStorage` for persistence.

## System Summary

The system provides a simple e-commerce flow:

- Browse products with category filters and search
- Register/login account before adding items to cart
- Add products to cart and manage quantity
- Checkout and place orders
- Track order progress in timeline view
- Responsive layout for desktop, tablets, and mobile phones

## Main Features

- **Account system**
  - Register and login modal
  - Session state stored in `localStorage`
  - Logout support
  - Cart and Track Orders access only when logged in

- **Product catalog**
  - Product list rendered from a JavaScript array
  - Category-based product icons
  - Category filter chips on Products page
  - Real-time search tied to Products page

- **Cart management**
  - Add to cart (requires login)
  - Increase/decrease quantity
  - Remove items
  - Live cart count in header

- **Checkout and orders**
  - Shipping address and payment form
  - Shipping method with dynamic totals
  - Order creation with generated order ID
  - Persisted order history

- **Order tracking**
  - Timeline-based status simulation
  - Delivery information
  - Cancel order while in transit

- **Notifications**
  - Toast notification for add-to-cart, auth, and status messages

- **Responsive design**
  - Tablet layout (`<=1024px`)
  - Mobile layout (`<=768px`)
  - Small-phone adjustments (`<=480px`)
  - Hamburger menu for navigation on small screens

## Key JavaScript Functions

- `showPage(pageName)`
  - Handles page-section navigation
  - Prevents logged-out access to cart/tracking

- `registerUser(event)`, `loginUser(event)`, `logoutUser()`
  - Account lifecycle and session handling

- `updateAuthUI()`
  - Updates account button, greeting, and protected nav visibility

- `toggleMobileMenu()`, `closeMobileMenu()`
  - Opens/closes hamburger menu for mobile

- `applyProductFilters()`, `setCategoryFilter(category)`, `searchProducts()`
  - Combined category + search product filtering

- `addToCart(productId)`, `displayCart()`, `increaseQty(index)`, `decreaseQty(index)`, `removeFromCart(index)`
  - Cart operations and rendering

- `displayCheckout()`, `updateShippingCost()`, `updateCheckoutTotals()`, `placeOrder()`
  - Checkout processing and order creation

- `displayOrders()`
  - Renders tracking cards and timeline

- `saveToLocalStorage()`, `loadFromLocalStorage()`, `saveAuthToLocalStorage()`, `loadAuthFromLocalStorage()`
  - Persistence for cart, orders, users, and current session

## Data Persistence

The app stores these keys in browser `localStorage`:

- `users`
- `currentUser`
- `cart`
- `orders`

## How to Run

1. Open `index.html` in a browser.
2. Register or login from **Account**.
3. Browse products, search/filter, and add to cart.
4. Proceed to checkout and place an order.
5. View order status in **Track Orders**.

## Screenshots (Template)

Add your screenshots in a folder named `screenshots/` in this project, then update filenames below if needed.

### Desktop

![Desktop - Home](screenshots/desktop-home.png)
![Desktop - Products](screenshots/desktop-products.png)

### Tablet

![Tablet - Products](screenshots/tablet-products.png)
![Tablet - Cart](screenshots/tablet-cart.png)

### Mobile

![Mobile - Hamburger Menu](screenshots/mobile-menu.png)
![Mobile - Products](screenshots/mobile-products.png)

### Account and Checkout Flow

![Auth - Login/Register](screenshots/auth-modal.png)
![Cart Page](screenshots/cart-page.png)
![Checkout Page](screenshots/checkout-page.png)
![Track Orders Page](screenshots/track-orders-page.png)

## Notes

- This is a front-end school project and does not use a backend/database.
- Login credentials are stored in plain text in `localStorage` for demo purposes only.
