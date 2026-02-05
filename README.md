Add to Cart Feature Testing (RICEPOT Framework)

## 📌 Project Overview
This project focuses on designing a comprehensive test suite for the **"Add to Cart"** feature of the [StackDemo](https://www.bstackdemo.com/) e-commerce application. 

The test cases were generated using the **RICEPOT Framework**, a structured prompt engineering methodology designed to act as a Senior QA Lead.

## 🛠️ The RICEPOT Methodology
This project utilizes the **RICEPOT** framework to ensure high-quality, structured output:
- **R - Role**: Senior QA Engineer / QA Lead.
- **I - Instructions**: Test the "Add to Cart" functionality with specific focus on positive, negative, and edge cases.
- **C - Context**: E-commerce web application (`bstackdemo.com`) with cart panels, pricing, and quantities.
- **E - Example**: Provided structured formats for test case definitions.
- **P - Parameters**: Defined scope including UI, Functional, Calculation, and Persistence testing.
- **O - Output**: High-density structured test cases in multiple formats.
- **T - Tone**: Professional, structured, and risk-focused.

## 📂 Project Artifacts
The following files have been generated as part of this project:

| File Name | Description | Suggested Use |
| :--- | :--- | :--- |
| **[Detailed Test Execution Report](#-detailed-test-execution-report)** | The full test report in this README. | **Tap here to view the report directly on Git.** |

## 🧪 Test Coverage
The suite includes **30 Test Cases** covering:
- ✅ **Functional**: Adding items, updating quantities (grid & cart), removing items.
- ⚡ **Performance**: Rapid clicking/stress testing.
- 🧮 **Calculations**: Subtotal, installments, and currency accuracy.
- 💾 **Persistence**: Refresh and new tab capability.
- 🎨 **UI/UX**: Animations, layout, and mobile responsiveness.

## 📊 Detailed Test Execution Report

| ID | Category | Summary | Preconditions | Steps | Expected Result | Priority |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **TC_01** | Functional (Pos) | Add single valid item to cart | Homepage loaded | 1. Click 'Add to cart' on 'iPhone 12'. | Cart opens; Item added; Qty=1; Subtotal=$799.00. | High |
| **TC_02** | Functional (Pos) | Add multiple distinct items | 'iPhone 12' in cart | 1. Click 'Add to cart' on 'iPhone 12 Mini'. | Cart has 2 unique items; Total = Sum of both prices. | High |
| **TC_03** | Functional (Pos) | Increase quantity via Product Grid | 'iPhone 12' (Qty:1) in cart | 1. Click 'Add to cart' on 'iPhone 12' again. | Qty becomes 2; Item row is NOT duplicated; Price updates. | High |
| **TC_04** | Functional (Pos) | Increase quantity via Cart (+) button | Cart open with item | 1. Click '+' button next to item. | Qty increases by 1; Subtotal recalculates immediately. | Medium |
| **TC_05** | Functional (Pos) | Decrease quantity via Cart (-) button | Item Qty > 1 | 1. Click '-' button next to item. | Qty decreases by 1; Subtotal recalculates. | Medium |
| **TC_06** | Functional (Pos) | Remove item via 'X' button | Item in cart | 1. Click 'X' icon on the item row. | Item removed specifically; Subtotal reduces; If 0 items, cart shows empty state. | High |
| **TC_07** | Functional (Neg) | Rapid click 'Add to Cart' (Performance) | Homepage loaded | 1. Click 'Add to cart' 10 times quickly. | App handles requests; Qty matches clicks (10); No UI freeze. | High |
| **TC_08** | Calculation | Verify Subtotal Accuracy | Cart has multiple items | 1. Sum individual (Price * Qty) manually. <br> 2. Compare with 'Subtotal'. | Manual sum matches displayed Subtotal exactly. | High |
| **TC_09** | Calculation | Verify Currency Formatting | 3+ items in cart | 1. Check all prices in Cart. | All prices have '$' prefix; 2 decimal places (e.g., 88.78). | Low |
| **TC_10** | UI/UX | Cart Slide-out Animation | Cart closed | 1. Click 'Add to cart'. | Cart panel slides in smoothly from right; No layout shift on main page. | Low |
| **TC_11** | UI/UX | Cart Badge Counter Update | Cart empty | 1. Add 1 item. <br> 2. Add 2nd item. | Badge on bag icon updates: 0 -> 1 -> 2. | Medium |
| **TC_12** | UI/UX | Installment Text Visibility | Item in cart | 1. Verify text below subtotal. | Display shows correct installment calc (e.g., "OR UP TO 9 x $ [value]"). | Low |
| **TC_13** | Persistence | Cart Retention on Refresh | Items in cart | 1. Refresh the browser page (F5). | Cart contents persist; Qty and Total remain unchanged. | Medium |
| **TC_14** | Persistence | Cart Retention on New Tab | Items in cart | 1. Open `bstackdemo.com` in new tab. | Cart mirrors the state of the first tab (Session Storage/Local Storage check). | Medium |
| **TC_15** | Checkout | Checkout Button State | Items in cart | 1. Check 'CHECKOUT' button. | Button is clickable/enabled; Contrast is distinct. | High |
| **TC_16** | Checkout | Empty Cart Checkout | Cart empty | 1. Check 'CHECKOUT' button or Cart Footer. | Checkout button hidden or disabled; "Add some products in the bag" msg shown. | Medium |
| **TC_17** | Filtering | Add to Cart after Filtering | Filter by 'Samsung' | 1. Click 'Samsung' filter. <br> 2. Add 'Galaxy S20'. | Correct item (S20) added, not a hidden Apple product. | Medium |
| **TC_18** | Ordering | Add to Cart after Sorting | Sort 'Lowest to Highest' | 1. Sort products. <br> 2. Add first item (Lowest price). | Correct item details (Price/Name) added to cart. | Medium |
| **TC_19** | Boundary | Minimum Quantity Handling | Item Qty = 1 | 1. Click '-' button in cart. | Verify behavior: Item removed OR button disabled (Usually removal is distinct check). | Medium |
| **TC_20** | Boundary | Maximum Quantity Check | Item in cart | 1. Click '+' 50 times (or edit input if available). | Verify if limit exists (e.g. 99) or allows infinite (within reason). | Low |
| **TC_21** | UI/UX | Close Cart via Overlay | Cart open | 1. Click grey overlay outside panel. | Cart panel closes. | Low |
| **TC_22** | Responsive | Cart View on Mobile (Simulation) | DevTools -> Dimensions: iPhone 12 | 1. Add item to cart. | Cart panel fits screen; 'Checkout' button visible/accessible. | Medium |
| **TC_23** | Data Integrity | Product Image Mismatch | Homepage | 1. Note 'iPhone 12' image. <br> 2. Add to cart. | Image in cart thumbnail matches homepage image exactly. | Low |
| **TC_24** | Integration | Add to cart then Login | Guest user with items | 1. Add items. <br> 2. Click 'Sign In'. <br> 3. Log in. | Verify if cart items persist after login (Merge cart strategy). | High |
| **TC_25** | API | Verify Add to Cart Network Request | Network Tab Open | 1. Add item. | Verify POST/PUT request to API; Status 200/201; Payload correct. | Medium |
| **TC_26** | Functional | Cross-Vendor Addition | Cart has Apple item | 1. Filter 'Google'. <br> 2. Add 'Pixel 5'. | Cart contains both Apple and Google items correctly. | Medium |
| **TC_27** | UI/UX | Long Product Name | (Hypothetical) | 1. Add product with longest name. | Name wraps correctly in cart; No text overflow/overlap. | Low |
| **TC_28** | Functional | Rapid Removal | 2 items in cart | 1. Click 'X' on Item 1 then Item 2 instantly. | Both items removed cleanly; No JS errors/orphaned rows. | Medium |
| **TC_29** | Localization | Currency Symbol Check | (If currency toggle exists) | 1. Change to EUR (if avail). <br> 2. Add item. | Cart displays prices in €. | Low |
| **TC_30** | Accessibility | Keyboard Navigation | Focus on Product Grid | 1. Tab to 'Add to cart'. <br> 2. Press Enter. | Item added; Focus management (Screen reader announcement). | Low |

---
*Created by Naveen Ravichandran - AI Testing Workspace*
