# Java - základy jazyka

## Príkazy výstupu

### Výstup údajov 
```java
public class JavaApp {

    public static void main(String[] args) {
      	System.out.println("Joseph");
      	System.out.println("Cucumber");

    }
    
}
```
### Hello World! 
```java
public class JavaApp {
    
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}
```

### Pozdrav
```java
public class JavaApp {
    
    public static void main(String[] args) {
        System.out.println("Hello");
      	System.out.println("Good day");
      	System.out.println("Hi");

    }
}
```

### Výpis do riadku 
```java
public class JavaApp {
    
    public static void main(String[] args) {
        System.out.print("I ");
      	System.out.print("am ");
      	System.out.print("learning.");
    }
}
```

## Premenné

### Výpočty - čísla 
```java
public class JavaApp {
    
    public static void main(String[] args) {
        System.out.print(5 + 48 + 3 * 11 - 96);
    }
}
```

### Výpočet - premenné 
```java
public class JavaApp {
    
    public static void main(String[] args) {
        int a = 10; int b = 17;
        System.out.println(a+b);
    }
}
```

### Výpočet - do premennej 
```java
public class JavaApp {
    
    public static void main(String[] args) {
        int a = 5; int b = 4;
        int product = a * b;
        System.out.println(product);        
    }
}
```

## Načítanie hodnôt

### Načítanie hodnôt 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int x = sc.nextInt();
        System.out.println(x * 2);
    }
}
```

### Plocha štvorca 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int x = sc.nextInt();
        System.out.println(x * x);
    }
}
```

### Rodinné prídavky 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int x = sc.nextInt();
        System.out.println(x * 30);
    }
}
```

### Tretia mocnina 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int x = sc.nextInt();
        System.out.println(x * x * x);
    }
} 
```

### Súčet dvoch čísel 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        System.out.println(a + b);
    }
}
```

### Obvod a obsah obdĺžnika 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        System.out.println(a * b + " " + 2 * (a + b));
    }
}
```

### Plocha a objem kvádra
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();

        int surfaceArea = 2 * (a * b + b * c + c * a);
        int volume = a * b * c;

        System.out.println(surfaceArea + " " + volume);
    }
}
```

### Dolet lietadla 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        System.out.println(a * b);
    }
}
```

## Podmienený príkaz

### Absolútna hodnota čísla 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        if (a > 0) {
            System.out.println(a);
        } else {
            System.out.println(-a);
        }
    }
}
```

### Porovnanie dvoch čísel 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        if (a > b) {
            System.out.println(a);
        } else if (a < b) {
            System.out.println(b);
        } else {
            System.out.println("cisla su rovnake");
        }
    }
}
```

### Maximum z troch čísel 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();
        int max = a;
        if (b > max) {
            max = b;
        }
        if (c > max) {
            max = c;
        }
        if (a == b && b == c) {
            System.out.println("Cisla su rovnake");
        } else {
            System.out.println(max);
        }
    }
}
```

## Cyklus

### Opakovanie výpisu 
```java
public class JavaApp {
    public static void main(String[] args) {

        for (int i = 1; i <= 10; i++) {
            System.out.println("Ahoj");
        }
    }
}
```

### Výpis s poradovým číslom 
```java
public class JavaApp {
    public static void main(String[] args) {

        for (int i = 1; i <= 10; i++) {
            System.out.println(i+"Ahoj");
        }
    }
}
```

### Súčet prvých n čísel 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int sum = 0;
        for (int i = 1; i <= n; i++) {
            sum += i;
            System.out.println(sum);
        }
    }
}

```

### Faktoriál 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int factorial = 1;
        for (int i = 1; i <= n; i++) {
            factorial *= i;
            System.out.println(factorial);
        }
    }
}

```

### Súčin kladných čísel bez násobenia 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a = scanner.nextInt();
        int b = scanner.nextInt();
        int x = 0;
        for (int i = 0; i < b; i++) {
            x += a;
        }
        System.out.println(x);
    }
}
```

### Súčin čísel v intervale 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a = scanner.nextInt();
        int b = scanner.nextInt();
        int product = 1;
        for (int i = a; i <= b; i++) {
            product *= i;
            System.out.println(i - a + 1 + " - " + product);
        }
        System.out.println(product);
    }
}

```

### Násobilka 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a = scanner.nextInt();
        for (int i = 1; i <= 10; i++) {
            System.out.println(i + " * " + a + " = " + i * a);
        }
    }
}

```

### Súčin čísel bez násobenia II. 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int a = scanner.nextInt();
        int b = scanner.nextInt();
        int result = 0;
        boolean isNegative = (a < 0 && b > 0) || (a > 0 && b < 0);
        a = Math.abs(a);
        b = Math.abs(b);
        for (int i = 0; i < b; i++) {
            result += a;
        }
        if (isNegative) {
            result = -result;
        }
        System.out.println(result);
    }
}

```

### Zvyšok po delení bez delenia 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a = scanner.nextInt();
        int b = scanner.nextInt();

        if (b == 0) {
            System.out.println("Nulou sa nedeli");
        } else {
            int c = a;
            while (c >= b) {
                c -= b;
            }
            System.out.println(c);
        }
    }
}

```

### Najväčší spoločný deliteľ 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a = scanner.nextInt();
        int b = scanner.nextInt();

        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }

        System.out.println(a);
    }
}

```

### Euklidov algoritmus 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a = scanner.nextInt();
        int b = scanner.nextInt();

        int old_a = a;
        int old_b = b;

        while (a != b) {
            if (a > b) {
                a -= b;
            } else {
                b -= a;
            }
        }

        int gcd = a;
        int lcm = (old_a * old_b) / gcd;

        System.out.println(gcd + " " + lcm);
    }
}

```

### Minimum a maximum 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int min = Integer.MAX_VALUE;
        int max = Integer.MIN_VALUE;

        while (true) {
            int num = scanner.nextInt();
            if (num == 999999) {
                break;
            }
            if (num < min) {
                min = num;
            }
            if (num > max) {
                max = num;
            }
        }
        System.out.println(min + " " + max);
    }
}

```

## Číselné údajové typy

### Podiel a zvyšok 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        if (b == 0) {
            System.out.println("Nulou nemozno delit");
        }
        else {
            int c = a / b;
            System.out.print(c+" "+(a%b));
        }
    }
}



```

### Párne čísla od 1 do 20 
```java
public class JavaApp {
    public static void main(String[] args) {
        for (int i = 2; i <= 20; i += 2) {
            System.out.println(i);
        }
    }
}
```

### Trojuholník 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double a = sc.nextDouble();
        double b = sc.nextDouble();
        double c = sc.nextDouble();

        if (a + b > c && a + c > b && b + c > a) {
            double s = (a + b + c) / 2;
            double result = Math.sqrt(s * (s - a) * (s - b) * (s - c));
            System.out.println(result);
        } else {
            int result = -1;
            System.out.println(result);
        }
    }
}

```

### Súčet dvoch reálnych čísel 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double a = sc.nextDouble();
        double b = sc.nextDouble();

        double c = a + b;
        System.out.println(Math.round(c));
    }
}

```

### Obsah a obvod kruhu 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double pi = 3.14;
        double r = sc.nextDouble();
        double p = pi * 2 * r;
        double s = pi * r * r;
        System.out.print(Math.round(s));
        System.out.print(" ");
        System.out.print(Math.round(p));
    }
}

```

### Dokonalé číslo 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int number = scanner.nextInt();

        if (number <= 1) {
            System.out.println("false");
        } else {
            int sumOfDivisors = 1;

            for (int i = 2; i <= Math.sqrt(number); i++) {
                if (number % i == 0) {
                    if (i == (number / i)) {
                        sumOfDivisors += i;
                    } else {
                        sumOfDivisors += i + (number / i);
                    }
                }
            }

            if (sumOfDivisors == number) {
                System.out.println("true");
            } else {
                System.out.println("false");
            }
        }
    }
}

```

### Počet deliteľov zadaného čísla 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a = scanner.nextInt();
        int d = 0;

        for (int i = 1; i <= a; i++) {
            if (a % i == 0) {
                d++;
            }
        }
        System.out.println(d);
    }
}

```

### Počet bitov 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a = scanner.nextInt();

        int pocet = 0;

        while (a != 0) {
            pocet += a & 1;
            a >>= 1;
        }
        System.out.println(pocet);
    }
}

```

### Mince 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double a = scanner.nextDouble();

        int cents = (int) (a * 100 + 0.5);

        while (cents >= 200) {
            System.out.print("2€ ");
            cents -= 200;
        }
        while (cents >= 100) {
            System.out.print("1€ ");
            cents -= 100;
        }
        while (cents >= 50) {
            System.out.print("50c ");
            cents -= 50;
        }
        while (cents >= 20) {
            System.out.print("20c ");
            cents -= 20;
        }
        while (cents >= 10) {
            System.out.print("10c ");
            cents -= 10;
        }
        while (cents >= 5) {
            System.out.print("5c ");
            cents -= 5;
        }
        while (cents >= 2) {
            System.out.print("2c ");
            cents -= 2;
        }
        while (cents >= 1) {
            System.out.print("1c ");
            cents -= 1;
        }
    }
}

```

### BMI index 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double weight = scanner.nextDouble();
        double height = scanner.nextDouble();
        double bmi = weight / (height * height);
        if (bmi < 18.5) {
            System.out.println("podváha");
        } else if (bmi < 25) {
            System.out.println("normálna hmotnosť");
        } else if (bmi < 30) {
            System.out.println("nadváha");
        } else {
            System.out.println("obezita");
        }
    }
}

```

