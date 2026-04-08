Zomato Food Delivery Analytics (SQL Project)
Project Overview

This project analyzes a Zomato food delivery dataset using SQL to generate business insights related to customer behavior, restaurant performance, and delivery efficiency. The analysis focuses on transforming raw transactional data into actionable insights that can support data-driven decision-making.

Objectives
Analyze customer ordering patterns and spending behavior
Identify top-performing restaurants and popular cuisines
Evaluate delivery performance across different locations
Understand revenue trends and peak order periods
Tools and Technologies
SQL (MySQL / PostgreSQL)
Relational Database Management System
CSV Dataset
Dataset Description

The dataset consists of multiple tables capturing different aspects of the food delivery process:

Customers: Customer details and identifiers
Orders: Order-level transaction data
Restaurants: Restaurant information and cuisine types
Order Items: Item-level details for each order
Delivery: Delivery time and status information
Key Business Questions
Customer Analysis
Who are the top customers based on total order value?
What is the average order value per customer?
Restaurant Analysis
Which restaurants generate the highest revenue?
Which cuisines are most frequently ordered?
Delivery Performance
What is the average delivery time?
Which locations have the fastest and slowest deliveries?
Revenue Insights
What is the total revenue generated?
How does revenue vary over time?
What are the peak ordering hours?
Database Schema

The project uses the following core tables:

customers
orders
Sample Queries

Top 5 Restaurants by Revenue
SELECT r.restaurant_name, SUM(o.order_amount) AS revenue
FROM orders o
JOIN restaurants r ON o.restaurant_id = r.restaurant_id
GROUP BY r.restaurant_name
ORDER BY revenue DESC
LIMIT 5;
Average Delivery Time
SELECT AVG(delivery_time) AS avg_delivery_time
FROM delivery;
Most Popular Cuisine
SELECT r.cuisine, COUNT(*) AS total_orders
FROM restaurants r
JOIN orders o ON r.restaurant_id = o.restaurant_id
GROUP BY r.cuisine
ORDER BY total_orders DESC;
Key Insights
A small set of restaurants contributes a significant portion of total revenue
Customer demand peaks during evening hours
Certain cuisines consistently dominate order volumes
Delivery time plays a critical role in customer satisfaction
Conclusion

This project demonstrates the application of SQL for analyzing real-world business data. It highlights how structured querying can uncover patterns, improve operational efficiency, and support strategic decision-making in the food delivery industry.
restaurants
order_items
delivery
