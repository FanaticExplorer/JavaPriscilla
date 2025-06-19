# Zoznam účastníkov 

## Množina (Set)

### Zoznam účastníkov 

```java
import java.util.Scanner;
import java.util.HashSet;

public class JavaApp {
    
    public static void main(String[] args) {
        HashSet<String> mySet = new HashSet<String>();
        Scanner scanner = new Scanner(System.in);
        
        while (true) {
            String input = scanner.nextLine();
            if (input.equals("0")) {
                break;
            }
            mySet.add(input);
        }
        
        System.out.println(mySet);
    }
}
```

### Jednoduchý zoznam 

```java
import java.util.Scanner;
import java.util.TreeSet;

public class JavaApp {
    
    public static void main(String[] args) {
        TreeSet<Integer> mySet = new TreeSet<Integer>();
        Scanner scanner = new Scanner(System.in);
        
        while (true) {
            int num = scanner.nextInt();
            if (num == 0) {
                break;
            }
            mySet.add(num);
        }
        
        System.out.println(mySet.toString().replace("[", "[ ").replace(",", ","));
        
        TreeSet<Integer> oddSet = new TreeSet<Integer>();
        for (int num : mySet) {
            if (num % 2 != 0) {
                oddSet.add(num);
            }
        }
        
        System.out.println(oddSet.toString().replace("[", "[ ").replace(",", ","));
    }
}
```

### Osoby v objekte (ID) 

```java
import java.util.Scanner;
import java.util.HashSet;

public class JavaApp {

    public static void main(String[] args) {
        HashSet<Integer> zoznam = new HashSet<>();
        Scanner scanner = new Scanner(System.in);

        int n = scanner.nextInt();

        for (int i = 0; i < n; i++) {
            int operacia = scanner.nextInt();
            int cislo = scanner.nextInt();

            if (operacia == 1) {
                zoznam.add(cislo);
            } else if (operacia == 0) {
                if (!zoznam.remove(cislo)) {
                    System.out.println("NARUSENIE " + cislo);
                }
            }
        }

        System.out.println(zoznam);
    }
}
```

### Osoby v objekte (priezvisko) 

```java
import java.util.Scanner;
import java.util.TreeSet;

public class JavaApp {
    public static void main(String[] args) {
        TreeSet<String> osoby = new TreeSet<>();
        Scanner scanner = new Scanner(System.in);

        int n = Integer.parseInt(scanner.nextLine().trim());

        for (int i = 0; i < n; i++) {
            String line = scanner.nextLine();
            String[] parts = line.split("\\s+");
            String operation = parts[0];
            String surname = parts[1].trim();

            if (operation.equals("1")) {
                osoby.add(surname);
            } else if (operation.equals("0")) {
                if (osoby.contains(surname)) {
                    osoby.remove(surname);
                } else {
                    System.out.println("NARUSENIE " + surname);
                }
            }
        }

        System.out.println(osoby);
    }
}
```

### Generátor slov 

```java
import java.util.Scanner;
import java.util.TreeSet;

public class JavaApp {

    public static void main(String[] args) {
        TreeSet<Character> uniqueLetters = new TreeSet<>();
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();

        for (int i = 0; i < input.length(); i++) {
            char c = input.charAt(i);
            if (c >= 'A' && c <= 'Z') {
                uniqueLetters.add(c);
            }
        }

        char[] letters = new char[uniqueLetters.size()];
        int index = 0;
        for (char c : uniqueLetters) {
            letters[index++] = c;
        }

        TreeSet<String> words = new TreeSet<>();
        for (int i = 0; i < letters.length; i++) {
            for (int j = 0; j < letters.length; j++) {
                if (j == i) continue;
                for (int k = 0; k < letters.length; k++) {
                    if (k == i || k == j) continue;
                    words.add("" + letters[i] + letters[j] + letters[k]);
                }
            }
        }

        System.out.println(words);
    }
}
```

## Mapa (Map)

### Zoznam obyvateľov 

```java
import java.util.Scanner;
import java.util.HashMap;
import java.util.TreeMap;

public class JavaApp {
    
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        HashMap<Integer, String> residents = new HashMap<>();
        
        while (true) {
            String input = scanner.nextLine();
            if (input.equals("0")) {
                break;
            }
            
            int houseNumber = Integer.parseInt(input);
            String name = scanner.nextLine();
            residents.put(houseNumber, name);
        }
        System.out.println(residents);
    }
}
```

