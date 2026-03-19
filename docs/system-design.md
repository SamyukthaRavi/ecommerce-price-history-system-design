# System Design

## Overview

This system enables price tracking, storage, and visualization of historical pricing data for e-commerce products.

---

## Key Components

### Client Application
Displays product page and price insights.

### API Gateway
Handles incoming requests.

### Backend Service
Coordinates data fetching and response.

### Subscription Service
Checks if user is eligible.

### Price Tracking Service
Captures price changes periodically.

### Price History Database
Stores historical price data.

### Analytics Service
Generates price trends and summaries.

---

## Data Flow

1. Price updates are captured periodically.
2. Data is stored in database.
3. User requests product page.
4. System checks sale event + subscription.
5. Fetch price history.
6. Generate summary.
7. Display to user.

---

## Storage Consideration

Use a **time-series database** for efficient storage and querying.
