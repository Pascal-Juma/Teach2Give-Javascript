# Encapsulation

### It is bundling data and methods into a single unit while restricting access to details of the object.

- ###  Can be achieved using *private properties*(with the `#` syntax) and *getters/setter*methods.
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
}

const account = new BankAccount("John");
account.deposit(500);
account.checkBalance();
// console.log(account.#balance); 
//Error: Private field '#balance' must be declared
```
### In the example above:

- ### `#balance` is private, it cannot be accessed outside the class.

- ### `deposit()` and `checkBalance()` methods provide controlled access to modify `#balance`.

- ### `checkBalance()` safely retrieves the balance without exposing direct access.
