
# Java Basics

This file summarizes the basic concepts of Java using a simple example.

## 🔹 Java Program Structure

```java
public class Test {
    int a = 10;

    public static void main(String[] args) {
        // System.out.println(args[0]);
        System.out.println(Integer.toString(a));

        for (int i = 1; i < 10; i++) {
            System.out.println(i);
        }
    }

    public static void main2(String[] args) {
        System.out.println("Hello, World!");
    }
}
````

### 🧠 How does Java know what to run?

* The `main` function is the **entry point** of a Java program.
* It **must be static** so the Java Virtual Machine (JVM) can call it **without creating an object** of the class.

### 🔑 Keywords Explained

* `public`: Access modifier — allows access from outside the class.
* `static`: Allows the method to be called without an instance of the class.
* `void`: The method doesn't return any value.
* `String[] args`: Command-line arguments passed to the program.

---

## 🧠 Memory Management in Java

Java divides memory into **stack** and **heap**:

### Stack Memory

* Used for **static memory allocation** and function calls.
* Follows **Last In, First Out (LIFO)**.
* Local variables and method calls are stored here.
* Each thread has its **own stack memory**.

### Heap Memory

* Used for **dynamic memory allocation**.
* Objects like `new Car()` are stored in heap memory.
* Heap is **shared among all threads**.
* Memory is **not automatically cleared** — this is where **Garbage Collection** comes in.

---

## 💡 Garbage Collection

* Java automatically frees heap memory that is no longer referenced.
* This process is known as **Garbage Collection**.
* Developers **do not manually deallocate memory**, unlike in C/C++.

---

## 🧱 Wrapper Classes

Java provides **wrapper classes** to use primitive types as objects:

| Primitive | Wrapper Class |
| --------- | ------------- |
| `int`     | `Integer`     |
| `long`    | `Long`        |
| `char`    | `Character`   |
| `boolean` | `Boolean`     |
| `float`   | `Float`       |
| `double`  | `Double`      |

### Why use wrapper classes?

* Allow primitives to be used where objects are required (e.g., collections).
* Provide **utility methods** like `Integer.toString()`, `parseInt()`, etc.

---

## 📝 Notes

* `Integer.toString(a)` doesn't require object creation because `Integer` is a class with **static methods**.
* Earlier, we had to create wrapper class objects using `new Integer(10)`, but that’s **not required** anymore due to **autoboxing**.

---

### ✅ Summary

* Java programs start from the `main()` method.
* `static` enables methods to be used without an object.
* Memory is managed through **stack** and **heap**.
* Java supports **automatic garbage collection**.
* Wrapper classes bridge primitives and objects.