### Slovník 

```java
import java.util.Scanner;
import java.util.HashMap;

public class JavaApp {
    
    public static void main(String[] args) {
        HashMap<String, String> dictionary = new HashMap<>();
        Scanner scanner = new Scanner(System.in);
        
        while (true) {
            String word = scanner.nextLine();
            if (word.equals("0")) {
                break;
            }
            String translation = scanner.nextLine();
            dictionary.put(word, translation);
        }
        
        while (true) {
            String wordToTranslate = scanner.nextLine();
            if (wordToTranslate.equals("0")) {
                break;
            }
            String translated = dictionary.get(wordToTranslate);
            if (translated != null) {
                System.out.println(translated);
            } else {
                System.out.println("x");
            }
        }
        
        scanner.close();
    }
}
```

### Hlavné mestá I. 

```java
import java.util.Scanner;
import java.util.TreeMap;
import java.util.Map;

public class JavaApp {
    
    public static void main(String[] args) {
        Map<String, String> capitals = new TreeMap<>();
        Scanner scanner = new Scanner(System.in);
        
        while (true) {
            String country = scanner.nextLine();
            if (country.equals("0")) {
                break;
            }
            String capital = scanner.nextLine();
            capitals.put(country, capital);
        }
        
        while (true) {
            String query = scanner.nextLine();
            if (query.equals("0")) {
                break;
            }
            if (capitals.containsKey(query)) {
                System.out.println(capitals.get(query));
            } else {
                System.out.println("x");
            }
        }
        
        System.out.println(capitals);
        
        scanner.close();
    }
}
```

### Hlavné mestá II. 

```java
import java.util.Scanner;
import java.util.TreeMap;

public class JavaApp {
    
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        TreeMap<String, String> countryToCapital = new TreeMap<>();
        while (true) {
            String country = scanner.nextLine();
            if (country.equals("0")) {
                break;
            }
            String capital = scanner.nextLine();
            countryToCapital.put(country, capital);
        }
        
        System.out.println(countryToCapital);
        
        TreeMap<String, String> capitalToCountry = new TreeMap<>();
        for (String country : countryToCapital.keySet()) {
            String capital = countryToCapital.get(country);
            capitalToCountry.put(capital, country);
        }
        
        while (true) {
            String city = scanner.nextLine();
            if (city.equals("0")) {
                break;
            }
            if (capitalToCountry.containsKey(city)) {
                System.out.println(capitalToCountry.get(city));
            } else {
                System.out.println("x");
            }
        }
        
        System.out.println(capitalToCountry);
    }
}
```

### Požičovňa áut 

```java
import java.util.HashMap;
import java.util.HashSet;
import java.util.Scanner;

public class JavaApp {

    public static void main(String[] args) {
        HashMap<String, String> rentedCars = new HashMap<>();
        HashSet<String> rentedECVs = new HashSet<>();

        Scanner scanner = new Scanner(System.in);
        int operations = scanner.nextInt();
        scanner.nextLine();

        for (int i = 0; i < operations; i++) {
            String line = scanner.nextLine();
            String[] parts = line.split(" ");

            int operation = Integer.parseInt(parts[0]);
            String ecv = parts[1];

            switch (operation) {
                case 1:
                    if (rentedECVs.contains(ecv)) {
                        System.out.println("OBSADENE");
                    } else {
                        String person = parts[2];
                        rentedCars.put(ecv, person);
                        rentedECVs.add(ecv);
                    }
                    break;
                case 2:
                    if (rentedECVs.contains(ecv)) {
                        System.out.println("ANO");
                    } else {
                        System.out.println("NIE");
                    }
                    break;
                case 0:
                    if (rentedECVs.contains(ecv)) {
                        rentedCars.remove(ecv);
                        rentedECVs.remove(ecv);
                    }
                    break;
            }
        }
    }
}
```

### Manipulácia so slovníkom 

```java
import java.util.HashMap;
import java.util.Scanner;

public class JavaApp {
    
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        HashMap<String, String> dictionary = new HashMap<>();
        
        while (true) {
            int operation = scanner.nextInt();
            if (operation == 0) {
                break;
            }
            
            if (operation == 1) {
                String englishWord = scanner.next();
                String slovakWord = scanner.next();
                dictionary.put(englishWord, slovakWord);
            } else if (operation == 2) {
                String englishWord = scanner.next();
                String translation;
                if (dictionary.containsKey(englishWord)) {
                    translation = dictionary.get(englishWord);
                } else {
                    translation = "x";
                }
                System.out.println(translation);
            }
        }
        
        scanner.close();
    }
}
```

