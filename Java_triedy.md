# Java - triedy

## Metódy

### House (Dom) 

```java
public class House {
  String color;
  double height;
  double width = 10.5;
  int rooms = 5;
}
```

### Tree (Strom) 

```java
public class Tree {
  String name = "elm";
  double height = 17.8;
  boolean leafs;
  int age;
}
```

### Person (Osoba) 

```java
public class Person {
  String name;
  String job;
  int age = 23;
  int kids = 1;
}
```

## Metódy

### Pozdrav 

```java
public class Hello {
	void sayHello() {
      System.out.println("Hello, my friend");
    }
}
```

### Text pozdravu 

```java
public class Greeting {
  String txt;
  void output() {
    System.out.print(txt);
    System.out.println("!");
  }
}
```

### Orámovanie pozdravu 

```java
public class BorderedGreeting {
    public String txt;
    public char symbol;

    public void output() {
        int borderLength = txt.length() + 3;
        String border = "";
        for (int i = 0; i < borderLength; i++) {
            border += symbol;
        }
        
        System.out.println(border);
        System.out.println(symbol + txt + "!" + symbol);
        System.out.println(border);
    }
}
```

### Auto 

```java
public class Car {
    public String car_type;
    public int speed = 50;

    public void faster() {
        speed += 10;
    }

    public void slower() {
        speed -= 5;
        if (speed < 0) {
            speed = 0;
        }
    }

    public void output() {
        System.out.println(car_type + ": " + speed);
    }
}
```

### Calculator 

```java
public class Calculator {
    
    public void sum(int a, int b) {
        System.out.println(a + b);
    }
    
    public void division(int dividend, int divisor) {
        if (divisor == 0) {
            System.out.println("Nulou deliť nemožno");
        } else {
            int quotient = dividend / divisor;
            int remainder = dividend % divisor;
            System.out.println(dividend + " : " + divisor + " = " + quotient + ", zvyšok " + remainder);
        }
    }
    
    public void digit_sum(int number) {
        int sum = 0;
        int n = Math.abs(number);
        
        while (n > 0) {
            sum += n % 10;
            n /= 10;
        }
        
        System.out.println(sum);
    }
}
```

### Car 

```java
public class Car {
    String car_type;
    int speed = 40;
    double fuel_consumption = 0.0;
    
    public void faster() {
        if (speed + 10 <= 180) {
            speed += 10;
        }
        else {
            speed = 180;
        }
        addConsumption();
    }
    
    public void addConsumption() {
        fuel_consumption += 0.5;
    }
    
    public void output() {
        System.out.println(car_type + ": " + speed + " / " + fuel_consumption);
    }
}
```

### Robot 

```java
class Robot {
    int x = 4;
    int y = 4;

    void left() {
        if (x - 1 >= 0) {
            x--;
        } else {
            System.out.println("BOOM");
        }
    }

    void right() {
        if (x + 1 <= 10) {
            x++;
        } else {
            System.out.println("BOOM");
        }
    }

    void up() {
        if (y + 1 <= 10) {
            y++;
        } else {
            System.out.println("BOOM");
        }
    }

    void down() {
        if (y - 1 >= 0) {
            y--;
        } else {
            System.out.println("BOOM");
        }
    }

    void output() {
        System.out.println("[" + x + "," + y + "]");
    }
}
```

### Pyramid 

```java
public class Pyramid {
    int floors;

    void classic() {
        for (int i = 1; i <= floors; i++) {
            for (int j = 0; j < floors - i; j++) {
                System.out.print(" ");
            }
            for (int j = 0; j < 2 * i - 1; j++) {
                System.out.print("*");
            }
            System.out.println();
        }
    }

    void reversed() {
        for (int i = floors; i >= 1; i--) {
            for (int j = 0; j < floors - i; j++) {
                System.out.print(" ");
            }
            for (int j = 0; j < 2 * i - 1; j++) {
                System.out.print("*");
            }
            System.out.println();
        }
    }

    void river() {
        classic();
        int riverLength = 2 * floors - 1;
        for (int i = 0; i < riverLength; i++) {
            System.out.print("=");
        }
        System.out.println();
    }
}
```

### TextProcesor 

