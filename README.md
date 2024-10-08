# Fufu_republic_repo
# Case Study: Fufu Republic
Overview:
Fufu Republic is a popular restaurant chain in Nigeria with multiple outlets nationwide. While the
core menu is standardized, some items vary by location (e.g., the Agege branch may sell
Chinese Rice, while the Lekki branch might not). Customers can order online through the
website or visit outlets for dine-in or take-out.
Payment Methods:
The restaurant accepts:
● Cash
● Debit card payments via Nomba POS terminals at outlets
● Online payments processed through gateways like Nomba Web Checkout, Paystack,
Interswitch etc.
Challenges:
1. Inventory Management:
Variations in customer demand and menu items across branches make it challenging to
maintain optimal stock levels.
2. Customer Experience:
The restaurant aims to improve the customer experience by offering personalized
promotions based on purchasing behavior.
Objective:
Fufu Republic wants to leverage data to:
● Understand sales trends across locations, payment methods, and dining options
(dine-in, take-out, online).
● Manage stock levels efficiently, reducing waste and ensuring availability.
● Enhance customer experience by analyzing purchasing habits and tailoring promotions
accordingly.

As a recently hired data engineer at Fufu Republic, you have been tasked with developing a
dimensional model to address the business's needs for data-driven decision-making.
1. Map out the necessary entities ,relationships and constraints: This should be a
model (Any degree of abstraction is okay)
2. Create a dimensional model:
○ Identify a business process of your choice
○ List the business question under the business process you selected
○ Identify the grain, dimensions and fact.

# Case Study Answers 

1.

 **Entities**
- Customer
- Order
- Branch
- Payments
- Items 
- Promotion
- Stock

 **Relationships**
- Customer places Order.
- Order contains Item(s).
- Order is made through a Branch.
- Payment is linked to an Order.
- Stock is related to Branch and Item.
- Promotion is related to customer

Constraints can be found in the ERD Diagram

2. 
a. Business Process
The Business process of understanding sales trends across locations, payment methods, and dining options(dine-in, take-out, online).

b. Business Questions 
- What are the total sales by payment method and dining option (dine-in, take-out, online) for each branch?

- Which menu items are the most popular at each branch for different dining options?

- When are the busiest hours for sales, and how do these peak times affect stock at each branch?

- How can we improve stock management by looking at previous sales trends?

c. 
- The grain is the indiidual order at a branch
- The Dimension table is Customer, Branch, Payment, Items, Promotion,Stock
- Fact table can be a sales table with 
  - order_id 
  - customer_id 
  - branch_id 
  - payment_method_id 
  - dining_option_id 
  - promotion_id
  - item_id 
