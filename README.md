#Lists
fish_list = []
weight_list = []

#Fish numbers
def get_number(prompt):
    while True:
        try:
            value = input(prompt).strip()
            number = float(value)
            return number
        except ValueError:
            print("Not a number. Please enter a real number.")

fish_name1 = input("Enter the name of the Fish1:")
A = get_number(input(f"Enter the length in inches for {fish_name1}: "))
B = get_number(input(f"Enter the girth in inches for {fish_name1}: "))



fish_name2 = input("Enter the name of the Fish2:")
C = float(input(f"Enter the length in inches for {fish_name2}: "))
D = float(input(f"Enter the girth in inches for {fish_name2}: "))


#Weight
Weight = B*B*A/800
Weight = round(Weight, 2)

Weight2 = D*D*C/800
Weight2 = round(Weight2, 2)

#Back to lists
if 0 <= Weight <= 41:
    print("Small Fish")
elif 42 <= Weight2 <= 99:
     print("Medium Fish")
elif 100 <= Weight2 <= 174:
    print("Big Fish")
else:
    print("Giant Fish")
    

if 0 <= Weight2 <= 41:
    print("Small Fish")
elif 42 <= Weight2 <= 99:
     print("Medium Fish")
elif 100 <= Weight2 <= 174:
    print("Big Fish")
else:
    print("Giant Fish")
    
fish_list.append(fish_name1)
weight_list.append(Weight)

fish_list.append(fish_name2)
weight_list.append(Weight2)

print(f"The weight of {fish_name1} is {Weight} pounds.\n")
print(f"The weight of {fish_name2} is {Weight2} pounds.\n")