```java
class TextProcesor {
    int operationCount;

    void getLength(String text) {
        operationCount++;
        System.out.println("Reťazec \"" + text + "\" má " + text.length() + " znakov");
    }

    void getDigits(String text) {
        operationCount++;
        String digits = "";
        for (int i = 0; i < text.length(); i++) {
            char c = text.charAt(i);
            if (Character.isDigit(c)) {
                digits += c;
            }
        }
        System.out.println(digits);
    }

    void getDigitCount(String text) {
        operationCount++;
        int count = 0;
        for (int i = 0; i < text.length(); i++) {
            char c = text.charAt(i);
            if (Character.isDigit(c)) {
                count++;
            }
        }
        System.out.println(count);
    }

    void getSumDigits(String text) {
        operationCount++;
        int sum = 0;
        for (int i = 0; i < text.length(); i++) {
            char c = text.charAt(i);
            if (Character.isDigit(c)) {
                sum += Character.getNumericValue(c);
            }
        }
        System.out.println(sum);
    }

    void getNumbers(String text) {
        operationCount++;
        String numbers = "";
        String currentNumber = "";

        for (int i = 0; i < text.length(); i++) {
            char c = text.charAt(i);
            if (Character.isDigit(c)) {
                currentNumber += c;
            } else {
                if (currentNumber.length() > 0) {
                    if (!numbers.isEmpty()) {
                        numbers += ", ";
                    }
                    numbers += currentNumber;
                    currentNumber = "";
                }
            }
        }

        if (currentNumber.length() > 0) {
            if (!numbers.isEmpty()) {
                numbers += ", ";
            }
            numbers += currentNumber + ", ";
        } else if (!numbers.isEmpty()) {
            numbers += ", ";
        }

        System.out.println(numbers);
    }

    void getOperationCount() {
        System.out.println(operationCount);
    }
}
```

### Square 

```java
class Square {
    int side;

    public void getContent(int side) {
        this.side = side;
        System.out.println("Obsah štvorca so stranou " + side + " je " + (side * side) + ".");
    }

    public void getCircumference(int side) {
        this.side = side;
        System.out.println("Obvod štvorca so stranou " + side + " je " + (4 * side) + ".");
    }

    public void drawFull(int side) {
        this.side = side;
        for (int i = 0; i < side; i++) {
            for (int j = 0; j < side; j++) {
                System.out.print("x");
            }
            System.out.println();
        }
        getContent(side);
    }

    public void drawEmpty(int side) {
        this.side = side;
        for (int i = 0; i < side; i++) {
            for (int j = 0; j < side; j++) {
                if (i == 0 || i == side - 1 || j == 0 || j == side - 1) {
                    System.out.print("x");
                } else {
                    System.out.print(" ");
                }
            }
            System.out.println();
        }
        getCircumference(side);
    }
}
```

### Drawer 

```java
class Drawer {
    void square(boolean full, String character, int size) {
        for (int i = 0; i < size; i++) {
            for (int j = 0; j < size; j++) {
                if (full || i == 0 || i == size - 1 || j == 0 || j == size - 1) {
                    System.out.print(character);
                } else {
                    System.out.print(" ");
                }
            }
            System.out.println();
        }
    }

    void diagonal(boolean full, int size) {
        if (full) {
            for (int i = 0; i < size; i++) {
                for (int j = 0; j < size; j++) {
                    System.out.print(i == j ? "x" : " ");
                }
                System.out.println();
            }
        } else {
            for (int i = 0; i < size; i++) {
                for (int j = 0; j < size; j++) {
                    if (i == 0 || i == size - 1 || j == 0 || j == size - 1) {
                        System.out.print("x");
                    } else if (i == j) {
                        System.out.print(" ");
                    } else {
                        System.out.print("x");
                    }
                }
                System.out.println();
            }
        }
    }

    void rectangle(boolean full, int rows, int cols) {
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                if (full || i == 0 || i == rows - 1 || j == 0 || j == cols - 1) {
                    System.out.print("x");
                } else {
                    System.out.print(" ");
                }
            }
            System.out.println();
        }
    }

    void triangle(boolean full, int size) {
        for (int i = 0; i < size; i++) {
            for (int j = 0; j < size - i; j++) {
                if (full || i == 0 || j == 0 || j == size - i - 1) {
                    System.out.print("x");
                } else {
                    System.out.print(" ");
                }
            }
            System.out.println();
        }
    }
}
```

### Tickets 

```java
public class Tickets {
    void getData(String destination, int count) {
        int price = 0;
        
        switch(destination) {
            case "Madrid": price = 500; break;
            case "Prague": price = 200; break;
            case "New York": price = 1200; break;
            case "Amsterdam": price = 400; break;
            case "Roma": price = 350; break;
            case "Moscow": price = 800; break;
            case "Krakow": price = 450; break;
            case "Paris": price = 333; break;
            case "Viena": price = 800; break;
            case "London": price = 678; break;
            default:
                System.out.println("Letenky do destinácie " + destination + " nie sú k dispozícii.");
                return;
        }
        
        int total = price * count;
        System.out.println("Vaše letenky v počte " + count + " do destinácie " + destination + " stoja " + total + " EUR.");
    }
}
```

### Súčet 

```java
public class MyClass {
    public double sum(double a, double b) {
        double result = a + b;
        return Math.round(result * 1000.0) / 1000.0;
    }
}
```

### Porovnanie 

```java
public class MyClass {
    public int getMax(int a, int b) {
        if (a >= b) {
            return a;
        } else {
            return b;
        }
    }
}
```

### Súčin 3 

