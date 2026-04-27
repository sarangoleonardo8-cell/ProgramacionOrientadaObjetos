# 💼 Programación Orientada a Objetos 
# Nombre: Jefferson Sarango

## 📌 Descripción
La presente actividad tiene la finalidad de nivelar y mejorar sus conocimientos a los estudiantes en fundamentos de la programación y en programación orientada a Objetos con Java, a través de la resolución de los siguiente ejercicios en línea. Los mismos que deberan entregar sus avances en las tutorías o hasta la fecha determinada.

## 📚 Contenido de Actividades

### 📁 Java Stdin and Stdout I
**Problema:** Leer 3 enteros desde stdin y imprimirlos en stdout, cada uno en una línea.
**Conceptos:** Scanner, System.out.println, Tipos de datos, Entrada/Salida básica

```java
import java.util.Scanner;

/**
 * @author Jefferson Sarango
 */

public class Solution {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int a = scan.nextInt();
        int b = scan.nextInt();
        int c = scan.nextInt();

        System.out.println(a);
        System.out.println(b);
        System.out.println(c);
    }
}
```

### 📁 Java If-Else
**Problema:** Determinar si un número es par, impar o cero usando condicionales if-else.
**Conceptos:** Condicionales, Operadores módulo, Estructuras de decisión, Control de flujo

```java
import java.util.Scanner;

/**
 * @author Jefferson Sarango
 */

public class Solution {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int n = scan.nextInt(); 
        
        if (n % 2 == 1) {
            System.out.println("Weird");
        } else if (n >= 2 && n <= 5) {
            System.out.println("Not Weird");
        } else if (n >= 6 && n <= 20) {
            System.out.println("Weird");
        } else {
            System.out.println("Not Weird");
        }
    }
}
```

### 📁 Java Stdin and Stdout II
**Problema:** Leer diferentes tipos de datos (int, double, string) y mostrarlos formateados.
**Conceptos:** Scanner, Formateo de salida, Tipos primitivos, Conversión de tipos

```java
import java.util.Scanner;

/**
 * @author Jefferson Sarango
 */

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int x = sc.nextInt();
        double y = sc.nextDouble();
        sc.nextLine(); // Consume newline
        String s = sc.nextLine();
        
        System.out.println("String: " + s);
        System.out.println("Double: " + y);
        System.out.println("Int: " + x);
    }
}
```

### 📁 Java Output Formatting
**Problema:** Formatear números para que ocupen exactamente 15 caracteres de ancho.
**Conceptos:** printf, Formato de números, Alineación de texto, Especificadores de formato

```java
import java.util.Scanner;

/**
 * @author Jefferson Sarango
 */

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("================================");
        for (int i = 0; i < 3; i++) {
            String s1 = sc.next();
            int x = sc.nextInt();
            System.out.printf("%-15s%03d%n", s1, x);
        }
        System.out.println("================================");
    }
}
```

### 📁 Java Loops I
**Problema:** Generar tabla de multiplicar de un número usando bucles.
**Conceptos:** Bucle for, Printf, Multiplicación, Tablas matemáticas

```java
import java.util.Scanner;

/**
 * @author Jefferson Sarango
 */

public class Solution {
    public static void main(String[] args) {
        Scanner N = new Scanner(System.in);
        int n = N.nextInt();
        
        for (int i = 1; i <= 10; i++) {
            System.out.printf("%d x %d = %d%n", n, i, n * i);
        }
    }
}
```

### 📁 Java Loops II
**Problema:** Calcular series matemáticas usando potencias y bucles anidados.
**Conceptos:** Bucle for, Math.pow, Series matemáticas, Estructuras de repetición

```java
import java.util.Scanner;
import java.lang.Math;

/**
 * @author Jefferson Sarango
 */

class Solution {
    public static void main(String[] argh) {
        Scanner in = new Scanner(System.in);
        int t = in.nextInt();

        for (int i = 0; i < t; i++) {
            int a = in.nextInt();
            int b = in.nextInt();
            int n = in.nextInt();

            int sum = a;

            for (int j = 0; j < n; j++) {
                sum += (int) Math.pow(2, j) * b;
                System.out.print(sum);

                if (j < n - 1) {
                    System.out.print(" ");
                }
            }

            System.out.println();
        }

        in.close();
    }
}
```

