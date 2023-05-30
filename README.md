def calculate_simple_interest(principal, time, gender, senior_citizen):
    if gender == 'female' and senior_citizen:
        rate = 8
    elif gender == 'female' and not senior_citizen:
        rate = 6
    elif gender == 'male' and senior_citizen:
        rate = 7
    elif gender == 'male' and not senior_citizen:
        rate = 5
    else:
        print("Invalid gender or senior citizen status")
        return
    
    interest = (principal * rate * time) / 100
    return interest

# Example usage
principal_amount = 100000
time_period = 5
customer_gender = 'female'
is_senior_citizen = True

interest_amount = calculate_simple_interest(principal_amount, time_period, customer_gender, is_senior_citizen)
print("Simple Interest Amount:", interest_amount)