```java
public class MyClass {
    public int product(int a, int b, int c) {
        long product = (long) a * b * c;
      
        int rounded;
        if (product >= 0) {
            rounded = (int) ((product + 5) / 10 * 10);
        } else {
            rounded = (int) ((product - 5) / 10 * 10);
        }

        return rounded;
    }
}
```

### Mocnina 

```java
public class MyClass {
    public int power(int base, int exponent) {
        if (exponent < 0) {
            return 0;
        }

        int result = 1;
        for (int i = 0; i < exponent; i++) {
            result *= base;
        }
        return result;
    }
}
```

### Delitele 5 

```java
public class MyClass {

    public String get5(int n) {
        if (n < 5 && n > 0 || n == 0) {
            return "-";
        }

        String result = "";
        if (n >= 5) {
            for (int i = 5; i <= n; i += 5) {
                result += i + ",";
            }
        } else {
            for (int i = -5; i >= n; i -= 5) {
                result += i + ",";
            }
        }

        if (!result.isEmpty()) {
            result = result.substring(0, result.length() - 1) + ".";
        }
        return result;
    }
}
```

### Súčet a súčin 

```java
public class MyClass {

    public String process(int a, int b) {
        int sum = a + b;
        int product = a * b;
        return sum + "\n" + product;
    }
}
```

### Riadok a stĺpec 

```java
public class MyClass {

    public String row(int n) {
        String result = "";
        for (int i = 0; i < n; i++) {
            result += 'o';
        }
        return result;
    }

    public String column(int n) {
        String result = "";
        for (int i = 0; i < n; i++) {
            result += 'o';
            if (i < n - 1) {
                result += "\n";
            }
        }
        return result;
    }
}
```

### Postupnosť 

```java
public class MyClass {
    public String stars(int n) {
        StringBuilder result = new StringBuilder();
        for (int i = 1; i <= n; i++) {
            for (int j = 0; j < i; j++) {
                result.append("x");
            }
            if (i < n) {
                result.append("\n");
            }
        }
        return result.toString();
    }
}
```

### Maximum v poli 

```java
public class MyClass {

    public String getMax(int[] n) {
        int max = n[0];
        for (int i = 1; i < n.length; i++) {
            if (n[i] > max) {
                max = n[i];
            }
        }
        return ""+max;
    }
}
```

### Súčet a priemer prvkov v poli 

```java
public class MyClass {

    public String getData(int[] n) {
        int sum = 0;
        for (int i = 0; i < n.length; i++) {
            sum += n[i];
        }
        double avg = (double) sum / n.length;
        double roundedAvg = Math.round(avg * 10) / 10.0;

        return "sum: " + sum + "\navg: " + roundedAvg;
    }
}
```

### Nadpriemerné prvky 

```java
public class MyClass {

    public String getData(double[] n) {
        double sum = 0;
        for (int i = 0; i < n.length; i++) {
            sum += n[i];
        }
        double avg = (double) sum / n.length;
        boolean flag = false;
        String result = "";
        for (int i = 0; i < n.length; i++) {
            if (n[i] > avg) {
                if (flag) {
                    result += ",";
                }
                flag = true;
                result += n[i];
            }
        }
        return result+".";
    }
}
```

### Porovnanie polí 

```java
import java.util.Arrays;

public class MyClass {

    public boolean compareData(int[] array1, int[] array2) {
        if (array1.length != array2.length) {
            return false;
        }

        Arrays.sort(array1);
        Arrays.sort(array2);

        return Arrays.equals(array1, array2);
    }
}
```

### Usporiadané pole? 

```java
public class MyClass {

    public boolean getInfo(int[] array) {
        for (int i = 0; i < array.length - 1; i++) {
            if (array[i] > array[i + 1]) {
                return false;
            }
        }
        return true;
    }
}
```

### Interval? 

```java
public class MyClass {

    public boolean compareData(int[] arr, int bound1, int bound2) {int min = Math.min(bound1, bound2);
        int max = Math.max(bound1, bound2);

        for (int num : arr) {
            if (num < min || num > max) {
                return false;
            }
        }
        return true;
    }
}
```

### Pozícia najdlhšieho 

```java
public class MyClass {

    public int getMax(String[] arr) {
        int maxLength = 0;
        for (String str : arr) {
            if (str.length() > maxLength) {
                maxLength = str.length();
            }
        }
        for (int i = 0; i < arr.length; i++) {
            if (arr[i].length() == maxLength) {
                return i;
            }
        }
        return -1;
    }
}
```

### Spracuj pole 

```java
public class MyClass {

    public int[] process(int[] arr, int n) {
        int[] result = new int[arr.length];
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] < 0) {
                result[i] = n;
            }
            else {
                result[i] = arr[i];
            }
        }
        return result;
    }
}
```

## Zapuzdrenosť

### Power 

```java
public class Power {
    private int value;
    public void setValues(int v) {
        value = v;
    }
    public int getPower3() {
        return (int) Math.pow(value, 3);
    }
    public int getPower(int exponent) {
        return (int) Math.pow(value, exponent);
    }
}
```

### GreetMe 

