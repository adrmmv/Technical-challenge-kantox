## Test Case: Rules applied

The following testcases have the assumption that special rules are applied, it affects the item not all the items on the
cart.

**Scenario 1: The rule does not apply if its condition is not fulfilled**\
***Given*** the following rules are applied:\
"Buy more than 10 Strawberries, pay 50% of the original price"\
***When*** the following items are added to the cart\

| Products     | Quantity |
|--------------|----------|
| Strawberries | 10       |

***Then*** the cart total price is "£50.00"

**Scenario 2: The rule does not apply if its condition is fulfilled**\
***Given*** the following rules are applied:\
"Buy more than 10 Strawberries, pay 50% of the original price"\
***When*** the following items are added to the cart\

| Products     | Quantity |
|--------------|----------|
| Strawberries | 11       |

***Then*** the cart total price is "£27.5"

**Scenario 3: The rule does not apply if its condition is fulfilled**\
***Given*** the following rules are applied:\
"Buy more than 10 Strawberries, pay 50% of the original price"\
***When*** the following items are added to the cart\

| Products     | Quantity |
|--------------|----------|
| Strawberries | 50       |

***Then*** the cart total price is "£125.00"