## Rekurzia

### Faktoriál 

```java
import java.util.Scanner;

public class JavaApp {

    public static long faktorial(int n) {
        if (n < 0) {
            return -1;
        }
        if (n == 0 || n == 1) {
            return 1;
        }
        return n * faktorial(n - 1);
    }

    public static void main(String[] args) {
        Scanner vstup = new Scanner(System.in);
        int n = vstup.nextInt();

        long result = faktorial(n);

        if (result == -1) {
            System.out.println("neexistuje");
        } else {
            System.out.println(result);
        }
    }
}
```

### Mocnina 

```java
import java.util.Scanner;

public class JavaApp {
    
    public static double mocnina(double a, int n) {
        if (n == 0) {
            return 1;
        }
        if (n < 0) {
            return 1 / mocnina(a, -n);
        }
        return a * mocnina(a, n - 1);
    }

    public static void main(String[] args) {
        Scanner vstup = new Scanner(System.in);
        double a = vstup.nextDouble();
        int n = vstup.nextInt();
        
        double result = mocnina(a, n);
        
        if (result == (long) result) {
            System.out.println((long) result);
        } else {
            System.out.println(result);
        }
    }
}
```

### Fibonacciho číslo 

```java
import java.util.Scanner;

public class JavaApp {
    
    public static int fib(int n) {
        if (n <= 1) {
            return n;
        }
        return fib(n - 1) + fib(n - 2);
    }

    public static void main(String[] args) {
        Scanner vstup = new Scanner(System.in);
        int n = vstup.nextInt();
        
        int result = fib(n);
        
        System.out.println(result);
    }
}
```

### Prvočíslo 

```java
import java.util.Scanner;

public class JavaApp {
    
    public static String prvocislo(int n, int delitel) {
        if (n <= 1) {
            return "nie";
        }
        if (n == 2) {
            return "ano";
        }
        if (delitel * delitel > n) {
            return "ano";
        }
        if (n % delitel == 0) {
            return "nie";
        }
        return prvocislo(n, delitel + 1);
    }

    public static void main(String[] args) {
        Scanner vstup = new Scanner(System.in);
        int cislo = vstup.nextInt();
        String vysledok = prvocislo(cislo, 2);
        System.out.println(vysledok);
    }
}
```

### Postupnosť 

```java
import java.util.Scanner;

public class JavaApp {
    
    public static int postupnost(int n) {
        if (n == 1) {
            return 2;
        } else if (n == 2) {
            return 3;
        } else {
            return postupnost(n-1) + postupnost(n-2);
        }
    }

    public static void main(String[] args) {
        Scanner vstup = new Scanner(System.in);
        int n = vstup.nextInt();
        int result = postupnost(n);
        System.out.println(result);
    }
}
```

### Súčet čísiel 

```java
import java.util.Scanner;

public class JavaApp {
    
    public static int sucet(int n) {
        if (n == 0) {
            return 0;
        }
        return n + sucet(n - 1);
    }

    public static void main(String[] args) {
        Scanner vstup = new Scanner(System.in);
        int n = vstup.nextInt();
        int vysledok = sucet(n);
        System.out.println(vysledok);
    }
}
```

## Bludisko

### Rozmery bludiska 

```java
import java.io.BufferedReader;
import java.io.FileReader;
import java.util.Scanner;

public class JavaApp {
    
    public static void main(String[] args) throws Exception {
        Scanner vstup = new Scanner(System.in);
        String fileName = vstup.nextLine();
        
        BufferedReader reader = new BufferedReader(new FileReader(fileName));
        
        int height = 0;
        int width = 0;
        String line;
        
        while ((line = reader.readLine()) != null) {
            if (height == 0) {
                width = line.length();
            }
            height++;
        }
        
        System.out.println(width + " x " + height);
        reader.close();
    }
}
```

### Typ miestnosti 