```java
public class GreetMe {
    private String greeting;
    
    public void setGreeting(String greeting) {
        this.greeting = greeting;
    }
    
    public String greet(String name) {
        return greeting + ", " + name + "!";
    }
}
```

### Prism 

```java
public class Prism {
    private int a, b, c;

    public void setValues(int a, int b, int c) {
        if (a <= 0) {
            this.a = 1;
        } else {
            this.a = a;
        }

        if (b <= 0) {
            this.b = 1;
        } else {
            this.b = b;
        }

        if (c <= 0) {
            this.c = 1;
        } else {
            this.c = c;
        }
    }

    public int getCapacity() {
        return a * b * c;
    }

    public int getSurface() {
        return 2 * (a*b + a*c + b*c);
    }
}
```

### Tree 

```java
public class Tree {
    private int age;
    private int height;
    private int width;

    public void setValues(int age, int width, int height) {
        this.age = Math.abs(age);
        this.width = Math.abs(width);
        this.height = Math.abs(height);
    }

    public void growOld() {
        age++;
        width += (int)(age * 0.5 + 1);
        height += (int)(age / 10.0);
    }

    public int getAge() {
        return age;
    }

    public int getWidth() {
        return width;
    }

    public int getHeight() {
        return height;
    }

    public String getInfo() {
        return "Age: " + age + "\nWidth: " + width + "\nHeight: " + height;
    }
}
```

## Konštruktory

### Calculator 

```java
public class Calculator {
    private int a;
    private int b;

    public Calculator(int a, int b) {
        this.a = a;
        this.b = b;
    }

    public int sum() {
        return a + b;
    }

    public int product() {
        return a * b;
    }

    public int difference() {
        return a - b;
    }

    public int quotient() {
        if (b == 0)
            return -1;
        else
            return a / b;
    }

    public int modulo() {
        if (b == 0)
            return -1;
        else
            return a % b;
    }

    public void setA(int a) {
        this.a = a;
    }

    public void setB(int b) {
        this.b = b;
    }

    public int getA() {
        return a;
    }

    public int getB() {
        return b;
    }
}
```

### 

```java

```

### Stopwatch 

```java
public class Stopwatch {
    private int hours, minutes, seconds;

    public Stopwatch(int hours, int minutes, int seconds) {
        this.hours = Math.max(hours, 0);
        this.minutes = Math.max(minutes, 0);
        this.seconds = Math.max(seconds, 0);

        this.minutes += this.seconds / 60;
        this.seconds %= 60;

        this.hours += this.minutes / 60;
        this.minutes %= 60;

        this.hours %= 24;
    }

    public Stopwatch() {
        this(1, 1, 1);
    }

    public void tick() {
        seconds++;
        if (seconds == 60) {
            seconds = 0;
            minutes++;
            if (minutes == 60) {
                minutes = 0;
                hours++;
                if (hours == 24) {
                    hours = 0;
                }
            }
        }
    }

    public String getTime() {
        return String.format("%02d:%02d:%02d", hours, minutes, seconds);
    }
}
```

### Label 

```java
public class Label {
    private String title;
    private String name;
    private String surname;

    public Label(String name, String surname) {
        if (name.equals("")) {
            this.name = "Anonymous";
        } else {
            this.name = name;
        }

        if (surname.equals("")) {
            this.surname = "Anonymous";
        } else {
            this.surname = surname;
        }

        this.title = "";
    }

    public Label(String title, String name, String surname) {
        if (name.equals("")) {
            this.name = "Anonymous";
        } else {
            this.name = name;
        }

        if (surname.equals("")) {
            this.surname = "Anonymous";
        } else {
            this.surname = surname;
        }

        setTitle(title);
    }

    public void setTitle(String title) {
        if (title.equals("")) {
            this.title = "titled";
        } else {
            this.title = title;
        }
        if (this.title.charAt(this.title.length()-1) != '.') {
            this.title += ".";
        }
    }

    public String getTitle() {
        return title;
    }

    public String getLabel() {
        if (title.equals("")) {
            return name + " " + surname;
        } else {
            return title + " " + name + " " + surname;
        }
    }
    public static void main(String[] args) {
        Label l1 = new Label("James","Bond");
        System.out.println(l1.getLabel()); // vypíše James Bond
        Label l2 = new Label("","James","Bond");
        System.out.println(l2.getLabel()); // vypíše titled. James Bond
        l2.setTitle("Mr.");
        System.out.println(l2.getLabel()); // vypíše Mr. James Bond
    }
}
```

### Car 

