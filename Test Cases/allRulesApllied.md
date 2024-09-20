## Test Case: Rules applied

The following testcases have the assumption that special rules are applied, it affects the item not all the items on the
cart and when the items are purchased there is a summary of the purchase

**Scenario 1: All rules are applied if the cart fulfill the conditions**\
***Given*** the following rules are applied:\
"Buy three Green tea get two free"\
"Buy more than 10 Coffe, pay £1.00 per coffe"\
"Buy more than 10 Strawberries, pay 50% of the original price"\
***When*** the following items are added to the cart\

| Products     | Quantity |
|--------------|----------|
| Coffe        | 20       |
| Green tea    | 5        |
| Strawberries | 11       |

***And*** the user proceed to buy the items\
***Then*** the payment is received\
***And*** the ticket has the following information:

| Products     | Quantity | Price per unit | Original price | Discounted price | Total price |
|--------------|----------|----------------|----------------|------------------|-------------|
| Coffee       | 20       | £11.23         | £224.60        | £204.60          | £20.00      |
| Green Tea    | 5        | £3.11          | £15.55         | £3.11            | £6.22       |
| Strawberries | 11       | £5.00          | £55.00         | £27.50           | £27.50      |

***And*** the ticket has price total of"£53.72"