### Usporiadanie čísel 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a = scanner.nextInt();
        int b = scanner.nextInt();

        if (a > b) {
            System.out.println(a+" "+b);
        }
        else if (a < b) {
            System.out.println(b+" "+a);
        }
        else {
            System.out.println("Cisla su rovnake");
        }
    }
}

```

### Prvočíslo 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        
        boolean isPrime = true;
        if (n <= 1) {
            isPrime = false;
        } else {
            for (int i = 2; i <= Math.sqrt(n); i++) {
                if (n % i == 0) {
                    isPrime = false;
                    break;
                }
            }
        }
        System.out.println(isPrime);
    }
}

```

### Hodnota z intervalu 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();

        if (a > b) {
            int temp = a;
            a = b;
            b = temp;
        }

        if (c >= a && c <= b) {
            System.out.println("ano");
        }
        else {
            System.out.println("nie");
        }
    }
}

```

### Deň alebo noc 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int hour = sc.nextInt();
        int period = sc.nextInt();

        if ((hour >= 6 && period == 0) || (hour < 6 && period == 1)) {
            System.out.println("den");
        } else {
            System.out.println("noc");
        }
    }
}

```

## Ostatné údajové typy

### Porovnanie troch čísel (jedna podmienka) 
```java
import java.util.Scanner;
public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();

        if (a == b && b == c) {
            System.out.println("Su totozne");
        } else {
            System.out.println("Nie su totozne");
        }
    }
}
```

### Hexadecimálna hodnota 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        char input = scanner.next().charAt(0);
        int output = -1;

        if (input >= 'A' && input <= 'F') {
            output = input - 'A' + 10;
        } else if (input >= 'a' && input <= 'f') {
            output = input - 'a' + 10;
        } else if (input >= '0' && input <= '9') {
            output = input - '0';
        }

        System.out.println(output);
    }
}
```

### Písmeno alebo číslica? 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        char znak = scanner.next().charAt(0);

        if (znak >= '0' && znak <= '9') {
            System.out.println("cislica");
        } else if ((znak >= 'a' && znak <= 'z') || (znak >= 'A' && znak <= 'Z')) {
            System.out.println("pismeno");
        } else {
            System.out.println("iny znak");
        }
    }
}
```

### Typ trojuholníka 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double a = scanner.nextDouble();
        double b = scanner.nextDouble();
        double c = scanner.nextDouble();

        if (a + b <= c || a + c <= b || b + c <= a) {
            System.out.println(-1);
            return;
        }

        boolean rovnostranny = a == b && b == c;
        boolean rovnoramenny = a == b || b == c || a == c;
        boolean pravouhly = a * a + b * b == c * c ||
                a * a + c * c == b * b ||
                b * b + c * c == a * a;

        System.out.println(rovnostranny + " " + rovnoramenny + " " + pravouhly);
    }
}
```

## String I.

### Pozdrav 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String name = scanner.nextLine();

        System.out.println("Ahoj " + name);
    }
}
```

### Pozdrav II. 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String greeting = scanner.nextLine();
        String name = scanner.nextLine();
        String surname = scanner.nextLine();

        System.out.println(greeting + ", " + name + " " + surname);
    }
}
```

### Počet znakov v reťazci 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String retazec = scanner.nextLine();

        System.out.println(retazec.length());
    }
}
```

### Palindrom 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine();
        String reversed = "";
        for (int i = input.length() - 1; i >= 0; i--) {
            reversed += input.charAt(i);
        }
        boolean isPalindrome = input.equals(reversed);
        System.out.println(input + " " + reversed + " " + isPalindrome);
    }
}
```

## String II.

### Počet výskytov cifry 
```java
import java.util.Scanner;
public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine();
        int amount = 0;
        for (int i = 0; i < input.length(); i++) {
            if (input.charAt(i) == '3') {
                amount++;
            }
        }
        System.out.println(amount);
    }
}
```

### Výskyt nuly 
```java
import java.util.Scanner;
public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine();
        boolean flag = false;
        for (int i = 0; i < input.length(); i++) {
            if (input.charAt(i) == '0') {
                flag = true;
                break;
            }
        }
        if (flag) {
            System.out.println("Nula tu je");
        }
        else {
            System.out.println("Nula tu nie je");
        }
    }
}
```

### Ciferný súčet 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine();
        int sum = 0;
        for (int i = 0; i < input.length(); i++) {
            if (!(input.charAt(i) + "").equals("-")) {
                sum += Integer.parseInt(input.charAt(i) + "");
            }
        }
        System.out.println(sum);
    }
}

```

### Maximálna cifra 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine();
        char minus = '-';
        if (input.charAt(0) == minus) {
            input = input.substring(1);
        }
        int cur, max_int = 0;
        for (int i = 0; i < input.length(); i++) {
            cur = Integer.parseInt(input.substring(i, i+1));
            if (cur  > max_int) {
                max_int = cur;
            }
        }
        System.out.println(max_int);
    }
}

```

### Párne číslice v reťazci 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();
        int evenCount = 0;
        boolean hasZero = false;

        for (int i = 0; i < input.length(); i++) {
            char c = input.charAt(i);
            if (c >= '0' && c <= '9') {
                int digit = c - '0';
                if (digit % 2 == 0) {
                    evenCount++;
                }
                if (digit == 0) {
                    hasZero = true;
                }
            }
        }

        System.out.println("Pocet parnych: " + evenCount);
        if (hasZero) {
            System.out.println("Nula tu je");
        } else {
            System.out.println("Nula tu nie je");
        }
    }
}
```

### Oprava čísla 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();
        String result = "";

        for (int i = 0; i < input.length(); i++) {
            char c = input.charAt(i);
            if (c >= '0' && c <= '9') {
                result += c;
            } else {
                result += '1';
            }
        }

        System.out.println(result);
    }
}
```

### Triedenie 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int[] nums = new int[5];
        for (int i = 0; i < 5; i++) {
            if (!scanner.hasNextInt()) {
                System.out.println(-1);
                return;
            }
            nums[i] = scanner.nextInt();
        }
        if (scanner.hasNextInt()) {
            System.out.println(-1);
            return;
        }

        for (int i = 0; i < 5; i++) {
            for (int j = i + 1; j < 5; j++) {
                if (nums[i] > nums[j]) {
                    int tmp = nums[i];
                    nums[i] = nums[j];
                    nums[j] = tmp;
                }
            }
        }

        for (int i = 0; i < 5; i++) {
            System.out.print(nums[i] + " ");
        }
    }
}
```

### Porovnanie reťazcov 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String first = scanner.nextLine();
        String second = scanner.nextLine();

        if (first.equals(second)) {
            System.out.println("ano");
        } else {
            System.out.println("nie");
        }
    }
}
```

### Výpis samohlások 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();
        String samohlasky = "aeiouyAEIOUY";

        for (int i = 0; i<input.length(); i++) {
            for (int j = 0; j < samohlasky.length(); j++) {
                if (input.charAt(i) == samohlasky.charAt(j)) {
                    System.out.print(samohlasky.charAt(j));
                    break;
                }
            }
        }
    }
}
```

### Veľké písmena 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();

        for (int i = 0; i < input.length(); i++) {
            char currentChar = input.charAt(i);
            if (currentChar >= 'a' && currentChar <= 'z') {
                System.out.print((char) (currentChar - 32));
            } else {
                System.out.print(currentChar);
            }
        }
    }
}
```

### Znak v reťazci 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();
        char input_char = scanner.nextLine().charAt(0);
        boolean flag = false;

        for (int i = 0; i < input.length(); i++) {
            if (input.charAt(i) == input_char) {
                flag = true;
                break;
            }
        }
        if (flag) {
            System.out.println("Ano");
        } else {
            System.out.println("Nie");
        }
    }
}
```

### Zrkadlový obraz 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();

        for (int i = input.length()-1; i >=0; i--) {
            System.out.print(input.charAt(i));
        }
    }
}
```

### Výskyt a zámena 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();
        int count = 0;

        for (int i = 0; i < input.length(); i++) {
            if (input.charAt(i) == 'y') {
                count++;
                input = input.substring(0, i) + 'i' + input.substring(i + 1);
            }
        }
        System.out.println(count);
        System.out.println(input);
    }
}
```

### Inicálky 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String meno = scanner.nextLine();
        String priezvisko = scanner.nextLine();

        System.out.println(""+meno.charAt(0) + priezvisko.charAt(0));
    }
}
```

### Vymazanie číslic 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();
        String result = "";

        for (int i = 0; i < input.length(); i++) {
            char c = input.charAt(i);
            if (c >= '0' && c <= '9') {
                result += '-';
            } else {
                result += c;
            }
        }

        System.out.println(result);
    }
}
```

### Odstránenie medzier 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();
        String result = "";

        for (int i = 0; i < input.length(); i++) {
            char c = input.charAt(i);
            if (c != ' ') {
                result += c;
            }
        }

        System.out.println(result);
    }
}
```

### Zámena znaku s počítaním zmien 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();
        int count = 0;

        for (int i = 0; i < input.length(); i++) {
            if (input.charAt(i) == ';') {
                count++;
                input = input.substring(0, i) + ',' + input.substring(i + 1);
            }
        }
        System.out.print(count+ " ");
        System.out.println(input);
    }
}
```

