## Теория

### Таблицы кодировок ASCII
В вычислительных машинах символы не могут храниться иначе, как в виде последовательностей бит. Для передачи символа и его корректного отображения ему должна соответствовать уникальная последовательность нулей и единиц. Для этого были разработаны таблицы кодировок. ASCII представляет собой кодировку для представления десятичных цифр, латинского и национального алфавитов, знаков препинания и управляющих символов.
* Найти информацию о таблицах кодировок.  Гуглить “ASCII symbol” или man ascii в терминале.

### Создание строк
Для извлечения символов по индексу в классе ```String``` определен метод **charAt(int index)**. Он принимает индекс, по которому надо получить символ и возвращает извлеченный символ. Как и в массивах индексация начинается с нуля. 
* Найти [информацию](https://docs.oracle.com/javase/tutorial/java/data/manipstrings.html) об управлении символами в строке в Java
* Найти информацию о классе ```StringBuilder```

## Практическая работа
**Запрещено** использовать любой импорт и класс String (если в описании метода не сказано иное).  
Все классы этого задания должны быть в пакете:
```java
package com.kovalevskyi.academy.codingbootcamp.week1.day2
```

### Класс StdString1
В этом задании мы начнем создавать свой собственный аналог класса ```String```!  Учтите, что многие методы взаимосвязаны.
```java
public class StdString1 implements Iterable<Character> {
   // TO DO
}
```

#### StdString1(char[] base) 
Простой конструктор, который создает строку из входного массива символов.
```java
// сигнатура конструктора
public StdString1(char[] base) {
   // TO DO
}
```

#### StdString1() 
Пустой конструктор, который создает пустую строку длиной 0.
```java
// сигнатура конструктора
public StdString1() {
   // TO DO
}
```

#### StdString1(StdString stdString) 
Конструктор, который создает копию входящей строки. Новая строка должна быть создана из точно таких же символов, как и входящая.
```java
// сигнатура конструктора
public StdString1(StdString1 stdString1) {
   // TO DO
}
```

#### length
Написать метод, который возвращает количество символов в строке. Например, "cat" вернет 3, "cat in the box" вернет 14.
```java
// сигнатура метода
public int length() {
   // TO DO
}
```

#### append
Написать метод, который принимает строку, добавляет ее к текущей строке и возвращает сформированную новую строку. Например, если есть строка "cat" и другая строка "dog", ваш метод должен вернуть новую строку "catdog". Если на вход передают NULL, кинуть ```NullPointerException```.
```java
// сигнатура метода
public StdString1 append(StdString1 that) {
   // TO DO
}
```

#### toCharArray
Написать метод, который возвращает массив символов из текущей строки.
```java
// сигнатура метода
public char[] toCharArray() {
   // TO DO
}
```

#### charAt
Написать метод, который возвращает символ по определенному  индексу. Например, в строке "cat", на позиции "0" находится символ 'с', в строке "dog", на позиции "2" находится символ 'g', а в строке "dogcat", на позиции "7" нет символа — ```indexOutOfBoundsException```.
```java
// сигнатура метода
public char charAt(int index) {
   // TO DO
}
```

#### indexOf
Написать метод, который находит первый нужный символ в строке и возвращает его индекс. Если такого символа нет, вернуть -1. Например, в строке "cat" индекс символа  't' →  2, в строке "dog" индекс символа 'c' → (-1),  а в строке "catanddog" индекс символа 'a' → 1.
```java
// сигнатура метода
public int indexOf(char target) {
   // TO DO
}
```

#### equals
Написать метод, который сравнивает каждый символ текущей строки с каждым символом входящей строки. Вернуть true, если строки равные и false, если нет.
```java
// сигнатура метода
@Override
public boolean equals(final Object otherObj) {
   // TO DO
}
```

#### hashCode
Написать метод, который возвращает хеш код строки. Хеш код подсчитывается путем суммирования целочисленных представлений каждого символа в строке.  
"Cat" → C: 67 a: 97 t: 116 → 67 + 97 + 116 = 280. Если строка нулевой длины — вернуть 0.
```java
// сигнатура метода
@Override
public int hashCode() {
   // TO DO
}
```

#### toString
Написать метод, который конвертирует объект StdString1 в объект String. Тут позволено использовать ```java.lang.String```. 
```java
// сигнатура метода
@Override
public String toString() {
   // TO DO
}
```

#### iterator
Написать метод **iterator()**, который работает точно так же, как и оригинальный [Iterator из документации](https://docs.oracle.com/javase/8/docs/api/java/util/Iterator.html) (придется импортировать этот интерфейс и класс исключение). 
```java
// сигнатура метода
@Override
public Iterator<Character> iterator() {
   // TO DO
}
```

#### forEach
Написать метод **forEach()**, который проходит по каждому символу в строке и применяет к нему action. Тут тоже придется импортировать один интерфейс. 
```java
// сигнатура метода
@Override
public void forEach(final Consumer<? super Character> action) {
   // TO DO
}
```

### Класс StringUtils
**Разрешено**: ```java.util.stream.IntStream```.  
**Запрещено**: методы: ```Integer.valueOf```, классы: ```String``` (но можно использовать ```StringBuilder```).

#### isAsciiUppercase	
Написать метод **isAsciiUppercase(char ch)**, который принимает на вход ```char``` и возвращает ```true```, если символ — это буква от A до Z (верхний регистр) и ```false``` — любой другой ASCII символ. Ожидается, что метод кинет ```IllegalArgumentException```, если входящий символ не является ASCII символом.
```java
// сигнатура метода
public static boolean isAsciiUppercase(char ch) {
   // TO DO
}
```
Пример:
```java
isAsciiUppercase('A'); // → true;
isAsciiUppercase('d'); // → false;
isAsciiUppercase((char)257); // → IllegalArgumentException
```

#### isAsciiLowercase
Написать метод **isAsciiLowercase(char ch)**, который принимает на вход ```char``` и возвращает ```true```, если символ — это буква от a до z (нижний регистр) и ```false``` — любой другой ASCII символ. Ожидается, что метод кинет ```IllegalArgumentException```, если входящий символ не является ASCII символом.
```java
// сигнатура метода
public static boolean isAsciiLowercase(char ch) {
   // TO DO
}
```
Пример:
```java
isAsciiLowercase('A'); // → false
isAsciiLowercase('d'); // → true
isAsciiLowercase((char)257); // → IllegalArgumentException
```

#### isAsciiNumeric
Написать метод **isAsciiNumeric(char ch)**, который принимает на вход ```char``` и возвращает ```true```, если символ — это цифра от 0 до 9 и ```false``` — любой другой ASCII символ. Ожидается, что метод кинет ```IllegalArgumentException```, если входящий символ не является ASCII символом.
```java
// сигнатура метода
public static boolean isAsciiNumeric(char ch) {
   // TO DO
}
```
Пример:
```java
isAsciiNumeric('Z'); // → false
isAsciiNumeric('1'); // → true
isAsciiNumeric((char)257); // → IllegalArgumentException
```

#### isAsciiAlphabetic
Написать метод **isAsciiAlphabetic(char ch)**, который принимает на вход ```char``` и возвращает ```true```, если символ — это буква от a до z (нижний регистр) или от A до Z (верхний регистр) и ```false``` — любой другой ASCII символ. Ожидается, что метод кинет ```IllegalArgumentException```, если входящий символ не является ASCII символом.
```java
// сигнатура метода
public static boolean isAsciiAlphabetic(char ch) {
   // TO DO
}
```
Пример:
```java
isAsciiAlphabetic('Z'); // → true
isAsciiAlphabetic('a'); // → true
isAsciiAlphabetic('1'); // → false
isAsciiAlphabetic((char)257); // → IllegalArgumentException
```

#### toAsciiUppercase
Написать метод **toAsciiUppercase(char ch)**, который принимает на вход ```char``` и возвращает символ в верхнем регистре. Ожидается, что метод кинет ```IllegalArgumentException```, если входящий символ не является ASCII символом.
```java
// сигнатура метода
public static char toAsciiUppercase(char ch) {
   // TO DO
}
```
Пример: 
```java
toAsciiUppercase('a'); // → 'A'
toAsciiUppercase('B'); // → 'B'
toAsciiUppercase('1'); // → '1'
toAsciiUppercase('@'); // → '@'
toAsciiUppercase((char)257); // → IllegalArgumentException
```

#### toAsciiLowercase
Написать метод **toAsciiLowercase(char ch)**, который принимает на вход ```char``` и возвращает символ в нижнем регистре. Ожидается, что метод кинет ```IllegalArgumentException```, если входящий символ не является ASCII символом.
```java
// сигнатура метода
public static char toAsciiLowercase(char ch) {
   // TO DO
}
```
Пример:
```java
toAsciiLowercase('a'); // → 'a'
toAsciiLowercase('B'); // → 'b'
toAsciiLowercase('1'); // → '1'
toAsciiLowercase('@'); // → '@'
toAsciiLowercase((char)257); // → IllegalArgumentException
```

#### makeUppercase
Написать метод **makeUppercase(char[] input)**, который принимает на вход массив символов и возвращает строку символов в верхнем регистре. Ожидается, что метод кинет ```IllegalArgumentException```, если хоть один из входящих символов не является ASCII.
```java
// сигнатура метода
public static StringBuilder makeUppercase(char[] input) {
   // TO DO
}
```
Пример: 
```java
makeUppercase({'h', 'e', 'l', 'L', 'o'}); // → "HELLO"
makeUppercase({'@','h', 'e', 'l', 'L', 'o', '1', '2'}); // → "@HELLO12"
makeUppercase({'h', 'e', 'l', 'L', 'o', (char)257}); // → IllegalArgumentException
```

#### makeLowercase
Написать метод **makeLowercase(char[] input)**, который принимает на вход массив символов и возвращает строку символов в нижнем регистре. Ожидается, что метод кинет ```IllegalArgumentException```, если хоть один из входящих символов не является ASCII. 
```java
// сигнатура метода
public static StringBuilder makeLowercase(char[] input) {
   // TO DO
}
```
Пример:
```java
makeLowercase({'h', 'e', 'l', 'L', 'o'}); // → "hello"
makeLowercase({'@','h', 'e', 'l', 'L', 'o', '1', '2'}); // → "@hello12"
makeLowercase({'h', 'e', 'l', 'L', 'o', (char)257}); // → IllegalArgumentException
```

#### makeCamel
Написать метод **makeCamel(char[] input)**, который принимает на вход массив символов и возвращает строку символов в нижнем и ВЕРХНЕМ регистре последовательно (начиная с нижнего). Ожидается, что метод кинет ```IllegalArgumentException```, если хоть один из входящих символов не является ASCII.
```java
// сигнатура метода
public static StringBuilder makeCamel(char[] input) {
   // TO DO
}
```
Пример: 
```java
makeCamel({'h', 'e', 'l', 'L', 'o'}); // → "hЕlLo"
makeCamel({'@','h', 'e', 'l', 'L', 'o', '0', '1', '2'}); // → "@HeLlO012"
makeCamel({'h', 'e', 'l', 'L', 'o', (char)257}); // → IllegalArgumentExcep tion
```

#### isStringAlphaNumerical
Написать метод **isStringAlphaNumerical(char[] input)**, который принимает на вход массив символов и возвращает ```true```, если все символы — это буквы или цифры, или пробелы. Ожидается, что метод кинет ```IllegalArgumentException```, если хоть один из входящих символов не является ASCII. 
```java
// сигнатура метода
public static boolean isStringAlphaNumerical(char[] input) {
   // TO DO
}
```
Пример:
```java
isStringAlphaNumerical({'a', 'b', '1', ' '}); // → true
isStringAlphaNumerical({'a', ',', '1', ' '}); // → false
isStringAlphaNumerical({'a', (char)257, '1', ' '}); // → IllegalArgumentException
```

#### concatStrings
Написать метод **concatStrings(char[][] input)**, который принимает на вход двумерный массив символов, соединяет их и возвращает новый одномерный результирующий массив. Ожидается, что метод кинет ```IllegalArgumentException```, если хоть один из входящих символов не является ASCII.
```java
// сигнатура метода
public static char[] concatStrings(char[][] input) {
   // TO DO
}
```
Пример: 
```java
concatStrings({'a', 'b'}, {'c', 'd'}); // → {'a', 'b', 'c', 'd'}
concatStrings({'a', 'b', (char)257}, {'c', 'd'}); // → IllegalArgumentException
```

#### toInt
Написать метод **toInt(char[] input)**, который принимает на вход массив символов и возвращает число ```int```. Ожидается, что метод кинет ```IllegalArgumentException```, если хоть один из входящих символов не является ASCII. 
```java
// сигнатура метода
public static int toInt(char[] input) {
   // TO DO
}
```
Пример:
```java
toInt({'1', '2'}); // → 12
toInt({'0'}); // → 0
toInt({'-', '1', '1'}); // → -11
toInt({(char)257, '2'}); // → IllegalArgumentException
```