```java
public class Car {
    private String brand;
    private String ecv;
    private int speed;

    public Car(String brand, String ecv, int speed) {
        if (brand == null || brand.equals("")) {
            this.brand = "Anonymous";
        } else {
            this.brand = brand;
        }

        if (ecv == null || ecv.equals("")) {
            this.ecv = "XX-000XX";
        } else {
            this.ecv = ecv;
        }

        if (speed < 0) {
            this.speed = 0;
        } else {
            this.speed = speed;
        }
    }

    public void faster() {
        speed++;
    }

    public void slower() {
        if (speed > 0) {
            speed--;
        }
    }

    public void stop() {
        speed = 0;
    }

    public String getInfo() {
        return brand + ": " + ecv + ", " + speed;
    }

    public static void main(String[] args) {
        Car c = new Car("Renault", "XX-123AB", 12);
        System.out.println(c.getInfo()); // Renault: XX-123AB, 12

        c.faster(); c.faster(); c.faster(); c.faster();
        System.out.println(c.getInfo()); // Renault: XX-123AB, 16

        c.slower();
        System.out.println(c.getInfo()); // Renault: XX-123AB, 15

        c.stop();
        System.out.println(c.getInfo()); // Renault: XX-123AB, 0
    }
}
```

### Spider 

```java
public class Spider {
    private int rows;
    private int columns;
    private int x;
    private int y;
    private char borderChar;

    public Spider(int rows, int columns, int x, int y, char borderChar) {
        this.rows = Math.max(rows, 5);
        this.columns = Math.max(columns, 5);

        if (x >= 2 && x <= this.columns - 1) {
            this.x = x;
        } else {
            this.x = 3;
        }

        if (y >= 2 && y <= this.rows - 1) {
            this.y = y;
        } else {
            this.y = 2;
        }

        this.borderChar = borderChar;
    }

    public String left() {
        if (x > 2) {
            x--;
            return "OK";
        } else {
            return "Au!";
        }
    }

    public String right() {
        if (x < columns - 1) {
            x++;
            return "OK";
        } else {
            return "Au!";
        }
    }

    public String up() {
        if (y > 2) {
            y--;
            return "OK";
        } else {
            return "Au!";
        }
    }

    public String down() {
        if (y < rows - 1) {
            y++;
            return "OK";
        } else {
            return "Au!";
        }
    }

    public String getSpider() {
        return "[" + x + "," + y + "]";
    }

    public String getDimensions() {
        return rows + "x" + columns;
    }

    public String getInfo() {
        String result = "";

        for (int row = 1; row <= rows; row++) {
            for (int col = 1; col <= columns; col++) {
                if (row == 1 || row == rows || col == 1 || col == columns) {
                    result += borderChar;
                } else if (row == y && col == x) {
                    result += 'o';
                } else {
                    result += ' ';
                }
            }
            result += '\n';
        }

        return result.trim();
    }
}
```

## Viac o triedach

### Rovnaké prvky polí 

```java
import java.util.Arrays;

public class MyClass {

    public String compareData(String[] arr1, String[] arr2) {
        boolean[] used = new boolean[arr2.length];

        int count = 0;
        for (String element : arr1) {
            for (int j = 0; j < arr2.length; j++) {
                if (!used[j] && element.equals(arr2[j])) {
                    count++;
                    used[j] = true;
                    break;
                }
            }
        }

        String[] result = new String[count];
        int resultIndex = 0;
        used = new boolean[arr2.length];

        for (String element : arr1) {
            for (int j = 0; j < arr2.length; j++) {
                if (!used[j] && element.equals(arr2[j])) {
                    result[resultIndex++] = element;
                    used[j] = true;
                    break;
                }
            }
        }

        Arrays.sort(result);

        String output = "";

        for (String s : result) {
            output += s + "\n";
        }

        output += "sú spoločné prvky polí:\n";
        output += arrayToString(arr1) + "\n";
        output += arrayToString(arr2);

        return output;
    }

    private String arrayToString(String[] arr) {
        String result = "[";
        for (int i = 0; i < arr.length; i++) {
            result += arr[i];
            if (i < arr.length - 1) {
                result += ",";
            }
        }
        result += "]";
        return result;
    }

    public static void main(String[] args) {
        MyClass mc = new MyClass();
        String[] firstArray = {"mama", "tata", "baba", "dedo", "mama"};
        String[] secondArray = {"mama", "dedo", "baba", "mama", "zima"};
        String result = mc.compareData(firstArray, secondArray);
        System.out.println(result);
    }
}
```

### Student 

```java
public class Student {
    private String meno;
    private String priezvisko;
    private int rocnyk;
    private int stipendium;

    public Student(String meno, String priezvisko, int rocnyk, int stipendium) {
        this.meno = meno;
        this.priezvisko = priezvisko;

        if (rocnyk < 1) {
            throw new IllegalArgumentException("too low year of study");
        }
        if (rocnyk > 5) {
            throw new IllegalArgumentException("too high year of study");
        }
        this.rocnyk = rocnyk;

        if (stipendium < 0) {
            throw new NumberFormatException("negative scholarship");
        }
        if (stipendium > 10000) {
            throw new NumberFormatException("too expensive scholarship");
        }
        this.stipendium = stipendium;
    }

    public String getInfo() {
        return meno + " " + priezvisko + ", " + rocnyk + "., " + stipendium + " EUR";
    }
}
```

