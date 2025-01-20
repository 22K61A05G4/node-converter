def rupees_to_dollars(rupees):
    conversion_rate = 0.012  # 1 INR = 0.012 USD (current exchange rate may vary)
    dollars = rupees * conversion_rate
    return dollars

def dollars_to_rupees(dollars):
    conversion_rate = 83.33  # 1 USD = 83.33 INR (current exchange rate may vary)
    rupees = dollars * conversion_rate
    return rupees

def main():
    print("Currency Converter")
    
    while True:
        print("\nSelect an option:")
        print("1. Convert Rupees to Dollars")
        print("2. Convert Dollars to Rupees")
        print("3. Exit")
        
        choice = input("Enter your choice (1/2/3): ")
        
        if choice == "1":
            try:
                rupees = float(input("Enter amount in Rupees: "))
                dollars = rupees_to_dollars(rupees)
                print(f"{rupees} Rupees is equal to {dollars:.2f} Dollars.")
            except ValueError:
                print("Please enter a valid number.")
        
        elif choice == "2":
            try:
                dollars = float(input("Enter amount in Dollars: "))
                rupees = dollars_to_rupees(dollars)
                print(f"{dollars} Dollars is equal to {rupees:.2f} Rupees.")
            except ValueError:
                print("Please enter a valid number.")
        
        elif choice == "3":
            print("Exiting the program. Goodbye!")
            break
        
        else:
            print("Invalid choice. Please select 1, 2, or 3.")

if __name__ == "__main__":
    main()
