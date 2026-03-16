# E-commerce Price History System Design

A system design exploration that looks at how e-commerce platforms can improve pricing transparency by providing built-in price history insights for products.

This feature focuses on improving customer trust by allowing users to understand how product prices have changed over time.

---

## Problem Statement

During major sale events on e-commerce platforms, products often show large discounts.

However, users cannot easily verify how the price has changed historically because the platform does not display price history directly.

As a result, many users rely on third-party tools or external websites to check product price history before making a purchase.

This creates a fragmented user experience and reduces trust in the platform.

Providing native price history insights directly inside the e-commerce platform can improve transparency and user confidence.

---

## Proposed Solution

Introduce a built-in **Price History Insight Feature** that allows users to view how product prices have changed over time.

To balance system performance and platform strategy, this feature will:

- Be available **only to platform subscribers**
- Be visible **during major sale events**
- Provide **price history graphs and trend summaries**

This approach improves trust while also adding value to the platform's subscription programs.

---

## Example Scenario

A user wants to buy a pair of headphones during a festive sale.

The product page shows:

Original Price: ₹5999  
Sale Price: ₹3499

If the user is a subscriber and visits during the sale event, they can see:

Price Trend (Last 90 Days)

Average Price: ₹4200  
Lowest Price: ₹3499  
Current Price: ₹3499

They can also view a simple **price history graph** showing how the price changed over time.

This helps the user make a more informed purchase decision without relying on external tools.

---

## Target Users

- Online shoppers
- Budget-conscious buyers
- Deal hunters
- E-commerce platform subscribers
- E-commerce platforms seeking to improve customer trust

---

## Functional Requirements

The system should:

1. Track historical prices of products
2. Store price changes over time
3. Display a price history graph for eligible users
4. Show price trend summaries (average price, lowest price, current price)
5. Allow users to set price drop alerts
6. Show the feature **only to subscribers**
7. Display price insights primarily **during major sale events**

---

## Non-Functional Requirements

- Scalability to track millions of products
- High availability during major sale events
- Fast loading price graphs on product pages
- Reliable historical data collection
- Efficient storage for large-scale price history data

---

## High Level Architecture

The system can include the following components:

Client Application  
Displays product pages and price history insights.

API Gateway  
Handles incoming requests from the client.

Subscription Service  
Verifies if the user is eligible to access price insights.

Price Tracking Service  
Continuously records product price changes.

Price History Database  
Stores historical price data for all products.

Analytics Service  
Processes historical price data to generate trend summaries.

---

## Data Flow

1. Product prices are periodically captured by the Price Tracking Service.
2. The price data is stored in the Price History Database.
3. When a user opens a product page during a sale event, the client sends a request to the backend.
4. The Subscription Service checks if the user is eligible for the feature.
5. If eligible, the backend fetches price history data.
6. The Analytics Service calculates trend summaries.
7. The client displays the price history graph and summary to the user.

---

## Possible Enhancements

Future improvements could include:

- AI-based price prediction
- Personalized price alerts
- Smart purchase recommendations
- Multi-platform price comparisons

---

## Author
Samyuktha Ravichandran

---

## Purpose of This Project

This repository is part of a personal learning series exploring how real-world product problems can be solved using system design and product thinking.

The goal is to analyze everyday digital product challenges and design scalable solutions that improve user experience.
