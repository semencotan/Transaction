# Transaction
class BankAccount:
    def __init__(self, account_holder, balance=0):
        self.account_holder = account_holder
        self.balance = balance

    def deposit(self, amount):
        if amount > 0:
            self.balance += amount
            print(f'Deposit successful. New balance: ${self.balance}')
        else:
            print('Invalid deposit amount.')

    def withdraw(self, amount):
        if 0 < amount <= self.balance:
            self.balance -= amount
            print(f'Withdrawal successful. New balance: ${self.balance}')
        else:
            print('Invalid withdrawal amount or insufficient funds.')

    def get_balance(self):
        print(f'Current balance for {self.account_holder}: ${self.balance}')

# Example usage
account_holder_name = "John Doe"
account = BankAccount(account_holder_name)

account.get_balance()
account.deposit(1000)
account.withdraw(500)
account.get_balance()
