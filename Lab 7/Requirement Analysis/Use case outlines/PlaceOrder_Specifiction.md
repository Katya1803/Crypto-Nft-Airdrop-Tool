# Specifications for "Place Order" Use Case

## Name: Place Order

## Brief Description:
After selecting items to buy and adding them to the cart, the customer requests to place an order with delivery details. Payment must be completed before the items are delivered.

## Actors:
- Customer

## Flow of Events:

### Preconditions:
- The customer's cart has items.
- The customer is viewing the cart.

### Basic Flow of Use Case:
1. Customer chooses to place an order.
2. AIMS checks and notifies if the inventory has enough items for the order.
3. Customer updates the cart based on current item quantities.
4. Customer requests to place the order again.
5. AIMS displays a form for delivery information and instructions.
6. Customer fills in the delivery information and instructions and submits.
7. AIMS validates the customer's input.
8. AIMS calculates fees.
9. AIMS displays the invoice with details and total amount to pay.
10. Customer confirms the invoice.
11. AIMS saves the invoice.
12. AIMS records payment details and sets the order to a pending state.
13. AIMS displays payment details to the customer.
14. AIMS sends an email of invoice transaction information to the customer.

### Alternative Flow of Use Case:
- At any time between steps 1 and 13, the customer can choose to cancel placing the order:
  - AIMS saves the current state of the cart.
  - AIMS clears all received information.
- At any time after step 13, the customer can choose to cancel placing the order:
  - AIMS displays a notification about the cancel order decision.
  - Customer confirms the cancellation.
  - AIMS calls the "REFUND" use case.
- At step 6:
  - Customer chooses to place a rush order.
  - AIMS calls the "PLACE RUSH ORDER" use case.
- At step 7:
  - Customer leaves a blank field.
  - AIMS notifies about the blank field, waiting for fulfillment.

