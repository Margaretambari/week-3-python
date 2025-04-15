Create a function named calculate_discount(price, discount_percent) that calculates the final price after applying a discount. The function should take the original price (price) and the discount percentage (discount_percent) as parameters. If the discount is 20% or higher, apply the discount; otherwise, return the original price.

def calculate_discount(price, discount_percent):

    # Check if the discount percentage is 20% or higher
    
    if discount_percent >= 20:
    
        # Calculate the discount amount
        
        discount_amount = price * (discount_percent / 100)
        
        # Calculate the final price after discount
        
        final_price = price - discount_amount
        
        return final_price
        
    else:
    
        # If the discount is less than 20%, return the original price
        
        return price

# Example usage:
original_price = 100

discount_percent = 25

final_price = calculate_discount(original_price, discount_percent)

print(f"The final price after applying the discount is: ${final_price:.2f}")

Using the calculate_discount function, prompt the user to enter the original price of an item and the discount percentage. Print the final price after applying the discount, or if no discount was applied, print the original price.

def calculate_discount(price, discount_percent):
    # Check if the discount percentage is 20% or higher
    if discount_percent >= 20:
        # Calculate the discount amount
        discount_amount = price * (discount_percent / 100)
        # Calculate the final price after discount
        final_price = price - discount_amount
        return final_price
    else:
        # If the discount is less than 20%, return the original price
        return price

# Prompt the user for input
try:
    original_price = float(input("Enter the original price of the item: $"))
    discount_percent = float(input("Enter the discount percentage: "))
    
    # Calculate the final price using the calculate_discount function
    final_price = calculate_discount(original_price, discount_percent)
    
    # Print the final price
    if final_price < original_price:
        print(f"Final price after applying the discount: ${final_price:.2f}")
    else:
        print(f"No discount applied, original price: ${original_price:.2f}")
except ValueError:
    print("Please enter valid numerical values for price and discount percentage.")