```java
import java.io.BufferedReader;
import java.io.FileReader;
import java.util.ArrayList;
import java.util.Scanner;

public class JavaApp {

    public static void main(String[] args) throws Exception {
        Scanner scanner = new Scanner(System.in);
        String fileName = scanner.nextLine();
        BufferedReader reader = new BufferedReader(new FileReader(fileName));
        ArrayList<String> maze = new ArrayList<>();
        String line;
        while ((line = reader.readLine()) != null) {
            maze.add(line);
        }
        reader.close();

        ArrayList<String> results = new ArrayList<>();
        while (true) {
            String input = scanner.nextLine();
            if (input.equals("-1,-1")) break;

            String[] parts = input.split(",");
            int row = Integer.parseInt(parts[0]);
            int col = Integer.parseInt(parts[1]);

            if (row < 0 || col < 0 || row >= maze.size() || col >= maze.get(0).length()) {
                results.add("mimo");
                continue;
            }

            char cell = maze.get(row).charAt(col);
            if (cell == 'x') {
                results.add("stena");
            } else {
                results.add("volno");
            }
        }

        String output = "";
        for (int i = 0; i < results.size(); i++) {
            if (i > 0) {
                output += ",";
            }
            output += results.get(i);
        }
        System.out.println(output);
    }
}
```

### Priama cesta 

```java
import java.io.BufferedReader;
import java.io.FileReader;
import java.util.Scanner;
import java.util.ArrayList;
import java.util.List;

public class JavaApp {
    public static void main(String[] args) throws Exception {
        Scanner vstup = new Scanner(System.in);
        String fileName = vstup.nextLine().trim();

        List<String> maze = new ArrayList<>();
        BufferedReader reader = new BufferedReader(new FileReader(fileName));
        String line;
        while ((line = reader.readLine()) != null) {
            maze.add(line);
        }
        reader.close();

        List<List<String>> paths = new ArrayList<>();
        if (!maze.isEmpty()) {
            int rows = maze.size();
            int cols = maze.get(0).length();

            for (int col = 0; col < cols; col++) {
                if (maze.get(0).charAt(col) == ' ') {
                    List<String> path = new ArrayList<>();
                    boolean valid = true;

                    for (int row = 0; row < rows; row++) {
                        if (col >= maze.get(row).length() || maze.get(row).charAt(col) != ' ') {
                            valid = false;
                            break;
                        }
                        path.add(row + "," + col);
                    }

                    if (valid) {
                        paths.add(path);
                    }
                }
            }
        }

        System.out.println(paths.size());
        for (List<String> path : paths) {
            String result = "";
            for (int i = 0; i < path.size(); i++) {
                if (i > 0) result += " ";
                result += path.get(i);
            }
            System.out.println(result);
        }
    }
}
```

### Cesta? 

```java
import java.util.Scanner;
import java.io.FileReader;
import java.io.BufferedReader;
import java.util.ArrayList;
import java.util.List;

public class JavaApp {

    private static boolean dfs(char[][] maze, boolean[][] visited, int x, int y, int endX, int endY) {
        if (x < 0 || x >= maze.length || y < 0 || y >= maze[0].length || maze[x][y] == 'x' || visited[x][y]) {
            return false;
        }

        if (x == endX && y == endY) {
            return true;
        }

        visited[x][y] = true;

        return dfs(maze, visited, x + 1, y, endX, endY) ||
                dfs(maze, visited, x - 1, y, endX, endY) ||
                dfs(maze, visited, x, y + 1, endX, endY) ||
                dfs(maze, visited, x, y - 1, endX, endY);
    }

    public static void main(String[] args) throws Exception {
        Scanner vstup = new Scanner(System.in);
        String fileName = vstup.nextLine();

        BufferedReader reader = new BufferedReader(new FileReader(fileName));
        List<String> lines = new ArrayList<>();
        String line;

        while ((line = reader.readLine()) != null) {
            lines.add(line);
        }
        reader.close();

        if (lines.isEmpty()) {
            System.out.println("chybný súbor");
            return;
        }

        int rows = lines.size();
        int cols = lines.get(0).length();
        char[][] maze = new char[rows][cols];

        List<int[]> oPositions = new ArrayList<>();

        for (int i = 0; i < rows; i++) {
            String currentLine = lines.get(i);
            if (currentLine.length() != cols) {
                System.out.println("chybný súbor");
                return;
            }

            for (int j = 0; j < cols; j++) {
                maze[i][j] = currentLine.charAt(j);
                if (maze[i][j] == 'o') {
                    oPositions.add(new int[]{i, j});
                }
            }
        }

        if (oPositions.size() != 2) {
            System.out.println("chybný súbor");
            return;
        }

        int[] start = oPositions.get(0);
        int[] end = oPositions.get(1);

        boolean[][] visited = new boolean[rows][cols];
        boolean pathExists = dfs(maze, visited, start[0], start[1], end[0], end[1]);

        if (pathExists) {
            System.out.println("áno");
        } else {
            System.out.println("nie");
        }
    }
}
```