### Počet výskytov podreťazca 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String substring = scanner.nextLine();
        String text = scanner.nextLine();
        int count = 0;
        int index = 0;

        while ((index = text.indexOf(substring, index)) != -1) {
            count++;
            index += substring.length();
        }

        System.out.println(count);
    }
}
```

### Vymazanie slov 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String text = scanner.nextLine();
        String substring = "ahoj";
        int index = 0;

        while ((index = text.indexOf(substring, index)) != -1) {
            text = text.substring(0, index)+text.substring(index+substring.length());
        }

        System.out.println(text);
    }
}
```

### Priemerná dĺžka slova 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine().trim();
        if (input.isEmpty()) {
            System.out.println("0.0");
            return;
        }
        int wordCount = 0;
        int totalLength = 0;
        int i = 0;
        int n = input.length();
        while (i < n) {
            while (i < n && input.charAt(i) == ' ') {
                i++;
            }
            if (i >= n) break;
            int start = i;
            while (i < n && input.charAt(i) != ' ') {
                i++;
            }
            int length = i - start;
            totalLength += length;
            wordCount++;
        }
        double average = (double) totalLength / wordCount;
        System.out.printf("%.1f%n", average);
    }
}
```

### Nuly a jednotky 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int countZero = 0;
        int countOne = 0;
        boolean validInput = true;

        while (validInput && scanner.hasNextInt()) {
            int number = scanner.nextInt();
            if (number == 0) {
                countZero++;
            } else if (number == 1) {
                countOne++;
            } else {
                validInput = false;
            }
        }

        System.out.println(countZero == countOne);
    }
}
```

### Nuly a jednotky II. 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();
        int count0 = 0;
        int count1 = 0;
        boolean flag = false;

        for (int i = 0; i < input.length(); i++) {
            if (input.charAt(i) == '0') {
                count0++;
            }
            else if (input.charAt(i) == '1') {
                count1++;
            }
            else if (input.charAt(i) != ' ') {
                flag = true;
                break;
            }
        }
        if (flag) {
            System.out.println("error");
        }
        else {
            System.out.println(count0 == count1);
        }
    }
}
```

### Dekompresia 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String vstup = scanner.nextLine();

        String rezultat = "";
        String[] casti = vstup.split(",");

        for (String cast : casti) {
            int i = 0;
            String cislo = "";

            while (i < cast.length() && Character.isDigit(cast.charAt(i))) {
                cislo += cast.charAt(i);
                i++;
            }

            if (i < cast.length()) {
                int pocet = Integer.parseInt(cislo);
                char znak = cast.charAt(i);

                for (int j = 0; j < pocet; j++) {
                    rezultat += znak;
                }
            } else {
                if (!cislo.isEmpty()) {
                    int pocet = Character.getNumericValue(cislo.charAt(0));

                    for (int k = 1; k < cislo.length(); k++) {
                        char znak = cislo.charAt(k);
                        for (int j = 0; j < pocet; j++) {
                            rezultat += znak;
                        }
                    }
                }
            }
        }

        System.out.println(rezultat);
    }
}
```

## Vnorené cykly a efektívnosť

### Postupnosť číslic 
```java
public class JavaApp {
    public static void main(String[] args) {
        for (int i = 1; i < 10; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print(i);
            }
            System.out.println();
        }
    }
}
```

### Obdĺžnik z hviezdičiek 
```java
import java.util.Scanner;
public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int m = sc.nextInt();
        int n = sc.nextInt();

        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print("x");
            }
            System.out.println();
        }
    }
}
```

### Trojuholník z hviezdičiek 
```java
import java.util.Scanner;
public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        for (int i = 1; i <= n; i++) {
            for (int j = 0; j < i; j++) {
                System.out.print("x");
            }
            System.out.println();
        }
    }
}
```

### Geometrická postupnosť z hviezdičiek 
```java
import java.util.Scanner;
public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        String s = "x";
        for (int i = 0; i < n; i++) {
            System.out.println(s);
            s += s;
        }
    }
}
```

### Rám obdĺžnika z hviezdičiek 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int m = scanner.nextInt();
        int n = scanner.nextInt();

        for (int i = 1; i <= m; i++) {
            for (int j = 1; j <= n; j++) {
                if (i == 1 || i == m || j == 1 || j == n) {
                    System.out.print(" x");
                } else {
                    System.out.print("  ");
                }
            }
            System.out.println();
        }
    }
}
```

### Opačný trojuholník z hviezdičiek 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        for (int i = 1; i <= n; i++) {
            for (int j = 0; j < n - i; j++) {
                System.out.print(" ");
            }
            for (int j = 0; j < i; j++) {
                System.out.print("x");
            }
            System.out.println();
        }
    }
}
```

### Výpis do štvorca 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int count = 1;

        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                System.out.printf("%4d", count++);
            }
            System.out.println();
        }
    }
}
```

### Medián slov 
```java
import java.util.*;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String line = sc.nextLine();
        
        // Count words
        int wordCount = 0;
        boolean inWord = false;
        for (int i = 0; i < line.length(); i++) {
            if (line.charAt(i) != ' ') {
                if (!inWord) {
                    wordCount++;
                    inWord = true;
                }
            } else {
                inWord = false;
            }
        }

        // Allocate array
        String[] words = new String[wordCount];

        // Fill array
        inWord = false;
        int wordIndex = 0;
        int start = 0;

        for (int i = 0; i < line.length(); i++) {
            if (line.charAt(i) != ' ') {
                if (!inWord) {
                    start = i;
                    inWord = true;
                }
            } else {
                if (inWord) {
                    words[wordIndex++] = line.substring(start, i);
                    inWord = false;
                }
            }
        }

        if (inWord) {
            words[wordIndex] = line.substring(start);
        }

        // Sort manually (bubble sort)
        for (int i = 0; i < words.length - 1; i++) {
            for (int j = i + 1; j < words.length; j++) {
                if (words[i].compareTo(words[j]) > 0) {
                    String tmp = words[i];
                    words[i] = words[j];
                    words[j] = tmp;
                }
            }
        }

        // Print median
        System.out.println(words[words.length / 2]);
    }
}
```

### Medián dĺžok slov 
```java
public class JavaApp {
    public static void main(String[] args) {
        java.util.Scanner sc = new java.util.Scanner(System.in);
        String input = sc.nextLine().trim();
        String[] words = input.split(" ");

        int n = words.length;
        if (n == 0) {
            System.out.println("error");
            return;
        }

        int[] lengths = new int[n];

        for (int i = 0; i < n; i++) {
            lengths[i] = words[i].length();
        }

        boolean allSame = true;
        if (n > 1) {
            for (int i = 1; i < n; i++) {
                if (lengths[i] != lengths[0]) {
                    allSame = false;
                    break;
                }
            }
            if (allSame) {
                System.out.println("error");
                return;
            }
        }

        for (int i = 0; i < n - 1; i++) {
            for (int j = i + 1; j < n; j++) {
                if (lengths[i] > lengths[j]) {
                    int tempLength = lengths[i];
                    lengths[i] = lengths[j];
                    lengths[j] = tempLength;

                    String tempWord = words[i];
                    words[i] = words[j];
                    words[j] = tempWord;
                }
            }
        }

        int medianLength;
        if (n % 2 == 1) {
            medianLength = lengths[n / 2];
        } else {
            medianLength = (lengths[n / 2 - 1] + lengths[n / 2]) / 2;
        }

        for (String word : words) {
            if (word.length() == medianLength) {
                System.out.println(word);
                return;
            }
        }
    }
}
```

### Komprimácia 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();
        int count = 1;
        for (int i = 0; i < input.length(); i++) {
            if (i + 1 < input.length() && input.charAt(i) == input.charAt(i + 1)) {
                count++;
            } else {
                System.out.print(input.charAt(i) + ":" + count + " ");
                count = 1;
            }
        }
    }
}
```

### Malá násobilka 
```java
public class JavaApp {
    public static void main(String[] args) {
        for (int i = 1; i <= 10; i++) {
            for (int j = 1; j <= 10; j++) {
                System.out.printf("%4d", i * j);
            }
            System.out.println();
        }
    }
}
```

### Znak s najväčším výskytom 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine();
        char mostFrequentChar = ' ';
        int maxCount = 0;

        for (char currentChar = 'a'; currentChar <= 'z'; currentChar++) {
            int count = 0;
            for (int i = 0; i < input.length(); i++) {
                if (input.charAt(i) == currentChar) {
                    count++;
                }
            }
            if (count > maxCount) {
                mostFrequentChar = currentChar;
                maxCount = count;
            }
        }

        System.out.println(mostFrequentChar);
    }
}
```

### Súčet čísel v reťazci 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine();
        int sum = 0;
        int currentNumber = 0;

        for (int i = 0; i < input.length(); i++) {
            char c = input.charAt(i);
            if (c >= '0' && c <= '9') {
                currentNumber = currentNumber * 10 + (c - '0');
            } else {
                sum += currentNumber;
                currentNumber = 0;
            }
        }

        sum += currentNumber;

        System.out.println(sum);
    }
}
```