### Bus 

```java
public class Bus {
    private int maxPassengers;
    private int currentPassengers;
    private boolean isMoving;
    private boolean doorsOpen;

    public Bus(int maxPassengers) {
        if (maxPassengers < 10) {
            this.maxPassengers = 10;
        } else {
            this.maxPassengers = maxPassengers;
        }
        this.currentPassengers = 0;
        this.isMoving = false;
        this.doorsOpen = true;
    }

    public Bus(int currentPassengers, int maxPassengers) {
        if (currentPassengers < 0 || maxPassengers < 0 || currentPassengers > maxPassengers) {
            throw new IllegalArgumentException("<0 or too much");
        }
        this.currentPassengers = currentPassengers;
        this.maxPassengers = maxPassengers;
        this.isMoving = false;
        this.doorsOpen = true;
    }

    public void closeDoor() {
        doorsOpen = false;
    }

    public void openDoor() {
        doorsOpen = true;
    }

    public void move() {
        if (!doorsOpen) {
            isMoving = true;
        }
    }

    public void stop() {
        isMoving = false;
    }

    public void exiting(int count) {
        if (count <= 0) return;
        if (!doorsOpen) return;

        if (count > currentPassengers) {
            currentPassengers = 0;
            throw new IllegalArgumentException("empty bus");
        } else {
            currentPassengers -= count;
        }
    }

    public void boarding(int count) {
        if (count <= 0) return;
        if (!doorsOpen) return;

        int availableSeats = maxPassengers - currentPassengers;
        if (count > availableSeats) {
            currentPassengers = maxPassengers;
            throw new IllegalArgumentException("full bus " + (count - availableSeats) + " more");
        } else {
            currentPassengers += count;
        }
    }

    public String getInfo() {
        return currentPassengers + "/" + maxPassengers + " " + doorsOpen + "/" + isMoving;
    }
}
```

## Statické premenné

### Passport 

```java
public class Passport {
    private static int nextSerial = 100001;

    private String owner;
    private int yearOfBirth;
    private int serialNumber;

    public Passport(String owner, int yearOfBirth) {
        if (owner == null || owner == "" || yearOfBirth < 1900) {
            this.owner = "invalid";
            this.yearOfBirth = -1;
        } else {
            this.owner = owner;
            this.yearOfBirth = yearOfBirth;
        }

        this.serialNumber = nextSerial++;
    }

    public String getInfo() {
        if (owner.equals("invalid")) {
            return "invalid: " + serialNumber;
        }
        return owner + "(" + yearOfBirth + "): " + serialNumber;
    }
}
```

### Landrover 

```java
public class Landrover {
    // Statické premenné pre sériové číslo a aktuálnu farbu
    private static int nextSerialNumber = 100;
    private static String currentColor = "red";

    // Inštančné atribúty
    private String farba;
    private int serioveCislo;
    private String operacnySystem;
    private String majitel;

    // Konštruktor
    public Landrover(String majitel, String operacnySystem) {
        if (!majitel.equals("")) {
            this.majitel = majitel;
        }
        else {
            this.majitel = "x";
        }

        if (!operacnySystem.equals("")) {
            this.operacnySystem = operacnySystem;
        }
        else {
            this.operacnySystem = "x";
        }

        this.serioveCislo = nextSerialNumber++;
        this.farba = currentColor;
    }

    public void changeColor(String newColor) {
        currentColor = newColor;
    }

    public int getOrder() {
        return serioveCislo - 99;
    }

    public String getInfo() {
        return majitel + " (" + serioveCislo + "): " + farba + ", OS: " + operacnySystem;
    }
}
```

### Preukaz študenta 

```java
public class StudentCard {
    private String name;
    private int cardNumber;
    private String gender;
    private int credit;

    private static int maleCounter = 1;
    private static int femaleCounter = 1;

    public StudentCard(String name, String gender) {
        this.name = name;
        if (gender.equals("male")) {
            this.gender = "male";
        }
        else {
            this.gender = "female";
        }

        this.credit = 20;

        if (this.gender.equals("male")) {
            this.cardNumber = maleCounter++;
        } else {
            this.cardNumber = femaleCounter++;
        }
    }

    public static void resetNumbering() {
        maleCounter = 1;
        femaleCounter = 1;
    }

    @Override
    public String toString() {

        return name + " (" + cardNumber + ") - " + gender + " credit: " + credit;
    }
}
```

### Batérie 

```java
public class Battery {
    private static int nextSerial = 100;
    private static int defaultLife = 5000;

    private int serialNumber;
    private int price;
    private int life;

    public Battery(int manufacturingPrice) {
        if (manufacturingPrice < 10) {
            this.price = 10;
        } else if (manufacturingPrice > 1000) {
            this.price = 1000;
        } else {
            this.price = manufacturingPrice;
        }

        this.serialNumber = nextSerial++;
        this.life = defaultLife;
    }

    public static void changeLife(int newLife) {
        if (newLife < 200) {
            defaultLife = 200;
        } else if (newLife > 10000) {
            defaultLife = 10000;
        } else {
            defaultLife = newLife;
        }
    }

    public void changePrice(int delta) {
        int newPrice = this.price + delta;
        if (newPrice < 10) {
            this.price = 10;
        } else if (newPrice > 500) {
            this.price = 500;
        } else {
            this.price = newPrice;
        }
    }

    public String toString() {
        return serialNumber+1 + " (price: " + price + "), life: " + life;
    }

    
}
```

