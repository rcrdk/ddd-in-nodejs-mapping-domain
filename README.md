# 🔎 Mapping a Domain Challenge
I developed this project during my latest studies on Node lessons with DDD at [Rocketseat](https://www.rocketseat.com.br).

## 🖥️ Project
In this challenge I had to read a conversation between and Domain Expert and the Developer of application. The objective is to identify all entities and use cases fo this application based on below conversation:

- 🧑🏼‍💻 **Dev:** Hey, thanks for the meeting. To begin with, which are the main functionalities would you like to this stock management system should have?
- 🧙🏻‍♂️ **Domain Expert:** We need a solution that allow us to track each product individually, set min stock quantities and receive reminders when some product has low quantities in stock. Also, it would be useful if we could check on sales and stock history to make future purchasing decisions.
- 🧑🏼‍💻 **Dev:** Got it. Could you give me an example on how would you like to the individual product tracking would work?
- 🧙🏻‍♂️ **Domain Expert:** We would like to set a unique identification number to each product, sou we could easily track it movements in our stock. It would be useful, also, to add extra informations such as size and color to make the tracking even mor precise.
- 🧑🏼‍💻 **Dev:** And about the min stock quantities functionality, how do you imagine this working?
- 🧙🏻‍♂️ **Domain Expert:** We would like to set a min limit to each product, in a way that we could receive a reminder when the stock is near the end. That would help us to ensure that we never would be without any popular product and also allow us to make efficient orders.
- 🧑🏼‍💻 **Dev:** And how would you like to receive this reminders? By e-mail, SMS or other method?
- 🧙🏻‍♂️ **Domain Expert:** It would be great if if we could receive reminders by e-mail and also by a notification in our stock management system.
- 🧑🏼‍💻 **Dev:** Got it. And about the functionality of sales and stock history, which kind of informations would you like to see?
- 🧙🏻‍♂️ **Domain Expert:** We would like to see how many products we sale in a certain period, what was the profit that each product brought and which products we sale the most on each period. Also, it would be useful if we could watch for trends in stock along the time, to help us to make proper buying decisions. 
- 🧑🏼‍💻 **Dev:** Ok, and do you have any other functionality that would you like to see on th system?
- 🧙🏻‍♂️ **Domain Expert:** It would be very useful if the system could allow us to create and manage buying orders automatically, based on min quantities in stock defined and on sales trends. It would be great, also, if we could integrate our system with our suppliers, so we could receive automatic updates on delivery time of our new shipments.

## 😶‍🌫️ What do I had to look for?
Based on the conversation, I should have answer this questions:

1) Which are the domain entities?
2) Which actions (use cases) this application should have?

## 🚀 Techs and Tools
- [Node.js v18](https://nodejs.org/)
- [Vitest](https://vitest.dev/)

## ⚙️ Get started
```zsh
npm i
npm run test
```