### Vykrátenie zlomku 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int d = sc.nextInt();
        int a = n;
        int b = d;

        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }

        int gcd = a;
        int sn = n / gcd;
        int sd = d / gcd;

        System.out.println(sn + "/" + sd);
    }
}
```

### Prvočísla od 2 po n 
```java
import java.util.Scanner;
public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        for (int i = 2; i <= n; i++) {
            boolean isPrime = true;
            for (int j = 2; j * j <= i; j++) {
                if (i % j == 0) {
                    isPrime = false;
                    break;
                }
            }
            if (isPrime) {
                System.out.println(i);
            }
        }
    }
}
```

### Mocnina 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        long result = 1;

        for (int i = 0; i < n; i++) {
            result = result * n;
        }
        System.out.println(result);
    }
}
```

### Hviezdičky 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner vstup = new Scanner(System.in);
        int n = vstup.nextInt();
        String hviezdy = "";
        for(int i=0; i<n; i++) {
            hviezdy += "x";
        }
        System.out.println(hviezdy);
    }
}
```

### Delitele 
```java
import java.util.Scanner;

public class JavaApp {

    public static void main(String[] args) {
        Scanner vstup = new Scanner(System.in);
        int a = vstup.nextInt();
        int pocet = 0;
        int i = a;
        while (i > 0) {
            if ((a % i) == 0) {
                pocet = pocet + 1;
                System.out.print(i);
            }
            i = i - 1;
        }
        System.out.println();
        System.out.println(pocet);
    }

}

```

### Faktoriál 
```java
import java.util.Scanner;

public class JavaApp {

    public static void main(String[] args) {
        Scanner vstup = new Scanner(System.in);
        int n = vstup.nextInt();
        long faktorial = 1;
        for(int i = n; i>0; i--)
            faktorial = faktorial * i;
        System.out.println(faktorial);
    }
}

```

### Mocnina II 
```java
import java.util.Scanner;

public class JavaApp {

    public static void main(String[] args) {
        Scanner vstup = new Scanner(System.in);
        int a = vstup.nextInt();
        int b = vstup.nextInt();
        long mocnina = 1;

        for(int i = 0; i < b; i++)
            mocnina = mocnina * a;

        System.out.println(mocnina);
    }
}
```

### Súčet cifier 
```java
import java.util.Scanner;

public class JavaApp {

    public static void main(String[] args) {
        Scanner vstup = new Scanner(System.in);
        int c, n = vstup.nextInt();
        int sucet = 0;

        while (n != 0) {
            c = n % 10;
            sucet = sucet + c;
            n = n / 10;
        }

        System.out.println(sucet);
    }
}
```

### Odstránenie medzier 
```java
import java.util.Scanner;

public class JavaApp {

    public static void main(String[] args) {
        Scanner vstup = new Scanner(System.in);
        String retazec = vstup.nextLine();

        while (retazec.contains(" ")) {
            int pozicia = retazec.indexOf(" ");
            retazec = retazec.substring(0, pozicia) + retazec.substring(pozicia + 1);
        }
        System.out.println(retazec);
    }
}
```

### Palindrom 
```java
import java.util.Scanner;

public class JavaApp {

    public static void main(String[] args) {
        Scanner vstup = new Scanner(System.in); 
        String retazec = vstup.nextLine();

        retazec = retazec.toLowerCase().replaceAll("\\s+", ""); // Odstránenie medzier

        String odzadu = "";
        for (int i = retazec.length() - 1; i >= 0; i--) {
            odzadu = odzadu + retazec.charAt(i);
        }

        if (retazec.equals(odzadu)) 
            System.out.println("Je palindrom");
        else 
            System.out.println("Nie je palindrom");
    }
}
```

### Trojuholník 
```java
import java.util.Scanner;

public class JavaApp {

    public static void main(String[] args) {
        Scanner vstup = new Scanner(System.in);
        int n = vstup.nextInt();

        String riadok = "";
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= n; j++) {
                if (j <= (n - i))
                    riadok = riadok + " ";
                else
                    riadok = riadok + "x";
            }
            System.out.println(riadok);
            riadok = "";
        }
    }
}

```

### Zrkadlo 
```java
import java.util.Scanner;

public class JavaApp {

    public static void main(String[] args) {
        Scanner vstup = new Scanner(System.in);
        String retazec = vstup.nextLine();
        String zrkadlo = ""; // do premennej vložíme prázdny reťazec

        // Prechádzame reťazcom od konca na začiatok
        for (int i = retazec.length() - 1; i >= 0; i--) {
            zrkadlo = zrkadlo + retazec.charAt(i); // pridávame znaky od konca
        }

        System.out.println(zrkadlo);
    }
}
```

## Viacnásobné vetvenie

### Počet párnych cifier 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();
        int count0 = 0, count2 = 0, count4 = 0, count6 = 0, count8 = 0;

        for (int i = 0; i < input.length(); i++) {
            char c = input.charAt(i);
            switch (c) {
                case '0': count0++; break;
                case '2': count2++; break;
                case '4': count4++; break;
                case '6': count6++; break;
                case '8': count8++; break;
            }
        }

        System.out.println("0-" + count0 + " 2-" + count2 + " 4-" + count4 + " 6-" + count6 + " 8-" + count8);
    }
}
```

### Počet dní v mesiaci (číselný vstup) 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int number = scanner.nextInt();

        switch (number) {
            case 1: System.out.println(31); break;
            case 2: System.out.println(28); break;
            case 3: System.out.println(31); break;
            case 4: System.out.println(30); break;
            case 5: System.out.println(31); break;
            case 6: System.out.println(30); break;
            case 7: System.out.println(31); break;
            case 8: System.out.println(31); break;
            case 9: System.out.println(30); break;
            case 10: System.out.println(31); break;
            case 11: System.out.println(30); break;
            case 12: System.out.println(31); break;
            default: System.out.println("Neplatny mesiac");
        }
    }
}
```

### Počet dní v mesiaci (slovný vstup) 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();

        switch (input) {
            case "januar":
            case "marec":
            case "maj":
            case "jul":
            case "august":
            case "oktober":
            case "december":
                System.out.println(31);
                break;
            case "april":
            case "jun":
            case "september":
            case "november":
                System.out.println(30);
                break;
            case "februar":
                System.out.println(28);
                break;
            default:
                System.out.println("Nepostojeci mesec");
                break;
        }
    }
}
```

### Kalkulačka 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        char action = sc.nextLine().charAt(0);
        int a = sc.nextInt();
        int b = sc.nextInt();

        switch (action) {
            case '+':
                System.out.println(a + b);
                break;
            case '-':
                System.out.println(a - b);
                break;
            case '*':
                System.out.println(a * b);
                break;
            case '/':
                System.out.println(a / b);
                break;
        }
    }
}
```

### Ročné obdobia 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int number = scanner.nextInt();

        switch (number) {
            case 12:
            case 1:
            case 2: System.out.println("ZIMA"); break;
            case 3:
            case 4:
            case 5: System.out.println("JAR"); break;
            case 6:
            case 7:
            case 8: System.out.println("LETO"); break;
            case 9:
            case 10:
            case 11: System.out.println("JESEN"); break;
            default: System.out.println("Neplatny mesiac");
        }
    }
}
```

### Počet zostávajúcich dní v mesiaci 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int day = scanner.nextInt();
        int month = scanner.nextInt();
        int total_month = 0;

        switch (month) {
            case 1: case 3: case 5: case 7: case 8: case 10: case 12: total_month = 31; break;
            case 4: case 6: case 9: case 11: total_month = 30; break;
            case 2: total_month = 28; break;
        }

        System.out.println(total_month-day);
    }
}
```

### Vekové kategórie 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int vek = scanner.nextInt();
        int kategoria = 0;

        if (vek >= 0 && vek <= 11) kategoria = 1;
        else if (vek >= 12 && vek <= 18) kategoria = 2;
        else if (vek >= 19 && vek <= 35) kategoria = 3;
        else if (vek >= 36 && vek <= 60) kategoria = 4;
        else if (vek >= 61 && vek <= 99) kategoria = 5;

        switch (kategoria) {
            case 1:
                System.out.println("dieta");
                break;
            case 2:
                System.out.println("teeneger");
                break;
            case 3:
                System.out.println("mlady dospely");
                break;
            case 4:
                System.out.println("dospely");
                break;
            case 5:
                System.out.println("stary clovek");
                break;
            default:
                System.out.println("neplatny vek");
        }
    }
}
```

### Hex Digits 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        char znak = scanner.next().charAt(0);
        int hodnota = -1;

        switch (znak) {
            case '0': hodnota = 0; break;
            case '1': hodnota = 1; break;
            case '2': hodnota = 2; break;
            case '3': hodnota = 3; break;
            case '4': hodnota = 4; break;
            case '5': hodnota = 5; break;
            case '6': hodnota = 6; break;
            case '7': hodnota = 7; break;
            case '8': hodnota = 8; break;
            case '9': hodnota = 9; break;
            case 'A': case 'a': hodnota = 10; break;
            case 'B': case 'b': hodnota = 11; break;
            case 'C': case 'c': hodnota = 12; break;
            case 'D': case 'd': hodnota = 13; break;
            case 'E': case 'e': hodnota = 14; break;
            case 'F': case 'f': hodnota = 15; break;
        }

        System.out.println(hodnota);
    }
}
```

### Výpis samohlások 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();

        for (int i = 0; i < str.length(); i++) {
            switch (str.charAt(i)) {
                case 'a': case 'e': case 'i': case 'y': case 'o': case 'u':
                    case 'A': case 'E': case 'I': case 'Y': case 'O': case 'U':
                        System.out.print(str.charAt(i));
                        break;
            }
        }
    }
}
```