### Najkratšia cesta v bludisku 

```java
import java.util.Scanner;
import java.io.FileReader;
import java.io.BufferedReader;
import java.util.LinkedList;
import java.util.List;

public class JavaApp {

    private static int findShortestPath(char[][] maze, int[] start, int[] end) {
        int rows = maze.length;
        int cols = maze[0].length;
        boolean[][] visited = new boolean[rows][cols];
        int[][] directions = {{1, 0}, {-1, 0}, {0, 1}, {0, -1}};

        LinkedList<int[]> toVisit = new LinkedList<>();
        toVisit.add(new int[]{start[0], start[1], 0});
        visited[start[0]][start[1]] = true;

        while (!toVisit.isEmpty()) {
            int[] current = toVisit.removeFirst();
            int x = current[0];
            int y = current[1];
            int steps = current[2];

            if (x == end[0] && y == end[1]) {
                return steps;
            }

            for (int[] dir : directions) {
                int newX = x + dir[0];
                int newY = y + dir[1];

                if (newX >= 0 && newX < rows && newY >= 0 && newY < cols
                        && maze[newX][newY] != 'x' && !visited[newX][newY]) {
                    visited[newX][newY] = true;
                    toVisit.add(new int[]{newX, newY, steps + 1});
                }
            }
        }

        return -1;
    }

    public static void main(String[] args) throws Exception {
        Scanner vstup = new Scanner(System.in);
        String fileName = vstup.nextLine().trim();

        BufferedReader reader = new BufferedReader(new FileReader(fileName));
        List<String> lines = new LinkedList<>();
        String line;
        while ((line = reader.readLine()) != null) {
            lines.add(line);
        }
        reader.close();

        if (lines.isEmpty()) {
            System.out.println("chybný súbor");
            return;
        }

        int rows = lines.size();
        int cols = lines.get(0).length();
        char[][] maze = new char[rows][cols];
        int[] start = null;
        int[] end = null;

        for (int i = 0; i < rows; i++) {
            String currentLine = lines.get(i);
            if (currentLine.length() != cols) {
                System.out.println("chybný súbor");
                return;
            }

            for (int j = 0; j < cols; j++) {
                maze[i][j] = currentLine.charAt(j);
                if (maze[i][j] == 'o') {
                    if (start == null) {
                        start = new int[]{i, j};
                    } else if (end == null) {
                        end = new int[]{i, j};
                    }
                }
            }
        }

        if (start == null || end == null) {
            System.out.println("chybný súbor");
            return;
        }

        int result = findShortestPath(maze, start, end);
        System.out.println(result != -1 ? result : "neexistuje");
    }
}
```

### Oddelené priestory 

```java
import java.util.Scanner;
import java.io.FileReader;
import java.io.BufferedReader;
import java.util.ArrayList;
import java.util.List;

public class JavaApp {

    public static void main(String[] args) throws Exception {
        Scanner vstup = new Scanner(System.in);
        String fileName = vstup.nextLine();

        BufferedReader reader = new BufferedReader(new FileReader(fileName));
        List<String> mazeLines = new ArrayList<>();
        String line;

        while ((line = reader.readLine()) != null) {
            mazeLines.add(line);
        }
        reader.close();

        if (mazeLines.isEmpty()) {
            System.out.println(0);
            return;
        }

        int rows = mazeLines.size();
        int cols = mazeLines.get(0).length();
        char[][] maze = new char[rows][cols];

        for (int i = 0; i < rows; i++) {
            maze[i] = mazeLines.get(i).toCharArray();
        }

        boolean[][] visited = new boolean[rows][cols];
        int spaceCount = 0;

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                if (maze[i][j] == ' ' && !visited[i][j]) {
                    exploreSpace(maze, visited, i, j, rows, cols);
                    spaceCount++;
                }
            }
        }

        System.out.println(spaceCount);
    }

    private static void exploreSpace(char[][] maze, boolean[][] visited, int i, int j, int rows, int cols) {
        if (i < 0 || i >= rows || j < 0 || j >= cols || maze[i][j] != ' ' || visited[i][j]) {
            return;
        }

        visited[i][j] = true;

        exploreSpace(maze, visited, i+1, j, rows, cols);
        exploreSpace(maze, visited, i-1, j, rows, cols);
        exploreSpace(maze, visited, i, j+1, rows, cols);
        exploreSpace(maze, visited, i, j-1, rows, cols);
    }
}
```