## Dedičnosť prakticky

### Rectangle 

It gives 18/30, but if you look in the tests result, the wanted output and real output is the same. So that's a website problem.

```java
public class Rectangle {
    protected int a;
    protected int b;

    public Rectangle(int a, int b) {
        if (a <= 0) {
            this.a = 1;
        } else {
            this.a = a;
        }
        if (b <= 0) {
            this.b = 1;
        } else {
            this.b = b;
        }
    }

    public int getContent() {
        return a * b;
    }

    public int getCircuit() {
        return 2 * (a + b);
    }

    public String getDraw() {
        int width = Math.max(a, b);
        int height = Math.min(a, b);
        String result = "";
        
        for (int i = 0; i < height; i++) {
            for (int j = 0; j < width; j++) {
                result += "o";
            }
            if (i < height - 1) {
                result += "\n";
            }
        }
        return result;
    }

    @Override
    public String toString() {
        return "a x b: " + a + " x " + b;
    }
}
```

```java
public class TurnedRectangle extends Rectangle {
    public TurnedRectangle(int a, int b) {
        super(a, b);
    }

    @Override
    public String getDraw() {
        int width = Math.min(a, b);
        int height = Math.max(a, b);
        String result = "";
        
        for (int i = 0; i < height; i++) {
            for (int j = 0; j < width; j++) {
                result += "o";
            }
            if (i < height - 1) {
                result += "\n";
            }
        }
        return result;
    }
}
```

### Animal 

```java
class Animal {
    private String species;
    private String sound;
    private int maxWeight;
    private int averageLifespan;

    public Animal(String species, String sound, int maxWeight, int averageLifespan) {
        this.species = species;
        this.sound = sound;
        
        if (maxWeight < 1) {
            this.maxWeight = 1;
        } else {
            this.maxWeight = maxWeight;
        }
        
        if (averageLifespan < 1) {
            this.averageLifespan = 1;
        } else {
            this.averageLifespan = averageLifespan;
        }
    }

    public String getSpecies() {
        return species;
    }

    public String getSound() {
        return sound;
    }

    public int getAge() {
        return averageLifespan;
    }

    public int getMaxWeight() {
        return maxWeight;
    }

    public String sing() {
        return sound + " " + sound + " " + sound;
    }

    public String toString() {
        return species + ": " + maxWeight + "/" + averageLifespan + " (" + sound + ")";
    }
}
```

```java
class Bird extends Animal {
    private int wingspan;

    public Bird(String species, String sound, int maxWeight, int averageLifespan, int wingspan) {
        super(species, sound, maxWeight, averageLifespan);
        
        if (wingspan < 1) {
            this.wingspan = 1;
        } else {
            this.wingspan = wingspan;
        }
    }

    public String toString() {
        return getSpecies() + ": " + getMaxWeight() + "/" + getAge() + "/" + wingspan + " (" + getSound() + ")";
    }
}
```

```java
class Fish extends Animal {
    private String waterType;

    public Fish(String species, String sound, int maxWeight, int averageLifespan, String waterType) {
        super(species, sound, maxWeight, averageLifespan);
        
        if (!waterType.equals("freshwater") && !waterType.equals("marine")) {
            this.waterType = "marine";
        } else {
            this.waterType = waterType;
        }
    }

    public String toString() {
        return super.toString() + " - " + waterType;
    }
}
```

### Čiara a obdžnik 

```java
class Line {
    protected double zaciatokX;
    protected double zaciatokY;
    protected double koniecX;
    protected double koniecY;

    public Line(double zaciatokX, double zaciatokY, double koniecX, double koniecY) {
        if (zaciatokX == koniecX && zaciatokY == koniecY) {
            this.zaciatokX = 0;
            this.zaciatokY = 0;
            this.koniecX = 10;
            this.koniecY = 10;
        } else {
            this.zaciatokX = zaciatokX;
            this.zaciatokY = zaciatokY;
            this.koniecX = koniecX;
            this.koniecY = koniecY;
        }
    }

    public double getSize() {
        double dx = koniecX - zaciatokX;
        double dy = koniecY - zaciatokY;
        return Math.sqrt(dx * dx + dy * dy);
    }

    public String toString() {
        return "[" + (int)zaciatokX + "," + (int)zaciatokY + "] - [" + (int)koniecX + "," + (int)koniecY + "]";
    }
}
```