### Výpis bez samohlások 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();

        for (int i = 0; i < str.length(); i++) {
            switch (str.charAt(i)) {
                case 'a': case 'e': case 'i': case 'y': case 'o': case 'u':
                    case 'A': case 'E': case 'I': case 'Y': case 'O': case 'U':
                        break;
                default:
                    System.out.print(str.charAt(i));
            }
        }
    }
}
```

### Malé a veľké písmená 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String retazec = scanner.nextLine();
        int male = 0, velke = 0, cislice = 0;

        for (int i = 0; i < retazec.length(); i++) {
            char znak = retazec.charAt(i);
            switch (znak) {
                case 'a': case 'b': case 'c': case 'd': case 'e': case 'f':
                case 'g': case 'h': case 'i': case 'j': case 'k': case 'l':
                case 'm': case 'n': case 'o': case 'p': case 'q': case 'r':
                case 's': case 't': case 'u': case 'v': case 'w': case 'x':
                case 'y': case 'z':
                    male++;
                    break;
                case 'A': case 'B': case 'C': case 'D': case 'E': case 'F':
                case 'G': case 'H': case 'I': case 'J': case 'K': case 'L':
                case 'M': case 'N': case 'O': case 'P': case 'Q': case 'R':
                case 'S': case 'T': case 'U': case 'V': case 'W': case 'X':
                case 'Y': case 'Z':
                    velke++;
                    break;
                case '0': case '1': case '2': case '3': case '4':
                case '5': case '6': case '7': case '8': case '9':
                    cislice++;
                    break;
                default:
                    // Ignore other characters
                    break;
            }
        }

        System.out.println("male-" + male + " velke-" + velke + " cislice-" + cislice);
    }
}
```

## Výnimky

### Správne zadanie číselnej hodnoty 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        try {
            int value = Integer.parseInt(scanner.nextLine());
            System.out.println("OK");
        } catch (NumberFormatException e) {
            System.out.println("Exception");
        }
    }
}
```

### Ošetrenie delenia nulou 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a = scanner.nextInt();
        int b = scanner.nextInt();

        if (b == 0) {
            System.out.println("Delenie nulou");
            return;
        }

        try {
            double result = (double) a / b;
            System.out.println((int) result);
        } catch (ArithmeticException e) {
            System.out.println("Delenie nulou");
        }
    }
}
```

### Chybuvzdorné sčítavanie 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String firstInput = scanner.nextLine();
        String secondInput = scanner.nextLine();

        int firstNumber, secondNumber;

        try {
            firstNumber = Integer.parseInt(firstInput);
        } catch (NumberFormatException e) {
            System.out.println("1. cislo je nekorektne");
            return;
        }

        try {
            secondNumber = Integer.parseInt(secondInput);
        } catch (NumberFormatException e) {
            System.out.println("2. cislo je nekorektne");
            return;
        }

        System.out.println(firstNumber + secondNumber);
    }
}

```

### Výpis pozície s chybou 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();
        int inputNumber;
        boolean isNegative = false;

        try {
            inputNumber = Integer.parseInt(input);
        } catch (NumberFormatException e) {
            if (input.charAt(0) == '-') {
                input = input.substring(1);
                isNegative = true;
            }
            for (int i = 0; i < input.length(); i++) {
                try {
                    Integer.parseInt(String.valueOf(input.charAt(i)));
                } catch (NumberFormatException e2) {
                    if (isNegative) {
                        System.out.println("chyba na pozicii " + (i + 1));
                    } else {
                        System.out.println("chyba na pozicii " + i);
                    }
                    return;
                }
            }
        }

        System.out.println("OK");
    }
}

```

## Polia

### Náhodné číslo z intervalu 0 až 100 
```java
public class JavaApp {

    public static void main(String[] args) {
        System.out.println((int) (Math.random() * 100));
    }
}
    
```

### Náhodné číslo z intervalu -50 až 50 
```java
public class JavaApp {

    public static void main(String[] args) {
        System.out.println(-50 + (int) (Math.random() * 101));
    }
}
```

### Náhodné číslo zo zadaného intervalu 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a = scanner.nextInt();
        int b = scanner.nextInt();
        int min = Math.min(a, b);
        int max = Math.max(a, b);
        int randomNum = min + (int)(Math.random() * (max - min + 1));
        System.out.println(randomNum);
    }
}
```

### Najväčší prvok v poli 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = scanner.nextInt();
        }
        int max = arr[0];
        for (int i = 1; i < n; i++) {
            if (arr[i] > max) {
                max = arr[i];
            }
        }
        System.out.println(max);
    }
}
```

### Pozícia najmenšieho prvku v poli 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = scanner.nextInt();
        }
        int minIndex = 0;
        for (int i = 1; i < n; i++) {
            if (arr[i] < arr[minIndex]) {
                minIndex = i;
            }
        }
        System.out.println(minIndex);
    }
}
```

### Počet výskytov zadanej hodnoty v poli 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int n = scanner.nextInt();
        int[] array = new int[n];

        for (int i = 0; i < n; i++) {
            array[i] = scanner.nextInt();
        }

        int target = scanner.nextInt();
        int count = 0;

        for (int i = 0; i < n; i++) {
            if (array[i] == target) {
                count++;
            }
        }

        System.out.println(count);
    }
}
```

### Počet kladných a záporných hodnôt v poli 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int n = scanner.nextInt();
        int[] array = new int[n];

        int input;
        int index = 0;
        for (int i = 0; i < n; i++) {
            input = scanner.nextInt();
            if (input != 0) {
                array[index] = input;
                index++;
            }
        }
        int kladnych = 0, zapornych = 0;
        for (int i = 0; i < n; i++) {
            if (array[i] > 0) {
                kladnych++;
            } else if (array[i] < 0) {
                zapornych++;
            }
        }
        System.out.println("kladných: "+kladnych);
        System.out.println("záporných: "+zapornych);
    }
}
```

### Výpis čísel deliteľných zadanou hodnotou 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = scanner.nextInt();
        }
        int num = scanner.nextInt();
        boolean flag = false;
        for (int i = 0; i < n; i++) {
            if ((arr[i] % num)==0) {
                if (flag) {
                    System.out.print(',');
                }
                flag = true;
                System.out.print(arr[i]);
            }
        }
        if (flag) {
            System.out.println('.');
        } else {
            System.out.println("Žiadny prvok deliteľný zadanou hodnotou");
        }
    }
}
```

### Rozdiel najväčšieho a najmenšieho prvku v poli 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = scanner.nextInt();
        }
        int max = arr[0];
        int min = arr[0];
        for (int i = 0; i < n; i++) {
            if (arr[i] > max) {
                max = arr[i];
            }
            if (arr[i] < min) {
                min = arr[i];
            }
        }
        System.out.println(max - min);
    }
}
```

### Prvé a druhé najväčšie číslo v poli 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int[] arr = new int[n];

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        int largest = arr[0];
        int secondLargest = arr[0];

        for (int i = 1; i < n; i++) {
            if (arr[i] > largest) {
                secondLargest = largest;
                largest = arr[i];
            } else if (arr[i] > secondLargest || largest == secondLargest) {
                secondLargest = arr[i];
            }
        }

        System.out.println(largest + "," + secondLargest);
    }
}
```

### Počet nadpriemerných a podpriemerných prvkov 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int[] arr = new int[n];

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        int sum = 0;

        for (int i = 0; i < n; i++) {
            sum += arr[i];
        }
        int avg = sum / n;

        int nadpriemer = 0;
        int podpriemer = 0;
        for (int i = 0; i < n; i++) {
            if (arr[i] > avg) {
                nadpriemer++;
            } else if (arr[i] < avg) {
                podpriemer++;
            }
        }
        System.out.println("nadpriemer: " + nadpriemer);
        System.out.println("podpriemer: " + podpriemer);
    }
}
```

### Výskyt deliteľných čísel 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int input;
        int counter = 0;

        for (int i = 0; i < 10; i++) {
            input = sc.nextInt();
            if (input % 8 == 0) {
                counter++;
            }
        }
        System.out.println(counter);
    }
}
```

### MinMax 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int count = scanner.nextInt();

        if (count <= 0) {
            return;
        }

        int first = scanner.nextInt();
        int min = first;
        int max = first;

        for (int i = 1; i < count; i++) {
            int num = scanner.nextInt();
            if (num < min) {
                min = num;
            }
            if (num > max) {
                max = num;
            }
        }

        System.out.println(min + " " + max);
    }
}
```

### Stredná hodnota 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int sum = 0;
        long product = 1;
        int count = 0;
        int num = scanner.nextInt();

        while (num != 999999) {
            sum += num;
            product *= num;
            count++;
            num = scanner.nextInt();
        }

        int arithmeticMean = Math.round((float) sum / count);
        int geometricMean = Math.round((float) Math.pow(product, 1.0 / count));

        System.out.println(arithmeticMean + " " + geometricMean);
    }
}
```

## Práca s poľom