### Ostrovy 

```java
import java.util.Scanner;
import java.io.BufferedReader;
import java.io.FileReader;
import java.util.ArrayList;
import java.util.List;

public class JavaApp {

    public static void main(String[] args) throws Exception {
        Scanner vstup = new Scanner(System.in);
        String fileName = vstup.nextLine();

        List<String> lines = new ArrayList<>();
        BufferedReader br = new BufferedReader(new FileReader(fileName));
        String line;
        while ((line = br.readLine()) != null) {
            lines.add(line);
        }
        br.close();

        int rows = lines.size();
        if (rows == 0) {
            System.out.println(0);
            return;
        }

        char[][] grid = new char[rows][];
        for (int i = 0; i < rows; i++) {
            grid[i] = lines.get(i).toCharArray();
        }

        int count = 0;
        for (int i = 0; i < grid.length; i++) {
            for (int j = 0; j < grid[i].length; j++) {
                if (grid[i][j] == 'o') {
                    count++;
                    dfs(grid, i, j);
                }
            }
        }

        System.out.println(count);
    }

    private static void dfs(char[][] grid, int i, int j) {
        if (i < 0 || i >= grid.length || j < 0 || j >= grid[i].length || grid[i][j] != 'o') {
            return;
        }

        grid[i][j] = '.';

        dfs(grid, i + 1, j);
        dfs(grid, i - 1, j);
        dfs(grid, i, j + 1);
        dfs(grid, i, j - 1);
    }
}
```

### Suchou nohou 

```java
import java.io.*;
import java.util.*;

public class JavaApp {
    
    public static void main(String[] args) {
        Scanner vstup = new Scanner(System.in);
        String nazovSuboru = vstup.nextLine();
        
        try {
            FileReader fr = new FileReader(nazovSuboru);
            BufferedReader br = new BufferedReader(fr);
            
            ArrayList<String> riadky = new ArrayList<>();
            String riadok;
            while ((riadok = br.readLine()) != null) {
                riadky.add(riadok);
            }
            br.close();
            
            char[][] mapa = new char[riadky.size()][];
            for (int i = 0; i < riadky.size(); i++) {
                mapa[i] = riadky.get(i).toCharArray();
            }
            
            int startR = -1, startC = -1, cielR = -1, cielC = -1;
            
            for (int i = 0; i < mapa.length; i++) {
                for (int j = 0; j < mapa[i].length; j++) {
                    if (mapa[i][j] == 'A') {
                        startR = i;
                        startC = j;
                    }
                    if (mapa[i][j] == 'B') {
                        cielR = i;
                        cielC = j;
                    }
                }
            }
            
            int vysledok = najdiCestu(mapa, startR, startC, cielR, cielC);
            System.out.println(vysledok);
            
        } catch (Exception e) {
            System.out.println(-1);
        }
    }
    
    static int najdiCestu(char[][] mapa, int startR, int startC, int cielR, int cielC) {
        int riadky = mapa.length;
        int stlpce = mapa[0].length;
        
        boolean[][] navstivene = new boolean[riadky][stlpce];
        Queue<int[]> fronta = new LinkedList<>();
        
        fronta.add(new int[]{startR, startC, 0});
        navstivene[startR][startC] = true;
        
        int[] dr = {-1, 1, 0, 0};
        int[] dc = {0, 0, -1, 1};
        
        while (!fronta.isEmpty()) {
            int[] aktualny = fronta.poll();
            int r = aktualny[0];
            int c = aktualny[1];
            int vzdialenost = aktualny[2];
            
            if (r == cielR && c == cielC) {
                return vzdialenost + 1;
            }
            
            for (int i = 0; i < 4; i++) {
                int novyR = r + dr[i];
                int novyC = c + dc[i];
                
                if (novyR >= 0 && novyR < riadky && 
                    novyC >= 0 && novyC < stlpce && 
                    !navstivene[novyR][novyC] && 
                    (mapa[novyR][novyC] == 'o' || mapa[novyR][novyC] == 'A' || mapa[novyR][novyC] == 'B')) {
                    
                    navstivene[novyR][novyC] = true;
                    fronta.add(new int[]{novyR, novyC, vzdialenost + 1});
                }
            }
        }
        
        return -1;
    }
}
```

