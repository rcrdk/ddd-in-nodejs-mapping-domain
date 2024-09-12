# 🔎 Mapping a Domain Challenge
[Jump to mapping 🖱️](#-mapping)

I worked in this analysis during my latest studies on Node lessons with DDD at [Rocketseat](https://www.rocketseat.com.br). In this challenge I had to read a conversation between and Domain Expert and the Developer of application. The objective is to identify all entities and use cases for this application based on below conversation:

- 🧑🏼‍💻 **Dev:** Hey, thanks for the meeting. To begin with, which are the main functionalities would you like to this stock management system should have?

- 🧙🏻‍♂️ **Domain Expert:** We need a solution that allow us to track each product individually, set min stock quantities and receive reminders when some product has low quantities in stock. Also, it would be useful if we could check on sales and stock history to make future purchasing decisions.

- 🧑🏼‍💻 **Dev:** Got it. Could you give me an example on how would you like to the individual product tracking would work?

- 🧙🏻‍♂️ **Domain Expert:** We would like to set a unique identification number to each product, sou we could easily track it movements in our stock. It would be useful, also, to add extra informations such as size and color to make the tracking even more precise.

- 🧑🏼‍💻 **Dev:** And about the min stock quantities functionality, how do you imagine this working?

- 🧙🏻‍♂️ **Domain Expert:** We would like to set a min limit to each product, in a way that we could receive a reminder when the stock is near the end. That would help us to ensure that we never would be without any popular product and also allow us to make efficient orders.

- 🧑🏼‍💻 **Dev:** And how would you like to receive this reminders? By e-mail, SMS or other method?

- 🧙🏻‍♂️ **Domain Expert:** It would be great if we could receive reminders by e-mail and also by a notification in our stock management system.

- 🧑🏼‍💻 **Dev:** Got it. And about the functionality of sales and stock history, which kind of informations would you like to see?

- 🧙🏻‍♂️ **Domain Expert:** We would like to see how many products we sale in a certain period, what was the profit that each product brought and which products we sale the most on each period. Also, it would be useful if we could watch for trends in stock along the time, to help us to make proper buying decisions. 

- 🧑🏼‍💻 **Dev:** Ok, and do you have any other functionality that would you like to see on the system?

- 🧙🏻‍♂️ **Domain Expert:** It would be very useful if the system could allow us to create and manage buying orders automatically, based on min quantities in stock defined and on sales trends. It would be great, also, if we could integrate our system with our suppliers, so we could receive automatic updates on delivery time of our new shipments.

## 😶‍🌫️ What do I had to look for?
Based on the conversation, I should have answer this questions:

1) Which are the domain entities?
2) Which actions (use cases) this application should have?

---

# 📋 Mapping

## Use Cases

- [ ] Should be able to define or update a min quantity of a product in stock.
- [ ] Should be able to send an automatic notification by email and in-app when a product quantity has a low quantity in stock.
- [ ] Should be able to make automatic orders to suppliers when a product has low quantity in stock.
- [ ] Should be able to send a notification to managers and suppliers when a automatic orders is made.
- [ ] Should be able to find a product by its unique identifier.
- [ ] Should be able to search for products by it's characteristics.
- [ ] Should be able to search for most sold products in a period of time.
- [ ] Should be able to get the history of how many products was sold in a period of time with the profit information included.
- [ ] Should be able to get the products trending in stock along the time.

## Entities

- **Manager:** entity who manage the app
  - id
  - name

- **Client:** entity who orders are made for
  - id
  - name

- **Supplier:** entity who supplies for the company
  - id
  - name
 
- **Product:**
  - id
  - code
  - name
  - cost price
  - selling price
  - available quantity
  - min quantity
  - allow renew stock (allows to automatically make buy order)
  - size
  - color

- **Orders:** by clients
  - id
  - client id
  - code
  - products
  - products price
  - shipment price
  - discounts
  - price total
  - status
  - created at
  - updated at

- **Order products:** 
  - id
  - product id
  - order id
  - name
  - quantity
  - cost price
  - selling price
  - subtotal price

- **Order status:**
  - id
  - order id
  - manager id
  - type
  - message
  - created_at

- **Shipments:** add products to stock from suppliers
  - id
  - supplier id
  - product id
  - status
  - created at
  - updated at
  - delivered at

- **Notification:**
  - id
  - message
  - sent at