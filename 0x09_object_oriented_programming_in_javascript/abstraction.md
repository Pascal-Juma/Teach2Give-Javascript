# Abstraction
 ### Abstraction is hiding implementation details and exposing only the relevant parts to the user.

- ### It also makes interactions with objects simpler while keeping the internal logic hidden.
### For Example: 
```js
class BankAccount{
    #balance = 0;

    constructor(owner){
        this.owner = owner;
    }

    deposit(amount){
        this.#balance += amount;
        console.log(`Deposited ${amount}. New balance: ${this.#balance}`);
    }

    checkBalance(){
        console.log(`Current balance is: ${this.#balance}`);
    }

    withdraw(amount){
        if(amount > this.#balance){
            console.log(`Please enter an amount that matches your balance`);
        }else{
            this.#balance -= amount;
            console.log(`Successful withdrawal of ${amount}. New balance: ${this.#balance}`,
            );
        }
    }
}

const account = new BankAccount("John");account.deposit(500);
account.withdraw(900); // Please enter an amount that matches your balance
account.withdraw(200); // Successful withdrawal of 200. New balance: 300
```
- ### In this case, the user only interacts with `withdraw()` without having to know how calculations are done internally.