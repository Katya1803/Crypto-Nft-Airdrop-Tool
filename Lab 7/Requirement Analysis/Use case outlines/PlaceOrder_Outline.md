# Outline for "Place Order" Use Case of AIMS Project

## Steps for Placing an Order:
1. **Order Placement**
   - Customer views the cart.
   - Customer requests to place the order.
   - AIMS software checks inventory availability.
   - Customer updates the cart if necessary.
   - Customer requests to place the order again.
2. **Order Payment**
   - Customer updates delivery information and instructions.
   - AIMS software validates the input.

## Description:
A customer initiates the order placement process after selecting items for purchase. The process involves requesting to place the order and completing the payment before the goods are delivered.

## Actors:
- Customers

## Flow of Events:

### Basic Flow:
1. **Order Placement:**
   - Customer views the contents of the cart.
   - Customer decides to proceed with placing the order.
   - AIMS software verifies inventory availability.
   - Customer adjusts the cart if necessary based on availability.
   - Customer submits the order request.
2. **Order Payment:**
   - Customer updates delivery information and any specific instructions.
   - AIMS software validates the provided details.

### Alternative Flow:
- **Exception Handling:**
   - If there's invalid input for delivery information:
     - AIMS software prompts the customer to correct the information.
     - Customer updates the information.
   - If the delivery address is not supported:
     - AIMS software notifies the customer.
     - Customer updates the delivery address.
- **Alternative Scenario:**
   - Customer opts for rush order:
     - AIMS software checks item availability for rush delivery.
     - Eligible items for rush delivery are combined.
     - AIMS software schedules rush order delivery.

This outline covers the steps for placing an order, including order placement and payment, along with handling exceptions and alternative scenarios in the process.
