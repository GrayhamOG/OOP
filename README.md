// Abstraction and Encapsulation
abstract class Animal {
    private String name; // Encapsulation

    public Animal(String name) {
        this.name = name;
    }

    public String getName() { // Encapsulation - getter
        return name;
    }

    public abstract void sound(); // Abstraction - abstract method
}

// Inheritance and Polymorphism
class Dog extends Animal {
    public Dog(String name) {
        super(name);
    }

    @Override
    public void sound() { // Polymorphism - method override
        System.out.println(getName() + " says: Woof!");
    }
}

public class Car {
    public static void main(String[] args) {
        Animal myDog = new Dog("Buddy");
        myDog.sound(); // Polymorphism - runtime method call
    }
}
