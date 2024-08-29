# Funciones-2
Codigo 2 de Funciones en Python

def calc_bmi(height, weight):

    bmi = weight / (height ** 2)
    return bmi

def calc_ideal_weight(ideal_bmi, height):

    ideal_weight = ideal_bmi * (height ** 2)
    return ideal_weight

height = float(input("Enter your height in meters: "))

weight = float(input("Enter your weight in kgs: "))

bmi = calc_bmi(height, weight)

print(f"Your body mass index is {bmi:.2f} kg/m^2")

if bmi < 18.5:
   
    print("You're thin")
    ideal_weight = calc_ideal_weight(18.5, height)
    print(f"Your ideal weight is: {ideal_weight:.2f} kg")

elif 18.5 <= bmi <= 24.9:
    
    print("You're in a normal weight range")

elif 25.0 <= bmi <= 29.9:
    
    print("You're overweight")
    ideal_weight = calc_ideal_weight(24.9, height)
    print(f"Your ideal weight is: {ideal_weight:.2f} kg")
else:
    
    print("You're obese")
    ideal_weight = calc_ideal_weight(24.9, height)
    print(f"Your ideal weight is: {ideal_weight:.2f} kg")
