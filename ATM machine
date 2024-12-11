class ATM:
    def __init__(self):
        self.balance = 10000  # Default starting balance
        self.pin = "1234"     # Default PIN

    def verify_pin(self):
        """Verify user PIN."""
        attempts = 3
        while attempts > 0:
            entered_pin = input("Enter your PIN: ")
            if entered_pin == self.pin:
                print("PIN verified successfully!")
                return True
            else:
                attempts -= 1
                print(f"Incorrect PIN. Attempts left: {attempts}")
        print("Too many incorrect attempts. Exiting...")
        return False

    def check_balance(self):
        """Check account balance."""
        print(f"Your current balance is ₹{self.balance}")

    def deposit(self):
        """Deposit money into the account."""
        try:
            amount = float(input("Enter the amount to deposit: ₹"))
            if amount <= 0:
                print("Please enter a valid amount greater than zero.")
            else:
                self.balance += amount
                print(f"₹{amount} deposited successfully. New balance: ₹{self.balance}")
        except ValueError:
            print("Invalid input. Please enter a numeric value.")

    def withdraw(self):
        """Withdraw money from the account."""
        try:
            amount = float(input("Enter the amount to withdraw: ₹"))
            if amount <= 0:
                print("Please enter a valid amount greater than zero.")
            elif amount > self.balance:
                print("Insufficient balance.")
            else:
                self.balance -= amount
                print(f"₹{amount} withdrawn successfully. Remaining balance: ₹{self.balance}")
        except ValueError:
            print("Invalid input. Please enter a numeric value.")

    def start(self):
        """Start the ATM interface."""
        if not self.verify_pin():
            return
        while True:
            print("\nATM Main Menu:")
            print("1. Check Balance")
            print("2. Deposit Money")
            print("3. Withdraw Money")
            print("4. Exit")
            choice = input("Select an option (1-4): ")
            if choice == "1":
                self.check_balance()
            elif choice == "2":
                self.deposit()
            elif choice == "3":
                self.withdraw()
            elif choice == "4":
                print("Thank you for using the ATM. Goodbye!")
                break
            else:
                print("Invalid option. Please select a valid menu option.")

# Run the ATM interface
if __name__ == "__main__":
    atm = ATM()
    atm.start()