### Po vode všetkými smermi 

```java
import java.io.BufferedReader;
import java.io.FileReader;
import java.util.LinkedList;
import java.util.Queue;
import java.util.Scanner;

public class JavaApp {

    public static void main(String[] args) {
        Scanner vstup = new Scanner(System.in);
        String fileName = vstup.nextLine();

        try {
            BufferedReader reader = new BufferedReader(new FileReader(fileName));
            Queue<String> lines = new LinkedList<>();
            String line;
            while ((line = reader.readLine()) != null) {
                lines.add(line);
            }
            reader.close();

            int rows = lines.size();
            if (rows == 0) {
                System.out.println(-1);
                return;
            }
            int cols = lines.peek().length();
            char[][] grid = new char[rows][cols];

            int aRow = -1, aCol = -1;
            int bRow = -1, bCol = -1;

            int i = 0;
            for (String l : lines) {
                for (int j = 0; j < l.length(); j++) {
                    grid[i][j] = l.charAt(j);
                    if (grid[i][j] == 'A') {
                        aRow = i;
                        aCol = j;
                    } else if (grid[i][j] == 'B') {
                        bRow = i;
                        bCol = j;
                    }
                }
                i++;
            }

            if (aRow == -1 || bRow == -1) {
                System.out.println(-1);
                return;
            }

            int[][] directions = {
                    {-1, -1}, {-1, 0}, {-1, 1},
                    {0, -1},          {0, 1},
                    {1, -1},  {1, 0}, {1, 1}
            };

            Queue<int[]> queue = new LinkedList<>();
            queue.add(new int[]{aRow, aCol, 0});
            boolean[][] visited = new boolean[rows][cols];
            visited[aRow][aCol] = true;

            int result = -1;

            while (!queue.isEmpty()) {
                int[] current = queue.poll();
                int row = current[0];
                int col = current[1];
                int dist = current[2];

                if (row == bRow && col == bCol) {
                    result = dist;
                    break;
                }

                for (int[] dir : directions) {
                    int newRow = row + dir[0];
                    int newCol = col + dir[1];

                    if (newRow >= 0 && newRow < rows && newCol >= 0 && newCol < cols
                            && !visited[newRow][newCol]
                            && (grid[newRow][newCol] == '.' || grid[newRow][newCol] == 'B')) {
                        visited[newRow][newCol] = true;
                        queue.add(new int[]{newRow, newCol, dist + 1});
                    }
                }
            }

            System.out.println(result);

        } catch (Exception e) {
            System.out.println(-1);
        }
    }
}
```

## Ďalšie údajové štruktúry 

### Ples pre osamelých 

```java
import java.util.Scanner;
import java.util.ArrayList;
import java.util.List;

public class JavaApp {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();

        List<Character> salon = new ArrayList<>();

        for (int i = 0; i < input.length(); i++) {
            char person = input.charAt(i);

            if (person == 'M') {
                if (!salon.isEmpty() && salon.get(salon.size()-1) == 'Z') {
                    salon.remove(salon.size()-1);
                    System.out.println("M - spárovať");
                } else {
                    salon.add('M');
                    System.out.println("M - do salónu");
                }
            } else if (person == 'Z') {
                if (!salon.isEmpty() && salon.get(salon.size()-1) == 'M') {
                    salon.remove(salon.size()-1);
                    System.out.println("Z - spárovať");
                } else {
                    salon.add('Z');
                    System.out.println("Z - do salónu");
                }
            }
        }

        System.out.print("salón: ");
        if (salon.isEmpty()) {
            System.out.println("prázdny");
        } else {
            for (char p : salon) {
                System.out.print(p);
            }
            System.out.println();
        }
    }
}
```

### Simulácia tlačiarne 

```java
import java.util.ArrayList;
import java.util.Scanner;

public class JavaApp {
    
    public static void main(String[] args) {
        ArrayList<String> printerTasks = new ArrayList<>();
        Scanner scanner = new Scanner(System.in);
        
        while (true) {
            String input = scanner.nextLine();
            
            if (input.equals("0")) {
                break;
            }
            
            if (input.startsWith("pridaj ")) {
                String task = input.substring(7);
                printerTasks.add(task);
            } else if (input.equals("vytlac")) {
                if (printerTasks.isEmpty()) {
                    System.out.println("prazdno");
                } else {
                    String task = printerTasks.remove(0);
                    System.out.println(task);
                }
            }
        }
        
        System.out.print("front: ");
        if (printerTasks.isEmpty()) {
            System.out.print("prazdno");
        } else {
            for (int i = 0; i < printerTasks.size(); i++) {
                if (i > 0) {
                    System.out.print(", ");
                }
                System.out.print(printerTasks.get(i));
            }
        }
        
        scanner.close();
    }
}
```

