# Discount Calculator

price = 74.5
discount = 20.0

def apply_discount(price, discount):
    if type(price) not in [int, float]:
        return("The price should be a number")
    elif type(discount) not in [int, float]:
        return("The discount should be a number")
    elif price <= 0:
        return("The price should be greater than 0")
    elif discount < 0 or discount > 100:
        return("The discount should be between 0 and 100")
    else:
        total_price = price*(1-discount/100)
        rounded =round(total_price, 1)
        return(rounded)

apply_discount(price, discount)