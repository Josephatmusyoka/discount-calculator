# Discount Calculator

This repository contains a Python script that calculates the final price of an item after applying a discount. The discount is only applied if the discount percentage is 20% or higher. If the discount percentage is less than 20%, the original price is returned.

## Features

- Define a function to calculate the discount.
- Prompt the user to enter the original price and the discount percentage.
- Print the final price after applying the discount, or the original price if no discount is applied.

## Script

The script includes a function `calculate_discount` and handles user input. Below is the implementation:

```python
def calculate_discount(price, discount_percent):
    """
    Calculate the final price after applying a discount.

    :param price: Original price of the item
    :param discount_percent: Discount percentage to apply
    :return: Final price after applying the discount or original price if discount is less than 20%
    """
    if discount_percent >= 20:
        discount_amount = price * (discount_percent / 100)
        final_price = price - discount_amount
        return final_price
    else:
        return price

# Prompt user for input
try:
    original_price = float(input("Enter the original price of the item: "))
    discount_percent = float(input("Enter the discount percentage: "))

    final_price = calculate_discount(original_price, discount_percent)

    print(f"The final price after applying the discount is: ${final_price:.2f}")
except ValueError:
    print("Invalid input. Please enter numeric values.")