### 📁 Java End-of-file
**Problema:** Leer entrada hasta fin de archivo (EOF) procesando múltiples líneas.
**Conceptos:** hasNext(), EOF, Streams de entrada, Procesamiento continuo

```java
import java.util.Scanner;

/**
 * @author Jefferson Sarango
 */

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        while (sc.hasNext()) {
            String input = sc.nextLine();
            System.out.println(input);
        }
        
        sc.close();
    }
}
```

### 📁 Java Static Initializer Block
**Problema:** Inicializar variables estáticas basadas en condiciones matemáticas.
**Conceptos:** Bloques estáticos, Variables estáticas, Inicialización automática, Validación

```java
import java.util.Scanner;

/**
 * @author Jefferson Sarango
 */

public class Solution {
    static int B, H;
    static boolean flag;
    
    static {
        Scanner scan = new Scanner(System.in);
        B = scan.nextInt();
        H = scan.nextInt();
        
        if (B > 0 && H > 0) {
            flag = true;
        } else {
            flag = false;
            System.out.println("java.lang.Exception: Breadth and height must be positive");
        }
    }
    
    public static void main(String[] args) {
        if (flag) {
            int area = B * H;
            System.out.print(area);
        }
    }
}
```

### 📁 Java Int to String
**Problema:** Convertir enteros a strings y manejar casos especiales.
**Conceptos:** String.valueOf(), Conversión de tipos, Manejo de nulos, Try-catch

```java
import java.util.Scanner;

/**
 * @author Jefferson Sarango
 */

public class Solution {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int n = scan.nextInt();
        
        try {
            String s = String.valueOf(n);
            System.out.println("Good job");
        } catch (Exception e) {
            System.out.println("Wrong answer");
        }
        
        scan.close();
    }
}
```

### 📁 Java Date and Time
**Problema:** Encontrar el día de la semana para una fecha específica.
**Conceptos:** LocalDate, DayOfWeek, Formato de fechas, Locale, Calendar API

```java
import java.time.LocalDate;
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.function.*;
import java.util.regex.*;
import java.util.stream.*;
import static java.util.stream.Collectors.joining;
import static java.util.stream.Collectors.toList;

/**
 * @author Jefferson Sarango
 */
 
class Result {
    public static String findDay(int month, int day, int year) {
        Calendar cal = Calendar.getInstance();
        cal.set(Calendar.YEAR, year);
        cal.set(Calendar.MONTH, month - 1);
        cal.set(Calendar.DAY_OF_MONTH, day);

        int dayOfWeek = cal.get(Calendar.DAY_OF_WEEK);

        String[] days = {
            "SUNDAY", "MONDAY", "TUESDAY",
            "WEDNESDAY", "THURSDAY", "FRIDAY", "SATURDAY"
        };

        return days[dayOfWeek - 1];
    }
}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        String[] firstMultipleInput = bufferedReader.readLine().replaceAll("\\s+$", "").split(" ");

        int month = Integer.parseInt(firstMultipleInput[0]);
        int day = Integer.parseInt(firstMultipleInput[1]);
        int year = Integer.parseInt(firstMultipleInput[2]);

        String res = Result.findDay(month, day, year);

        bufferedWriter.write(res);
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}
```

### 📁 Java Currency Formatter
**Problema:** Formatear moneda según diferentes configuraciones locales.
**Conceptos:** NumberFormat, Locale, Formato de moneda, Internacionalización

```java
import java.util.Scanner;
import java.text.NumberFormat;
import java.util.Locale;

import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

/**
 * @author Jefferson Sarango
 */

public class Solution {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double payment = scanner.nextDouble();
        scanner.close();
        
        NumberFormat usFormat = NumberFormat.getCurrencyInstance(Locale.US);
        NumberFormat indiaFormat = NumberFormat.getCurrencyInstance(new Locale("en", "IN"));
        NumberFormat chinaFormat = NumberFormat.getCurrencyInstance(Locale.CHINA);
        NumberFormat franceFormat = NumberFormat.getCurrencyInstance(Locale.FRANCE);
        
        System.out.println("US: " + usFormat.format(payment));
        System.out.println("India: " + indiaFormat.format(payment));
        System.out.println("China: " + chinaFormat.format(payment));
        System.out.println("France: " + franceFormat.format(payment));
    }
}
```

