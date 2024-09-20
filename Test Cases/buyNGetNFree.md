## Test Case: Rules applied

The following testcases have the assumption that special rules are applied, it affects the item not all the items on the cart.

**Scenario 1: The rule does not apply if its condition is not fulfilled**\
***Given*** the following rules are applied:\
"Buy one Coffe get one free"\
***When*** the following items are added to the cart\

| Products | Quantity |
|----------|----------|
| Coffe    | 1        |

***Then*** the cart total price is "£11.23"

**Scenario 2: The rule is applied when the rule is fulfilled**\
***Given*** the following rules are applied:\
"Buy one Coffe get one free"\
***When*** the following items are added to the cart\

| Products | Quantity |
|----------|----------|
| Coffe    | 2        |

***Then*** the cart total price is "£11.23"

**Scenario 3: The rule only applies to the expected amount of items**\
***Given*** the following rules are applied:\
"Buy one Coffe get one free"\
***When*** the following items are added to the cart\

| Products | Quantity |
|----------|----------|
| Coffe    | 3        |

***Then*** the cart total price is "£22.46"

**Scenario 4: The rule applies multiple times if it matches the condition more than one time**\
***Given*** the following rules are applied:\
"Buy one Coffe get one free"\
***When*** the following items are added to the cart\

| Products | Quantity |
|----------|----------|
| Coffe    | 4        |

***Then*** the cart total price is "£22.46"

**Scenario 5: The rule is applied to the next N items added**\
***Given*** the following rules are applied:\
"Buy two Coffe get four free"\
***When*** the following items are added to the cart\

| Products | Quantity |
|----------|----------|
| Coffe    | 4        |

***Then*** the cart total price is "£22.46"

**Scenario 6: The rule does not apply if its condition is not fulfilled**\
***Given*** the following rules are applied:\
"Buy one Coffe get one free"\
***When*** the following items are added to the cart\

| Products     | Quantity |
|--------------|----------|
| Strawberries | 2        |

***Then*** the cart total price is "£10.00"