### Presúvanie guličiek - ručne 

```java
import java.util.Scanner;
import java.util.ArrayList;

public class JavaApp {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        ArrayList<Integer> snurka1 = new ArrayList<>();
        ArrayList<Integer> snurka2 = new ArrayList<>();
        ArrayList<Integer> snurka3 = new ArrayList<>();

        String vstup = sc.nextLine();
        String[] gulicky = vstup.split(" ");

        for (String g : gulicky) {
            snurka1.add(Integer.parseInt(g));
        }

        while (true) {
            String prikaz = sc.nextLine();

            if (prikaz.equals("0")) {
                break;
            }

            String[] cast = prikaz.split("-");
            int odkial = Integer.parseInt(cast[0]);
            int kam = Integer.parseInt(cast[1]);

            ArrayList<Integer> odSnurka;
            if (odkial == 1) {
                odSnurka = snurka1;
            } else if (odkial == 2) {
                odSnurka = snurka2;
            } else {
                odSnurka = snurka3;
            }

            if (odSnurka.isEmpty()) {
                System.out.println("PRAZDNA");
                continue;
            }

            int gulicka = odSnurka.remove(odSnurka.size() - 1);

            if (kam == 1) {
                snurka1.add(gulicka);
            } else if (kam == 2) {
                snurka2.add(gulicka);
            } else {
                snurka3.add(gulicka);
            }
        }

        System.out.print("1:");
        for (int g : snurka1) {
            System.out.print(" " + g);
        }
        System.out.println();

        System.out.print("2:");
        for (int g : snurka2) {
            System.out.print(" " + g);
        }
        System.out.println();

        System.out.print("3:");
        for (int g : snurka3) {
            System.out.print(" " + g);
        }
        System.out.println();
    }
}
```

### Binárny vyhľadávací strom 

```java
import java.util.Scanner;

public class JavaApp {

    public static class Strom {
        Vrchol koren;

        void pridaj(int hodnota) {
            koren = pridajVrchol(koren, hodnota);
        }

        Vrchol pridajVrchol(Vrchol v, int hodnota) {
            if (v == null) {
                return new Vrchol(hodnota);
            }
            if (hodnota <= v.hodnota) {
                v.lavy = pridajVrchol(v.lavy, hodnota);
            } else {
                v.pravy = pridajVrchol(v.pravy, hodnota);
            }
            return v;
        }

        void preorder(Vrchol v) {
            if (v != null) {
                System.out.print(v.hodnota + " ");
                preorder(v.lavy);
                preorder(v.pravy);
            }
        }

        void postorder(Vrchol v) {
            if (v != null) {
                postorder(v.lavy);
                postorder(v.pravy);
                System.out.print(v.hodnota + " ");
            }
        }

        void inorder(Vrchol v) {
            if (v != null) {
                inorder(v.lavy);
                System.out.print(v.hodnota + " ");
                inorder(v.pravy);
            }
        }
    }

    public static class Vrchol {
        int hodnota;
        Vrchol lavy;
        Vrchol pravy;

        Vrchol(int h) {
            hodnota = h;
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Strom strom = new Strom();

        String riadok = sc.nextLine();
        String[] cisla = riadok.split(" ");

        for (String s : cisla) {
            int cislo = Integer.parseInt(s);
            strom.pridaj(cislo);
        }

        strom.preorder(strom.koren);
        System.out.println();

        strom.postorder(strom.koren);
        System.out.println();

        strom.inorder(strom.koren);
        System.out.println();
    }
}
```

### Generátor n-tíc 

```java
import java.util.Scanner;

public class JavaApp {
    
    public static void main(String[] args) {
        
        Scanner sc = new Scanner(System.in);
        int m = sc.nextInt();
        int n = sc.nextInt();
        
        String[] stack = new String[10000];
        int top = 0;
        stack[top++] = "";
        
        while (top > 0) {
            String current = stack[--top];
            
            if (current.length() == n) {
                System.out.print(current + " ");
            } else {
                for (int i = m; i >= 0; i--) {
                    stack[top++] = current + i;
                }
            }
        }
        
    }
}
```
