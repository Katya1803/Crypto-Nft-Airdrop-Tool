

**Use Case: Customer Order Placement**

**Actor:** Customer

**Precondition:** The Customer has already selected items to purchase and added them to the shopping cart.

**Main Flow:**

1. **Customer:** Reviews the contents of the shopping cart and chooses items for purchase.
2. **Customer:** Initiates the order process.
3. **System:**
    - Checks the availability of each item in the inventory.
    - Continues if all items are available.
4. **System:** Prompts the Customer to input delivery information.
5. **Customer:** Enters or updates delivery details, including recipient name, contact information, and address.
6. **System:**
    - Calculates the delivery fee based on factors such as weight and destination.
    - Generates a temporary invoice displaying selected items, quantities, prices, subtotal (with and without VAT), delivery fee, and total amount payable.
7. **Customer:** Reviews and confirms the invoice details.
8. **Customer:** Chooses rush order delivery, if desired.
9. **Customer:** Adjusts delivery method or modifies the items in the order if necessary.
10. **System:** Recalculates fees and updates the invoice accordingly.
11. **Customer:** Selects a payment method supported by VNPay.
12. **System:** Processes payment via VNPay.
13. **System:**
    - Upon successful payment:
        - Presents transaction details such as ID, amount, and timestamp.
        - Sends order and payment confirmation to the Customer via email.
        - Updates the order status to "pending processing."
        - Logs transaction and order information.
14. **Customer:** (Optional) Can review or cancel the order using the provided link in the email.

**Alternate Flows:**

1. **Insufficient Inventory:**
- **Trigger:** Detected during inventory check in step 3.
- **Action:**
    - System alerts the Customer about items with insufficient stock.
    - Customer may adjust the cart contents or cancel the order.
2. **Rush Order Processing:**
- **Trigger:** Customer selects rush delivery in step 8.
- **Action:**
    - System checks eligibility for rush delivery and requests additional details if necessary.
    - Customer makes adjustments as needed.
    - System recalculates fees accordingly.
3. **Customer Abandons Order Process:** Customer exits at any step.
4. **Payment Failure:** System notifies the Customer and offers options for retrying payment or cancelling the order.
5. **Invalid Delivery Information:**
- **Trigger:** Detected during delivery information input.
    - System flags invalid information and prompts the Customer for correction.
    - Customer corrects the errors, and the process resumes.

**Postcondition:**

- **Successful Order:** Customer receives confirmation email, and the order status is set to "pending processing."
- **Cancelled Order:** Customer receives cancellation confirmation email, and a full refund is processed.
