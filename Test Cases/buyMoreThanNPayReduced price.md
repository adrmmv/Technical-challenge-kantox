## Test Case: Rules applied

The following testcases have the assumption that special rules are applied, it affects the item not all the items on the cart.

**Scenario 1: The rule does not apply if its condition is not fulfilled**\
***Given*** the following rules are applied:\
"Buy more than 10 Coffe, pay £1.00 per coffe"\
***When*** the following items are added to the cart\

| Products | Quantity |
|----------|----------|
| Coffe    | 10       |

***Then*** the cart total price is "£112.30"

**Scenario 2: The rule does not apply if its condition is fulfilled**\
***Given*** the following rules are applied:\
"Buy more than 10 Coffe, pay £1.00 per coffe"\
***When*** the following items are added to the cart\

| Products | Quantity |
|----------|----------|
| Coffe    | 11       |

***Then*** the cart total price is "£11.00"

**Scenario 3: The rule does not apply if its condition is fulfilled**\
***Given*** the following rules are applied:\
"Buy more than 10 Coffe, pay £1.00 per coffe"\
***When*** the following items are added to the cart\

| Products | Quantity |
|----------|----------|
| Coffe    | 50       |

***Then*** the cart total price is "£50.00"

