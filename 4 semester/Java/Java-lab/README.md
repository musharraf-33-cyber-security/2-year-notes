1. WAP in Java to show implementation of classes.
2. WAP in Java to show implementation of inheritance.
3.  WAP in Java to show Implementation of packages and interfaces. To accomplish
4. WAP in Java to show Implementation of threads.
5. WAP in Java Using exception handling mechanisms.
6. WAP in Java to show Implementation of Applets.
7. WAP in Java to show Implementation of mouse events, and keyboard events.
8. WAP in Java to show Implementing basic file reading and writing methods.
9. Using basic networking features, WAP in Java To accomplish
10. WAP in Java to show Connecting to Database using JDBC.
Project work: A desktop based application project should be designed and implemented in java.





---

### 1. Java Program to Show Implementation of Classes


[Run](https://www.programiz.com/java-programming/online-compiler/)
```java
// Java program to demonstrate the implementation of classes

// Define a class
class Person {
    // Attributes
    String name;
    int age;

    // Constructor
    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Method to display details
    void display() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}

public class Main {
    public static void main(String[] args) {
        // Create an object of Person
        Person person1 = new Person("Alice", 30);
        person1.display();
    }
}
```

### 2. Java Program to Show Implementation of Inheritance


[Run](https://www.programiz.com/java-programming/online-compiler/)
```java
// Java program to demonstrate inheritance

// Base class
class Animal {
    void eat() {
        System.out.println("This animal eats food.");
    }
}

// Derived class
class Dog extends Animal {
    void bark() {
        System.out.println("The dog barks.");
    }
}

public class Main {
    public static void main(String[] args) {
        // Create an object of Dog
        Dog dog = new Dog();
        dog.eat(); // Method from base class
        dog.bark(); // Method from derived class
    }
}
```

### 3. Java Program to Show Implementation of Packages and Interfaces


[Run](https://www.programiz.com/java-programming/online-compiler/)
```java
// Define package
package mypackage;

// Define interface
interface Animal {
    void sound();
}

// Implement interface in class
class Cat implements Animal {
    public void sound() {
        System.out.println("The cat meows.");
    }
}

// Define another class in the same package
public class Main {
    public static void main(String[] args) {
        Cat cat = new Cat();
        cat.sound();
    }
}
```

### 4. Java Program to Show Implementation of Threads


[Run](https://www.programiz.com/java-programming/online-compiler/)
```java
// Java program to demonstrate threads

// Define a class that extends Thread
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread is running.");
    }
}

public class Main {
    public static void main(String[] args) {
        // Create and start the thread
        MyThread thread = new MyThread();
        thread.start();
    }
}
```

### 5. Java Program Using Exception Handling Mechanisms


[Run](https://www.programiz.com/java-programming/online-compiler/)
```java
// Java program to demonstrate exception handling

public class Main {
    public static void main(String[] args) {
        try {
            int[] numbers = new int[5];
            numbers[10] = 50; // This will throw ArrayIndexOutOfBoundsException
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Exception caught: " + e.getMessage());
        } finally {
            System.out.println("Finally block executed.");
        }
    }
}
```

### 6. Java Program to Show Implementation of Applets


[Run](https://www.programiz.com/java-programming/online-compiler/)
```java
// Import Applet package
import java.applet.Applet;
import java.awt.Graphics;

/* <applet code="MyApplet.class" width="300" height="300"></applet> */

public class MyApplet extends Applet {
    public void paint(Graphics g) {
        g.drawString("Hello, Applet!", 20, 20);
    }
}
```

### 7. Java Program to Show Implementation of Mouse Events and Keyboard Events


[Run](https://www.programiz.com/java-programming/online-compiler/)
```java
import java.awt.*;
import java.awt.event.*;

public class Main extends Frame implements MouseListener, KeyListener {
    public Main() {
        addMouseListener(this);
        addKeyListener(this);
        setSize(300, 300);
        setVisible(true);
    }

    public void mouseClicked(MouseEvent e) {
        System.out.println("Mouse clicked at: " + e.getX() + ", " + e.getY());
    }

    public void keyPressed(KeyEvent e) {
        System.out.println("Key pressed: " + e.getKeyChar());
    }

    public void mouseEntered(MouseEvent e) {}
    public void mouseExited(MouseEvent e) {}
    public void mousePressed(MouseEvent e) {}
    public void mouseReleased(MouseEvent e) {}
    public void keyReleased(KeyEvent e) {}
    public void keyTyped(KeyEvent e) {}

    public static void main(String[] args) {
        new Main();
    }
}
```

### 8. Java Program to Show Implementing Basic File Reading and Writing Methods


[Run](https://www.programiz.com/java-programming/online-compiler/)
```java
import java.io.*;

public class FileExample {
    public static void main(String[] args) {
        // Writing to a file
        try (BufferedWriter writer = new BufferedWriter(new FileWriter("example.txt"))) {
            writer.write("Hello, World!");
        } catch (IOException e) {
            e.printStackTrace();
        }

        // Reading from a file
        try (BufferedReader reader = new BufferedReader(new FileReader("example.txt"))) {
            String line;
            while ((line = reader.readLine()) != null) {
                System.out.println(line);
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

### 9. Java Program Using Basic Networking Features


[Run](https://www.programiz.com/java-programming/online-compiler/)
```java
import java.io.*;
import java.net.*;

public class NetworkExample {
    public static void main(String[] args) {
        try {
            // Create a socket to connect to a server
            Socket socket = new Socket("example.com", 80);

            // Send a request to the server
            PrintWriter out = new PrintWriter(socket.getOutputStream(), true);
            out.println("GET / HTTP/1.1");
            out.println("Host: example.com");
            out.println("Connection: close");
            out.println();

            // Read the response from the server
            BufferedReader in = new BufferedReader(new InputStreamReader(socket.getInputStream()));
            String responseLine;
            while ((responseLine = in.readLine()) != null) {
                System.out.println(responseLine);
            }

            // Close the connections
            in.close();
            out.close();
            socket.close();
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

### 10. Java Program to Show Connecting to Database Using JDBC


[Run](https://www.programiz.com/java-programming/online-compiler/)
```java
import java.sql.*;

public class JDBCExample {
    public static void main(String[] args) {
        // Database URL, username, and password
        String url = "jdbc:mysql://localhost:3306/mydatabase";
        String user = "root";
        String password = "password";

        try {
            // Load JDBC driver
            Class.forName("com.mysql.cj.jdbc.Driver");

            // Establish a connection
            Connection conn = DriverManager.getConnection(url, user, password);
            System.out.println("Connected to the database.");

            // Create a statement
            Statement stmt = conn.createStatement();
            ResultSet rs = stmt.executeQuery("SELECT * FROM mytable");

            // Process the result set
            while (rs.next()) {
                System.out.println("ID: " + rs.getInt("id"));
                System.out.println("Name: " + rs.getString("name"));
            }

            // Close connections
            rs.close();
            stmt.close();
            conn.close();
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Project Work: Desktop-Based Application Project


[Run](https://www.programiz.com/java-programming/online-compiler/)
For the project, you would typically create a more complex Java desktop application using Swing or JavaFX. Below is a basic example of a Swing application:

```java
import javax.swing.*;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class DesktopApp {
    public static void main(String[] args) {
        JFrame frame = new JFrame("Simple Desktop Application");
        JButton button = new JButton("Click Me");

        button.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                JOptionPane.showMessageDialog(frame, "Button Clicked!");
            }
        });

        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(300, 200);
        frame.setLayout(new FlowLayout());
        frame.add(button);
        frame.setVisible(true);
    }
}
```

 
