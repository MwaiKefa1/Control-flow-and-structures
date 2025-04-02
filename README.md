# Control-flow-and-structures
def calculate_discount(price, discount_percent):
    """
    Calculates the final price after applying a discount if it's 20% or higher.

    :param price: Original price of the item
    :param discount_percent: Discount percentage
    :return: Final price after applying the discount (if applicable)
    """
    if discount_percent >= 20:
        discount_amount = (discount_percent / 100) * price
        return price - discount_amount
    return price  # Return original price if discount is less than 20%

# Prompt user for input
price = float(input("Enter the original price of the item: "))
discount_percent = float(input("Enter the discount percentage: "))

# Calculate the final price
final_price = calculate_discount(price, discount_percent)

# Display the result
if discount_percent >= 20:
    print(f"Final price after {discount_percent}% discount: ${final_price:.2f}")
else:
    print(f"No discount applied. Original price: ${price:.2f}")