```java
class Rectangle extends Line {
    public Rectangle(double zaciatokX, double zaciatokY, double koniecX, double koniecY) {
        super(zaciatokX, zaciatokY, koniecX, koniecY);
    }

    public double getSize() {
        double width = Math.abs(koniecX - zaciatokX);
        double height = Math.abs(koniecY - zaciatokY);
        return width * height;
    }
}
```

### Osoba a zamestanec 

```java
public class Person {
    String meno;
    int rok_narodenia;
    int vyska;
    int hmotnost;

    public Person(String meno, int rok_narodenia, int vyska, int hmotnost) {
        this.meno = meno;
        
        if (rok_narodenia < 1900 || rok_narodenia > 2020) {
            this.rok_narodenia = 2000;
        } else {
            this.rok_narodenia = rok_narodenia;
        }
        
        if (vyska < 100 || vyska > 250) {
            this.vyska = 170;
        } else {
            this.vyska = vyska;
        }
        
        if (hmotnost < 50 || hmotnost > 150) {
            this.hmotnost = 80;
        } else {
            this.hmotnost = hmotnost;
        }
    }

    public int getAge() {
        return 2021 - rok_narodenia;
    }

    public String whatHeight() {
        if (vyska > 170) {
            return "above average";
        } else if (vyska < 170) {
            return "below average";
        } else {
            return "average";
        }
    }

    public String toString() {
        return meno + " (" + rok_narodenia + "), height: " + vyska + ", weight: " + hmotnost;
    }
}
```

```java
public class Employee extends Person {
    int plat;
    int pocet_deti;

    public Employee(String meno, int rok_narodenia, int vyska, int hmotnost, int plat, int pocet_deti) {
        super(meno, rok_narodenia, vyska, hmotnost);
        
        if (plat < 100) {
            this.plat = 100;
        } else if (plat > 10000) {
            this.plat = 10000;
        } else {
            this.plat = plat;
        }
        
        if (pocet_deti < 0) {
            this.pocet_deti = 0;
        } else if (pocet_deti > 15) {
            this.pocet_deti = 15;
        } else {
            this.pocet_deti = pocet_deti;
        }
    }

    public String toString() {
        return super.toString() + ", salary: " + plat + ", kids: " + pocet_deti;
    }
}
```

## Polymorfizmus

### Person 

Yet again, it scores 27/45, but the needed and program output is identical. Blame the website.

```java
public class Person {
    private String name;
    private String address;
    private int birthYear;

    public Person(String name, String address, int birthYear) {
        this.name = name;
        this.address = address;
        if (birthYear >= 1900 && birthYear <= 2020) {
            this.birthYear = birthYear;
        } else {
            this.birthYear = 2000;
        }
    }

    public String toString() {
        return name + " (" + birthYear + "), " + address;
    }
}
```

```java
public class Man extends Person {
    private int income;

    public Man(String name, String address, int birthYear, int income) {
        super(name, address, birthYear);
        if (income >= 100 && income <= 10000) {
            this.income = income;
        } else {
            this.income = 0;
        }
    }

    public String toString() {
        return super.toString() + ": " + income + " EUR";
    }
}
```

```java
public class Woman extends Person {
    private String hairColor;
    private int hairLength;

    public Woman(String name, String address, int birthYear, String hairColor, int hairLength) {
        super(name, address, birthYear);
        if (hairColor.equals("black") || hairColor.equals("blond") || hairColor.equals("brown") || hairColor.equals("red")) {
            this.hairColor = hairColor;
        } else {
            this.hairColor = "neutral";
        }
        if (hairLength < 0) {
            this.hairLength = 1;
        } else if (hairLength > 120) {
            this.hairLength = 120;
        } else {
            this.hairLength = hairLength;
        }
    }

    public String toString() {
        return super.toString() + ", hairs: " + hairColor + " - " + hairLength;
    }
}
```

```java
public class Kid extends Person {
    private String parentName;

    public Kid(String name, String address, int birthYear, String parentName) {
        super(name, address, birthYear);
        this.parentName = parentName;
    }

    public String toString() {
        return super.toString() + ", parent: " + parentName;
    }
}
```

```java
public class CustomerList {
    private Person[] customers;
    private int count;

    public CustomerList() {
        customers = new Person[20];
        count = 0;
    }

    public void addMan(String name, String address, int birthYear, int income) {
        if (count < 20) {
            customers[count] = new Man(name, address, birthYear, income);
            count++;
        }
    }

    public void addWoman(String name, String address, int birthYear, String hairColor, int hairLength) {
        if (count < 20) {
            customers[count] = new Woman(name, address, birthYear, hairColor, hairLength);
            count++;
        }
    }

    public void addKid(String name, String address, int birthYear, String parentName) {
        if (count < 20) {
            customers[count] = new Kid(name, address, birthYear, parentName);
            count++;
        }
    }

    public String getList() {
        String result = "";
        for (int i = 0; i < count; i++) {
            result += customers[i].toString();
            if (i < count - 1) {
                result += "\n";
            }
        }
        return result;
    }
}
```