### Test Case: No rules applied

The following testcases have the assumption that no special rules are applied in order to test the cashier system.

**Scenario 1: Add items to the cart displays the correct price**\
***Given*** the cart is empty\
***When*** the item "Green tea" is added to the cart\
***Then*** the cart total price is "£3.11"

**Scenario 2: The total price is updated when we add a new item**\
***Given*** the cart has the item "Green tea" and a total price of "£3.11"\
***When*** the item "Coffe" is added to the cart\
***Then*** the cart total price is "£14.34"

**Scenario 3: The total price is updated when we remove an item**\
***Given*** the cart has the following items in the cart with a total price of "£19.34":

| Products     |
|--------------|
| Green Tea    |
| Strawberries |
| Coffee       |

***When*** the item "Coffe" is removed from the cart\
***Then*** the cart total price is "£8.11"

**Scenario 4: Cart total price is zero when all items are removed**\
***Given*** the cart has the folowing items with a total price of "£61.8":

| Products     | Quantity |
|--------------|----------|
| Green Tea    | 1        |
| Strawberries | 5        |
| Coffee       | 3        |

***When*** all the items are removed from the cart
***Then*** the cart total price is "£0"

**Scenario 5: When an undifined item is added to the cart it returns a warning**\
***Given*** the cart has the folowing items with a total price of "£61.8":

| Products     | Quantity |
|--------------|----------|
| Green Tea    | 1        |
| Strawberries | 5        |
| Coffee       | 3        |

***When*** the item "Unexpected item" is added to the cart\
***Then*** a warning message is returned\
***And*** the cart total price is "£61.8"

**Scenario 5: When an undifined item is added to the cart it returns a warning**\
***Given*** the cart has the folowing items with a total price of "£61.8":

| Products     | Quantity |
|--------------|----------|
| Green Tea    | 1        |
| Strawberries | 5        |
| Coffee       | 3        |

***When*** the user proceed to buy the items\
***Then*** the payment is received\
***And*** the ticket has the following information:

| Products     | Quantity | Price per unit | Total price |
|--------------|----------|----------------|-------------|
| Green Tea    | 1        | £3.11          | £3.11       |
| Strawberries | 5        | £5.00          | £25.00      |
| Coffee       | 3        | £11.23         | £33.69      |

***And*** the ticket has price total of"£61.8"