### Rozdelenie poľa na párne a nepárne prvky 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int count = scanner.nextInt();
        int[] input = new int[count];
        int parneCount = 0;
        int neparneCount = 0;

        for (int i = 0; i < count; i++) {
            input[i] = scanner.nextInt();
            if (input[i] % 2 == 0) {
                parneCount++;
            } else {
                neparneCount++;
            }
        }

        int[] parne = new int[parneCount];
        int[] neparne = new int[neparneCount];
        int parneIndex = 0;
        int neparneIndex = 0;

        for (int num : input) {
            if (num % 2 == 0) {
                parne[parneIndex++] = num;
            } else {
                neparne[neparneIndex++] = num;
            }
        }

        System.out.print("parne:");
        for (int num : parne) {
            System.out.print(" " + num);
        }
        System.out.println();

        System.out.print("neparne:");
        for (int num : neparne) {
            System.out.print(" " + num);
        }
        System.out.println();
    }
}
```

### Pole párnych hodnôt 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int[] original = new int[10];
        int evenCount = 0;

        for (int i = 0; i < 10; i++) {
            original[i] = scanner.nextInt();
            if (original[i] % 2 == 0) {
                evenCount++;
            }
        }

        int[] evenNumbers = new int[evenCount];
        int index = 0;

        for (int num : original) {
            if (num % 2 == 0) {
                evenNumbers[index++] = num;
            }
        }

        for (int i = 0; i < evenNumbers.length; i++) {
            if (i > 0) {
                System.out.print(" ");
            }
            System.out.print(evenNumbers[i]);
        }
    }
}
```

### Výpis pozícií pre zadanú hodnotu 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        int searchElement = sc.nextInt();
        for (int i = 0; i < n; i++) {
            if (arr[i] == searchElement) {
                System.out.println(i);
            }
        }
    }
}
```

### Zámena prvku v poli 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String[] arr = new String[5];

        for (int i = 0; i < 5; i++) {
            arr[i] = sc.nextLine();
        }

        int index = Integer.parseInt(sc.nextLine());
        String repl = sc.nextLine();

        arr[index-1] = repl;

        for (int i = 0; i < 5; i++) {
            System.out.println(arr[i]);
        }
    }
}
```

### Mazanie v poli 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String[] arr = new String[5];

        for (int i = 0; i < 5; i++) {
            arr[i] = sc.nextLine();
        }

        int index = Integer.parseInt(sc.nextLine());
        for (int i = 0; i < arr.length; i++) {
            if (i != index-1) {
                System.out.println(arr[i]);
            }
        }
    }
}
```

### Zrkadlo 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int[] arr = new int[5];

        for (int i = 0; i < 5; i++) {
            arr[5-i-1] = sc.nextInt();
        }
        for (int i = 0; i < 5; i++) {
            System.out.print(arr[i] + " ");
        }
    }
}
```

### Postupnosť 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int[] arr = new int[20];
        arr[0] = sc.nextInt();
        arr[1] = sc.nextInt();
        for (int i = 2; i < 20; i++) {
            arr[i] = arr[i - 1] + arr[i - 2];
        }
        for (int i = 0; i < 20; i++) {
            System.out.print(arr[i] + " ");
        }
    }
}
```

### Zoznam mien 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = Integer.parseInt(sc.nextLine());
        String[] arr = new String[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextLine();
        }
        char symb = sc.nextLine().charAt(0);
        for (int i = 0; i < n; i++) {
            if (arr[i].charAt(0) == symb) {
                System.out.print(arr[i]+" ");
            }
        }
    }
}
```

### Druhé najväčšie číslo 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int[] arr = new int[10];

        for (int i = 0; i < 10; i++) {
            arr[i] = sc.nextInt();
        }

        int largest = arr[0];
        int secondLargest = arr[0];

        for (int i = 0; i < 10; i++) {
            if (arr[i] > largest) {
                secondLargest = largest;
                largest = arr[i];
            } else if (arr[i] > secondLargest && arr[i] != largest) {
                secondLargest = arr[i];
            }
        }

        System.out.println(secondLargest);
    }
}
```

### Počet znakov 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();

        for (int i = 0; i < input.length(); i++) {
            char c = input.charAt(i);
            if (!((c >= 'a' && c <= 'z') || (c >= 'A' && c <= 'Z') || (c >= '0' && c <= '9'))) {
                System.out.println("Error");
                return;
            }
        }

        int[] counts = new int[256];

        for (int i = 0; i < input.length(); i++) {
            char c = input.charAt(i);
            counts[c]++;
        }

        for (int i = 0; i < counts.length; i++) {
            if (counts[i] > 0) {
                System.out.print((char)i + ":" + counts[i] + " ");
            }
        }
    }
}
```

### Početnosť jednotlivých čísel 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[] array = new int[n];
        for (int i = 0; i < n; i++) {
            array[i] = scanner.nextInt();
        }

        int[] unique = new int[n];
        int[] counts = new int[n];
        int uniqueCount = 0;

        for (int i = 0; i < n; i++) {
            boolean found = false;
            for (int j = 0; j < uniqueCount; j++) {
                if (unique[j] == array[i]) {
                    counts[j]++;
                    found = true;
                    break;
                }
            }
            if (!found) {
                unique[uniqueCount] = array[i];
                counts[uniqueCount] = 1;
                uniqueCount++;
            }
        }

        for (int i = 0; i < uniqueCount; i++) {
            System.out.println((i+1) + ". " + unique[i] + ": " + counts[i]);
        }
    }
}
```

### Výskyt cifier 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String number = sc.nextLine();
        int[] arr = new int[10];
        for (int i = 0; i < number.length(); i++) {
            int digit = Integer.parseInt(number.charAt(i)+"");
            arr[digit]++;
        }
        for (int i = 0; i < 10; i++) {
            System.out.println(i + " - " + arr[i]);
        }
    }
}
```

### Kontrola vkladania a minimum 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int[] arr = new int[5];
        for (int i = 0; i < 5; i++) {
            try {
                int number = sc.nextInt();
                arr[i] = number;
            } catch (Exception e) {
                System.out.println("Zoznam obsahuje nekorektnú hodnotu, neuvažujeme ju.");
                sc.next();
                arr[i] = 999999;
            }
        }
        int min = arr[0];
        for (int i = 1; i < 5; i++) {
            if (arr[i] < min) {
                min = arr[i];
            }
        }
        System.out.println(min);
    }
}
```

### Počet výskytov písmen 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine().toLowerCase();
        int[] counts = new int[26];

        for (int i = 0; i < input.length(); i++) {
            char c = input.charAt(i);
            if (c >= 'a' && c <= 'z') {
                counts[c - 'a']++;
            }
        }

        for (int i = 0; i < 26; i++) {
            if (counts[i] > 0) {
                System.out.println((char)('a' + i) + " - " + counts[i]);
            }
        }
    }
}
```

### Priemerná dĺžka slova 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine();
        String[] words = input.split(" ");

        String shortest = words[0];
        String longest = words[0];
        int totalLength = 0;

        for (int i = 0; i < words.length; i++) {
            String word = words[i];
            if (word.length() < shortest.length()) {
                shortest = word;
            }
            if (word.length() > longest.length()) {
                longest = word;
            }
            totalLength += word.length();
        }

        double average = (double) totalLength / words.length;
        System.out.printf("%s %s %.2f", shortest, longest, average);
    }
}
```

### Odstránenie prvočísel z poľa 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] input = new int[n];
        for (int i = 0; i < n; i++) {
            input[i] = sc.nextInt();
        }

        int count = 0;
        for (int i = 0; i < input.length; i++) {
            int num = input[i];
            if (num <= 1) {
                count++;
                continue;
            }
            boolean isPrime = true;
            for (int j = 2; j * j <= num; j++) {
                if (num % j == 0) {
                    isPrime = false;
                    break;
                }
            }
            if (!isPrime) count++;
        }

        int[] output = new int[count];
        int index = 0;
        for (int num : input) {
            if (num <= 1) {
                output[index++] = num;
                continue;
            }
            boolean isPrime = true;
            for (int i = 2; i * i <= num; i++) {
                if (num % i == 0) {
                    isPrime = false;
                    break;
                }
            }
            if (!isPrime) output[index++] = num;
        }

        for (int i = 0; i < output.length; i++) {
            System.out.print(output[i] + " ");
        }
    }
}
```