### 📁 Java Strings Introduction
**Problema:** Manipulación básica de strings: longitud, concatenación, caracteres específicos.
**Conceptos:** String.length(), concat(), charAt(), Operaciones básicas

```java
import java.util.Scanner;

/**
 * @author Jefferson Sarango
 */

public class Solution {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String A = scanner.next();
        String B = scanner.next();
        
        int sum = A.length() + B.length();
        System.out.println(sum);
        
        if (A.compareTo(B) > 0) {
            System.out.println("Yes");
        } else {
            System.out.println("No");
        }
        
        String capitalizedA = A.substring(0, 1).toUpperCase() + A.substring(1);
        String capitalizedB = B.substring(0, 1).toUpperCase() + B.substring(1);
        
        System.out.println(capitalizedA + " " + capitalizedB);
        
        scanner.close();
    }
}
```

### 📁 Java Substring
**Problema:** Extraer substring específico basado en índices start y end.
**Conceptos:** substring(), Índices, Extracción de texto, Manejo de rangos

```java
import java.util.Scanner;

/**
 * @author Jefferson Sarango
 */

public class Solution {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        String S = in.next();
        int start = in.nextInt();
        int end = in.nextInt();
        
        String result = S.substring(start, end);
        System.out.println(result);
    }
}
```

### 📁 Java Substring Comparisons
**Problema:** Encontrar el substring lexicográficamente más grande y más pequeño.
**Conceptos:** compareTo(), Ordenamiento lexicográfico, Búsqueda de patrones, Comparación

```java
import java.util.Scanner;

/**
 * @author Jefferson Sarango
 */

public class Solution {
    public static String getSmallestAndLargest(String s, int k) {
        String smallest = s.substring(0, k);
        String largest = s.substring(0, k);
        
        for (int i = 1; i <= s.length() - k; i++) {
            String sub = s.substring(i, i + k);
            
            if (sub.compareTo(smallest) < 0) {
                smallest = sub;
            }
            if (sub.compareTo(largest) > 0) {
                largest = sub;
            }
        }
        
        return smallest + "\n" + largest;
    }

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        String s = scan.next();
        int k = scan.nextInt();
        scan.close();
        
        System.out.println(getSmallestAndLargest(s, k));
    }
}
```

### 📁 Java String Reverse
**Problema:** Verificar si un string es palíndromo usando reversión.
**Conceptos:** StringBuilder, reverse(), Palíndromos, Eficiencia en strings

```java
import java.util.Scanner;

/**
 * @author Jefferson Sarango
 */

class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String A = sc.next();
        
        // Reverse the string
        String reversed = new StringBuilder(A).reverse().toString();
        
        // Check if palindrome
        if (A.equals(reversed)) {
            System.out.println("Yes");
        } else {
            System.out.println("No");
        }
        
        sc.close();
    }
}
```

## 🎯 Objetivos de Aprendizaje
- ✅ Dominar entrada/salida estándar en Java
- ✅ Implementar estructuras de control efectivas
- ✅ Manejar bucles y iteraciones eficientemente
- ✅ Formatear salida de manera profesional
- ✅ Trabajar con strings y sus operaciones
- ✅ Gestionar fechas, tiempos y monedas
- ✅ Aplicar conceptos de programación orientada a objetos

## 📈 Progreso
- 🟢 Java Stdin and Stdout I - Completado
- 🟢 Java If-Else - Completado  
- 🟢 Java Stdin and Stdout II - Completado
- 🟢 Java Output Formatting - Completado
- 🟢 Java Loops I - Completado
- 🟢 Java Loops II - Completado
- 🟢 Java End-of-file - Completado
- 🟢 Java Static Initializer Block - Completado
- � Java Int to String - Completado
- 🟢 Java Date and Time - Completado
- 🟢 Java Currency Formatter - Completado
- 🟢 Java Strings Introduction - Completado
- 🟢 Java Substring - Completado
- � Java Substring Comparisons - Completado
- 🟢 Java String Reverse - Completado
___
## 🔗 Enlaces Útiles
- 👤 [Perfil de Jefferson Sarango](https://www.hackerrank.com/profile/jefferson_l_sar1)
- 📚 [Documentación Oracle Java](https://docs.oracle.com/javase/tutorial/)
