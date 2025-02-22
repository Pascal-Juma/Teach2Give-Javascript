 # Polymorphism

### Polymorphism allows variable or a method to have more than one form.

### It is achieved through:

- ### Method overriding: *child class provides its own implementation of a method that it has inherited*

- ### Method overloading: *feature that allows multiple methods in the same class to have the same name but different parameters.*

### Example of method overriding:
```js
class Math {
    add(number1, number2){
        return number1 + number2;
    }
}

class Arithmetics extends Math {
    add(number1, number2){
        if(number1 < 0){
            console.log("Can only add positivenumbers");
        }else if(number2 < 0){
            console.log("Can only add positivenumbers");
        }else{
            console.log("number1 + number2");
        }
    }
}

const arithmetic = new Arithmetics();
arithmetic.add(-5, 5);
arithmetic.add(5, -5);
arithmetic.add(5, 5);
```