### Medián 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String line = sc.nextLine().trim();
        String[] parts = line.split("\\s+");

        if (parts.length == 0) {
            System.out.println("Error");
            return;
        }

        int n = Integer.parseInt(parts[0]);

        if (n <= 0) {
            System.out.println("Error");
            return;
        }

        int[] arr = new int[n];

        for (int i = 1; i < parts.length && i <= n; i++) {
            arr[i - 1] = Integer.parseInt(parts[i]);
        }

        for (int i = 0; i < n; i++) {
            for (int j = i + 1; j < n; j++) {
                if (arr[i] > arr[j]) {
                    int temp = arr[i];
                    arr[i] = arr[j];
                    arr[j] = temp;
                }
            }
        }

        boolean hasDuplicates = false;
        for (int i = 0; i < n - 1; i++) {
            if (arr[i] == arr[i + 1]) {
                hasDuplicates = true;
                break;
            }
        }

        if (hasDuplicates) {
            System.out.println("Error");
        } else {
            if (n % 2 == 1) {
                System.out.println(arr[n / 2]);
            } else {
                System.out.println(arr[(n / 2) - 1]);
            }
        }
    }
}
```

### Usporiadanie poľa (čísel) 
```java
import java.util.Scanner;
import java.util.Arrays;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[] numbers = new int[n];
        for (int i = 0; i < n; i++) {
            numbers[i] = scanner.nextInt();
        }
        Arrays.sort(numbers);
        for (int i = 0; i < n; i++) {
            System.out.print(numbers[i]);
            if (i < n - 1) {
                System.out.print(',');
            }
            else {
                System.out.println('.');
            }
        }
    }
}
```

### Rozdelenie a usporiadanie 
```java
import java.util.Scanner;
import java.util.Arrays;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[] input = new int[n];
        for (int i = 0; i < n; i++) {
            input[i] = scanner.nextInt();
        }

        int positiveCount = 0;
        int negativeCount = 0;
        for (int i = 0; i < n; i++) {
            if (input[i] > 0) positiveCount++;
            else if (input[i] < 0) negativeCount++;
        }

        int[] positive = new int[positiveCount];
        int[] negative = new int[negativeCount];
        int posIndex = 0;
        int negIndex = 0;
        for (int i = 0; i < n; i++) {
            if (input[i] > 0) {
                positive[posIndex++] = input[i];
            } else if (input[i] < 0) {
                negative[negIndex++] = input[i];
            }
        }

        Arrays.sort(positive);
        Arrays.sort(negative);

        for (int i = 0; i < positiveCount; i++) {
            System.out.print(positive[i] + " ");
        }
        System.out.println();

        for (int i = negativeCount - 1; i >= 0; i--) {
            System.out.print(negative[i] + " ");
        }
    }
}
```

### Usporiadanie poľa (textov) 
```java
import java.util.Scanner;
import java.util.Arrays;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = Integer.parseInt(scanner.nextLine());
        String[] words = new String[n];
        for (int i = 0; i < n; i++) {
            words[i] = scanner.nextLine();
        }
        Arrays.sort(words);
        for (int i = 0; i < n; i++) {
            System.out.println(words[i]);
        }
    }
}
```

### Zostupné poradie reťazcov 
```java
import java.util.Arrays;
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String input = scanner.nextLine();
        String[] words = input.split(" ");

        Arrays.sort(words);

        for (int i = 0; i < words.length / 2; i++) {
            String temp = words[i];
            words[i] = words[words.length - 1 - i];
            words[words.length - 1 - i] = temp;
        }

        for (int i = 0; i < words.length; i++) {
            System.out.print(words[i]+" ");
        }
    }
}
```

### Je pole usporiadané? 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        boolean flag = false;
        for (int i = 0; i < n-1; i++) {
            if (arr[i] > arr[i + 1]) {
                System.out.println("Nie");
                flag = true;
                return;
            }
        }
        if (!flag) {
            System.out.println("Ano");
        }
    }
}
```

### Zoradenie poľa podľa dĺžky a abecedy 
```java
import java.util.*;

public class JavaApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String[] words = sc.nextLine().split(" ");

        for (int i = 0; i < words.length - 1; i++) {
            int minIndex = i;
            for (int j = i + 1; j < words.length; j++) {
                if (words[j].length() < words[minIndex].length()) {
                    minIndex = j;
                } else if (words[j].length() == words[minIndex].length()) {
                    if (words[j].compareTo(words[minIndex]) < 0) {
                        minIndex = j;
                    }
                }
            }

            String temp = words[minIndex];
            words[minIndex] = words[i];
            words[i] = temp;
        }

        System.out.println(String.join(" ", words));
    }
}
```

## Matice

### Párne a nepárne hodnoty 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int[][] matrix = new int[2][4];

        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 4; j++) {
                matrix[i][j] = scanner.nextInt();
            }
        }

        int parne = 0;
        int neparne = 0;

        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 4; j++) {
                if (matrix[i][j] % 2 == 0) {
                    parne++;
                } else {
                    neparne++;
                }
            }
        }

        if (parne > neparne) {
            System.out.println("parnych " + parne);
        } else if (neparne > parne) {
            System.out.println("neparnych " + neparne);
        } else {
            System.out.println("rovnako");
        }
    }
}
```

### Vynulovanie hodnôt pod hlavnou diagonálou 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int[][] matrix = new int[3][3];

        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                matrix[i][j] = scanner.nextInt();
            }
        }

        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                if (i > j) {
                    matrix[i][j] = 0;
                }
            }
        }

        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                System.out.printf("%4d", matrix[i][j]);
            }
            System.out.println();
        }
    }
}
```

### Štvorec 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[][] matrix = new int[n][n];
        int num = 1;

        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                matrix[i][j] = num++;
            }
        }

        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                System.out.printf("%4d", matrix[i][j]);
            }
            System.out.println();
        }
    }
}
```

### Súčet diagonál 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[][] matrix = new int[n][n];

        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                matrix[i][j] = scanner.nextInt();
            }
        }

        int sum1 = 0;
        int sum2 = 0;

        for (int i = 0; i < n; i++) {
            sum1 += matrix[i][i];
            sum2 += matrix[i][n - 1 - i];
        }

        System.out.println(sum1 + " " + sum2);
    }
}
```

### Hľadanie v matici celých čísel 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int rows = scanner.nextInt();
        int cols = scanner.nextInt();
        int[][] matrix = new int[rows][cols];
        
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                matrix[i][j] = scanner.nextInt();
            }
        }
        
        int target = scanner.nextInt();
        boolean found = false;
        int foundRow = -1;
        int foundCol = -1;
        
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                if (matrix[i][j] == target) {
                    found = true;
                    foundRow = i;
                    foundCol = j;
                    break;
                }
            }
            if (found) break;
        }
        
        if (found) {
            System.out.println("najdeny na pozicii " + foundRow + " " + foundCol);
        } else {
            System.out.println("nenajdeny");
        }
    }
}
```

### Symetrická matica 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[][] matrix = new int[n][n];
        
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                matrix[i][j] = scanner.nextInt();
            }
        }
        
        boolean symmetric = true;
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                if (matrix[i][j] != matrix[j][i]) {
                    symmetric = false;
                    break;
                }
            }
            if (!symmetric) break;
        }
        
        System.out.println(symmetric);
    }
}
```

### Zrkadlová matica 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[][] matrix = new int[n][n];
        
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                matrix[i][j] = scanner.nextInt();
            }
        }
        
        for (int i = 0; i < n; i++) {
            for (int j = n - 1; j >= 0; j--) {
                System.out.print(matrix[i][j] + " ");
            }
            System.out.println();
        }
    }
}
```

### Súčet pozície vs. prvok 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int cols = scanner.nextInt();
        int rows = scanner.nextInt();
        int[][] matrix = new int[rows][cols];
        int count = 0;

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                matrix[i][j] = scanner.nextInt();
                if (matrix[i][j] == i + j) {
                    count++;
                }
            }
        }

        System.out.println(count);
    }
}
```

### Zoradená matica s celými číslami 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int rows = scanner.nextInt();
        int cols = scanner.nextInt();
        int[][] matrix = new int[rows][cols];
        
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                matrix[i][j] = scanner.nextInt();
            }
        }

        boolean sorted = true;
        
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                if (i == 0 && j == 0) {
                    continue;
                }

                int previousRow = i;
                int previousCol = j - 1;

                if (j == 0) {
                    previousRow = i - 1;
                    previousCol = cols - 1;
                }

                if (matrix[i][j] < matrix[previousRow][previousCol]) {
                    sorted = false;
                    break;
                }
            }
            if (!sorted) {
                break;
            }
        }

        if (sorted) {
            System.out.println("zoradene");
        } else {
            System.out.println("nezoradene");
        }
    }
}
```

### Zoradená matica s reťazcami 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int rows = scanner.nextInt();
        int cols = scanner.nextInt();
        String[][] matrix = new String[rows][cols];
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                matrix[i][j] = scanner.next();
            }
        }
        boolean sorted = true;

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols - 1; j++) {
                if (matrix[i][j].compareTo(matrix[i][j + 1]) < 0) {
                    sorted = false;
                    break;
                }
            }
            if (!sorted) {
                break;
            }
        }

        if (sorted) {
            for (int j = 0; j < cols; j++) {
                for (int i = 0; i < rows - 1; i++) {
                    if (matrix[i][j].compareTo(matrix[i + 1][j]) < 0) {
                        sorted = false;
                        break;
                    }
                }
                if (!sorted) {
                    break;
                }
            }
        }

        if (sorted) {
            System.out.println("zoradena");
        } else {
            System.out.println("nezoradena");
        }
    }
}
```

### Vyhľadávanie v matici reťazcov 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int rows = scanner.nextInt();
        int cols = scanner.nextInt();
        String[][] matrix = new String[rows][cols];
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                matrix[i][j] = scanner.next();
            }
        }
        String target = scanner.next();
        boolean found = false;
        int x = -1;
        int y = -1;

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                if (matrix[i][j].equals(target)) {
                    found = true;
                    x = i;
                    y = j;
                    break;
                }
            }
            if (found) {
                break;
            }
        }

        if (found) {
            System.out.println("najdeny na pozicii " + x + " " + y);
        } else {
            System.out.println("nenajdeny");
        }
    }
}
```

### Vyhľadávanie v tabuľke 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String[][] data = new String[3][3];

        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                data[i][j] = scanner.nextLine();
            }
        }

        String target = scanner.nextLine();
        boolean found = false;

        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                if (data[i][j].equals(target)) {
                    System.out.println(data[i][0] + " " + data[i][1] + " " + data[i][2]);
                    found = true;
                    break;
                }
            }
        }

        if (!found) {
            System.out.println("Ziadna zhoda");
        }
    }
}
```

