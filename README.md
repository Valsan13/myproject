# myproject
from random import randint


def get_random_index(items):
    return randint(0, len(items) - 1)  #len items takes the 3 list items and minus one, bcz index start from 0
pizza_types = ["margherita", "napoletana", "marinara", "pepperoni"]
pizza_prices = [6.0, 7.0, 7.5, 8.0]
extra_types = ["mushrooms", "cheese", "anchovies", "sausage", "pineapple"]
extra_prices = [0.5, 1.0, 1.5, 1.8, 1.6]

random = get_random_index(pizza_types)
pizza_type = pizza_types[random]
pizza_price = pizza_prices[random]

pizza_description = pizza_type

n_random_extras = randint(1, 4)
for e in range(n_random_extras):
    random = get_random_index(extra_types)
    extra_type = extra_types[random]
    if e == 0:
        pizza_description += f" with extra {extra_type}"
    else:
        pizza_description += f", {extra_type}"
    extra_price = extra_prices[random]
    pizza_price += extra_price

print(f"You have won a {pizza_description} worth £{pizza_price:.2f}")
