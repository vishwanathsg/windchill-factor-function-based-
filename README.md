# windchill-factor-function-based-
This code tell the temperature that a living being feels due to wind

#Factor:  Calculate temperature that a person feels because of the wind
#This program tells the temperature that a person feels due to moving air

def wind(temp,vel):
    wind=13.12+0.6215*temp-11.37*vel**0.16+0.3965*temp*vel**0.16//1
    return wind
"""
Input : temp entry can be both positive and negative, but vel entry should be positive 
Returns True if a numerical value, otherwise False
"""

temp=float(input("Enter value for temperature in degree celsius: "))
#Took temperature input from the user

vel=float(input("Enter a positive velocity of wind speed (KMPH): "))
#Took velocity value from the user

if vel<0:
    print("velocity of wind is invalid, try again")
    vel = float(input("Enter a positive velocity of wind speed (KMPH): "))

result = wind(temp,vel)

print("The temperature that a person will experience due to wind in the given condition is:", result )