### Zmazanie riadku 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String[][] data = new String[3][3];

        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                data[i][j] = scanner.nextLine();
            }
        }

        int rowToRemove = Integer.parseInt(scanner.nextLine()) - 1;

        for (int i = 0; i < 3; i++) {
            if (i != rowToRemove) {
                System.out.println(data[i][0] + " " + data[i][1] + " " + data[i][2]);
            }
        }
    }
}
```

### Vyhľadávanie znaku v matici 
```java
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int rows = scanner.nextInt();
        int cols = scanner.nextInt();
        String[][] matrix = new String[rows][cols];

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                matrix[i][j] = scanner.next();
            }
        }

        char target = scanner.next().charAt(0);
        int count = 0;

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                String word = matrix[i][j];
                for (int k = 0; k < word.length(); k++) {
                    if (Character.toLowerCase(word.charAt(k)) == Character.toLowerCase(target)) {
                        count++;
                    }
                }
            }
        }

        System.out.println(count);
    }
}
```

### Usporiadanie výskytov znakov 
```java
class JavaApp {
    public static void main(String[] args) {
        java.util.Scanner sc = new java.util.Scanner(System.in);
        String input = sc.nextLine();
        int[] count = new int[256];
        for (int i = 0; i < input.length(); i++) {
            count[input.charAt(i)]++;
        }

        String result = "";
        boolean first = true;
        while (true) {
            int max = -1;
            char ch = 0;
            for (int i = 0; i < 256; i++) {
                if (count[i] > max) {
                    max = count[i];
                    ch = (char) i;
                }
            }
            if (max == 0) break;
            if (first) {
                result += ch + ":" + max;
                first = false;
            } else {
                result += " " + ch + ":" + max;
            }
            count[ch] = 0;
        }
        System.out.println(result);
    }
}
```

## Súbory

### Čítanie zo súboru 
```java
import java.io.File;
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);
        String fileName = sc.nextLine();
        Scanner fileScanner = new Scanner(new File(fileName));
        int[] array = new int[10];
        for (int i = 0; i < 10; i++) {
            array[i] = fileScanner.nextInt();
        }
        for (int num : array) {
            System.out.println(num);
        }
    }
}
```

### Prvý a posledný žiak 
```java
import java.io.*;
import java.util.*;

public class JavaApp {
    public static void main(String[] args) throws IOException {
        Scanner scanner = new Scanner(System.in);
        String fileName = scanner.nextLine();
        scanner.close();

        BufferedReader reader = new BufferedReader(new FileReader(fileName));
        String first = null;
        String last = null;
        String line;
        while ((line = reader.readLine()) != null) {
            if (line.trim().length() > 0) {
                if (first == null) {
                    first = line.trim();
                }
                last = line.trim();
            }
        }
        reader.close();

        if (first != null) {
            System.out.println(first);
            System.out.println(last);
        }
    }
}
```

### Mená začínajúce s písmenom B 
```java
import java.io.*;
import java.util.*;

public class JavaApp {
    public static void main(String[] args) throws IOException {
        Scanner scanner = new Scanner(System.in);
        String fileName = scanner.nextLine();
        scanner.close();

        BufferedReader reader = new BufferedReader(new FileReader(fileName));
        String line;
        while ((line = reader.readLine()) != null) {
            if (line.charAt(0) == 'B') {
                System.out.println(line);
            }
        }
        reader.close();
    }
}
```

### Vyznamenaní študenti 
```java
import java.io.*;
import java.util.*;

public class JavaApp {
    public static void main(String[] args) throws IOException {
        Scanner scanner = new Scanner(System.in);
        String file1 = scanner.nextLine();
        String file2 = scanner.nextLine();

        BufferedReader reader1 = new BufferedReader(new FileReader(file1));
        String line;
        while ((line = reader1.readLine()) != null) {
            int semicolon = line.indexOf(';');
            if (semicolon > 0) {
                String name = line.substring(0, semicolon).trim();
                String gradeStr = line.substring(semicolon + 1).trim().replace(',', '.');
                try {
                    double grade = Double.parseDouble(gradeStr);
                    if (grade <= 1.5) {
                        System.out.println(name);
                    }
                } catch (NumberFormatException e) {}
            }
        }
        reader1.close();

        BufferedReader reader2 = new BufferedReader(new FileReader(file2));
        while ((line = reader2.readLine()) != null) {
            int semicolon = line.indexOf(';');
            if (semicolon > 0) {
                String name = line.substring(0, semicolon).trim();
                String gradeStr = line.substring(semicolon + 1).trim().replace(',', '.');
                try {
                    double grade = Double.parseDouble(gradeStr);
                    if (grade <= 1.5) {
                        System.out.println(name);
                    }
                } catch (NumberFormatException e) {}
            }
        }
        reader2.close();
    }
}
```

### Počet znakov, riadkov, viet a slov 
```java
import java.io.*;
import java.util.*;

public class JavaApp {
    public static void main(String[] args) throws IOException {
        Scanner scanner = new Scanner(System.in);
        String fileName = scanner.nextLine();
        scanner.close();

        BufferedReader reader = new BufferedReader(new FileReader(fileName));
        int chars = 0;
        int lines = 0;
        int sentences = 0;
        int words = 0;
        String line;

        while ((line = reader.readLine()) != null) {
            lines++;
            chars += line.length();
            boolean inWord = false;

            for (int i = 0; i < line.length(); i++) {
                char c = line.charAt(i);
                if (c == '.' || c == '?' || c == '!') {
                    sentences++;
                }
                if (c == ' ') {
                    if (inWord) {
                        words++;
                        inWord = false;
                    }
                } else {
                    inWord = true;
                }
            }
            if (inWord) {
                words++;
            }
        }
        reader.close();

        System.out.println("znakov: " + chars + " riadkov: " + lines +
                " viet: " + sentences + " slov: " + words);
    }
}
```

### Vymeškané hodiny - max 
```java
import java.io.*;
import java.util.*;

public class JavaApp {
    public static void main(String[] args) throws IOException {
        Scanner scanner = new Scanner(System.in);
        String file1 = scanner.nextLine();

        BufferedReader reader = new BufferedReader(new FileReader(file1));
        String line;
        int max = 0;
        String maxName = "";
        while ((line = reader.readLine()) != null) {
            int devider = line.indexOf(':');
            if (devider > 0) {
                String name = line.substring(0, devider).trim();
                String vymeskanych = line.substring(devider + 1).trim().replace(',', '.');
                try {
                    int index = Integer.parseInt(vymeskanych);
                    if (index > max) {
                        max = index;
                        maxName = name;
                    }
                } catch (NumberFormatException e) {}
            }
        }
        reader.close();
        System.out.println(maxName);
    }
}
```

### Vymeškané hodiny - výpočty 
```java
import java.io.*;
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) throws IOException {
      	Scanner scanner = new Scanner(System.in);
        String fileName = scanner.nextLine();
        FileReader fr = new FileReader(fileName);
        BufferedReader br = new BufferedReader(fr);
        String line;
        int count = 0;
        int total = 0;
        while ((line = br.readLine()) != null) {
            String[] parts = line.split(":");
            int hours = Integer.parseInt(parts[1]);
            total += hours;
            count++;
        }
        br.close();
        double average = (double) total / count;
        System.out.println(count);
        System.out.println(total);
        System.out.printf("%.1f\n", average);
    }
}
```

### Prvý a posledný podľa abecedy 
```java
import java.io.*;
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) throws IOException {
        Scanner scanner = new Scanner(System.in);
        String fileName = scanner.nextLine();

        FileReader fr = new FileReader(fileName);
        BufferedReader br = new BufferedReader(fr);

        String[] names = new String[10];
        int count = 0;

        String line;
        while ((line = br.readLine()) != null && count < 10) {
            names[count] = line;
            count++;
        }

        br.close();

        for (int i = 0; i < count - 1; i++) {
            for (int j = i + 1; j < count; j++) {
                if (names[i].compareTo(names[j]) > 0) {
                    String temp = names[i];
                    names[i] = names[j];
                    names[j] = temp;
                }
            }
        }

        if (count > 0) {
            System.out.println(names[0]);
            System.out.println(names[count - 1]);
        }
    }
}
```

### Najdlhšie meno 
```java
import java.io.*;
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) throws IOException {
        Scanner scanner = new Scanner(System.in);
        String fileName = scanner.nextLine();

        FileReader fr = new FileReader(fileName);
        BufferedReader br = new BufferedReader(fr);

        String[] names = new String[10];
        int count = 0;

        String line;
        while ((line = br.readLine()) != null && count < 10) {
            names[count] = line.trim();
            count++;
        }

        br.close();

        String longest = names[0];
        for (int i = 1; i < count; i++) {
            if (names[i].length() > longest.length()) {
                longest = names[i];
            }
        }

        System.out.println(longest);
    }
}
```

### Zrkadlo 
```java
import java.io.*;
import java.util.Scanner;

public class JavaApp {
    public static void main(String[] args) throws IOException {
        Scanner scanner = new Scanner(System.in);
        String fileName = scanner.nextLine();

        FileReader fr = new FileReader(fileName);
        BufferedReader br = new BufferedReader(fr);

        String[] names = new String[10];
        int count = 0;

        String line;
        while ((line = br.readLine()) != null && count < 10) {
            names[count] = line;
            count++;
        }

        br.close();

        for (int i = count-1; i >= 0; i--) {
            System.out.println(names[i]);
        }
    }
}
```