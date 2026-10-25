# Paradise Nursery Shopping Cart Application
https://github.com/chetanagrawal721/e-plantShopping/blob/main/README.md

**Project Name:** Paradise Nursery Shopping Cart Application (e-plantShopping)  
**Repository:** https://github.com/chetanagrawal721/e-plantShopping  

---

A responsive e-commerce web application developed for **Paradise Nursery**, an online plant store where green meets serenity. This project provides users with an intuitive, dynamic shopping experience to browse house plants across multiple categories, view plant details, manage a shopping cart using Redux Toolkit state management, and calculate real-time order totals.

---

## 🌿 Project Overview

The **Paradise Nursery (e-plantShopping) Shopping Cart Application** is built with **React**, **Vite**, and **Redux Toolkit**. It allows users to:
1. Land on an engaging homepage introducing Paradise Nursery, its values, and mission.
2. Browse a rich catalog of house plants grouped logically into five distinct categories.
3. Add plants to their shopping cart with instant UI feedback (button changes to "Added to Cart" and becomes disabled).
4. Monitor their cart count dynamically in the navigation bar.
5. Manage their shopping cart by incrementing/decrementing quantities, viewing sub-totals and grand totals, removing items, and proceeding towards checkout.

---

## ✨ Features

- **Landing Page (`App.jsx` & `App.css`):**
  - Full-screen scenic greenhouse background image (`.background-image`).
  - Company branding: "Welcome To Paradise Nursery" and tagline "Where Green Meets Serenity".
  - Informative "About Us" section highlighting plant benefits and company background.
  - Interactive "Get Started" button to transition into the plant shop.

- **Product Catalog (`ProductList.jsx`):**
  - Grouped categories with headings:
    - *Air Purifying Plants* (Snake Plant, Spider Plant, Peace Lily, Boston Fern, Rubber Plant, Aloe Vera)
    - *Aromatic Fragrant Plants* (Lavender, Jasmine, Rosemary, Mint, Lemon Balm, Hyacinth)
    - *Insect Repellent Plants* (Oregano, Marigold, Geraniums, Basil, Lavender, Catnip)
    - *Medicinal Plants* (Aloe Vera, Echinacea, Peppermint, Lemon Balm, Chamomile, Calendula)
    - *Low Maintenance Plants* (ZZ Plant, Pothos, Snake Plant, Cast Iron Plant, Succulents, Aglaonema)
  - Detailed product cards containing plant thumbnail, name, description, unit price, and an "Add to Cart" button.
  - State tracking: Buttons dynamically show "Added to Cart" and disable once an item is added to the cart using `addedToCart[plant.name]`.

- **Navigation & Dynamic Cart Badge:**
  - Responsive navigation bar with company logo and brand name (`className="navbar"`).
  - Navigation links to all three views:
    - **Home:** Clicking company branding calls `handleParadiseNurseyClick` and returns the user to the landing page.
    - **Plants:** Clicking "Plants" calls `handlePlantsClick` and displays the plant product catalog.
    - **Cart:** Clicking the cart icon calls `handleCartClick` and toggles the shopping cart view.
  - Cart icon with a live quantity badge displaying the total number of items currently in the cart (`calculateTotalQuantity`).
  - Navbar is rendered at top level and displayed consistently on both Product Listing and Cart pages.

- **Shopping Cart Management (`CartItem.jsx`):**
  - Complete list of added items showing thumbnail, title, and unit price.
  - Quantity adjustments: Increment (`+`) and Decrement (`-`) buttons.
  - Automatically removes items if decremented below 1.
  - Explicit "Delete" button to remove items completely.
  - Dynamic subtotal calculation per item ($\text{Unit Cost} \times \text{Quantity}$).
  - Live Grand Total amount for all items in the cart.
  - "Continue Shopping" button returning the user to the catalog.
  - "Checkout" button triggering a confirmation alert ("Functionality to be added for future reference").

- **State Management (`CartSlice.jsx`):**
  - Redux Toolkit slice containing reducers:
    - `addItem`: Adds plant to cart or increments quantity if already present.
    - `removeItem`: Filters out plant by name.
    - `updateQuantity`: Adjusts item quantity based on payload.

---

## 🛠️ Tech Stack

- **Frontend Framework:** React 18
- **Build Tool:** Vite
- **State Management:** Redux Toolkit (`@reduxjs/toolkit`) & React-Redux (`react-redux`)
- **Styling:** CSS3 (Flexbox, responsive media queries, CSS transitions)
- **Language:** JavaScript (ES6+)

---

## 📁 Project Structure

```
e-plantShopping/
├── public/
│   └── vite.svg
├── src/
│   ├── assets/
│   │   └── react.svg
│   ├── AboutUs.css
│   ├── AboutUs.jsx
│   ├── App.css
│   ├── App.jsx
│   ├── CartItem.css
│   ├── CartItem.jsx
│   ├── CartSlice.jsx
│   ├── index.css
│   ├── main.jsx
│   ├── ProductList.css
│   ├── ProductList.jsx
│   └── store.js
├── index.html
├── package.json
├── README.md
└── vite.config.js
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js (v18 or higher recommended)
- npm (Node Package Manager)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/chetanagrawal721/e-plantShopping.git
   cd e-plantShopping
   ```

2. Install the dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

4. Build for production:
   ```bash
   npm run build
   ```

5. Preview the production build:
   ```bash
   npm run preview
   ```

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
