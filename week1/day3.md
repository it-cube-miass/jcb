## Теория

### List
**List** — это структура данных, которая позволяет хранить информацию в списке, а не, например, в массиве.
В мире Java ```List``` — это интерфейс, а его имплементаций существует несколько.
* Поищите различные реализации ```List```
* Не старайтесь копировать готовые реализации

## Практическая работа
Написать свою реализацию ```List```, которая пройдет тесты. Изучите сигнатуры методов и подумайте как это может стать двунаправленным ```LinkedList```. 

Совет: не старайтесь скопировать или написать по аналогии с уже реализованными двусвязными списками. Тут нужно изобрести свой двусвязный список, основываясь на выданном вам  API.

**Нельзя** использовать внешние импорты, но можно использовать свои классы из прошлых дней и ```Function```.

**Предупреждение!** Eсли какой либо тест вывел просто null — значит было получено неожиданное исключение (постараемся выдать это исключение на экран, в обновлениях).

Класс должен быть в пакете:
```java
package com.kovalevskyi.academy.codingbootcamp.week1.day3
```

### Класс List
Написать свой класс List и реализовать в нем все ниже описанные методы.  Объект класса можно создавать только при помощи ```new```. Каждый объект этого класса хранит в себе некое ```value```. 
Обратите внимание, что тестирование некоторых методов комплексное — методы взаимозависимы. Например ```createOne``` и ```getValue```. 

#### List
Этот конструктор на вход принимает предыдущий и следующий элементы листа и текущее значение.
```java
// сигнатура конструктора
private List(List<T> prev, List<T> next, T value) {
   // TODO
}
```

#### createOne 
Создает новый объект со значением value.
```java
// сигнатура метода
public static <T> List<T> createOne(T value) {
   // TODO
}
```

#### addToEnd
Этот метод добавляет новое значение  в конец листа и возвращает ссылку на этот новый элемент листа.
```java
// сигнатура метода
public static <T> List<T> addToEnd(List<T> list, T newValue) {
   // TODO
}
```

#### addToStart
Этот метод добавляет новое значение  в начало листа и возвращает ссылку на этот новый элемент листа.
```java
// сигнатура метода
public static <T> List<T> addToStart(List<T> list, T newValue) {
  // TODO
}
```

#### сontains
Возвращает ```true```, если заданное значение присутствует в листе и ```false```, если такого значения нет. **List<T> list** — любой случайный элемент листа.
```java
// сигнатура метода
public static <T> boolean contains(List<T> list, T value) {
   // TODO
}
```

#### map
Создает новый лист равный по размеру текущему листу, в котором каждый элемент получен путем применения mapFunction к value элемента текущего листа.  
Рекомендуем почитать про обобщение методов в java.
```java
// сигнатура метода
public static <T, R> List<R> map(List<T> list, Function<T, R> mapFunction) {
   // TODO
}
```

#### length
Возвращает количество элементов в  текущем листе.  Независимо от того у какого элемента листа был вызван этот метод.
```java
// сигнатура метода
public int length() {
  // TODO
}
```

#### insertAfter
Добавляет новый элемент листа после текущего и возвращает этот новый элемент.
// сигнатура метода
```java
public List<T> insertAfter(T newValue) {
  // TODO
}
```

#### insertAfter(T[] newValues)
Добавляет новые элементы из входящего массива в текущий список, после текущего элемента списка.
```java
// сигнатура метода
public void insertAfter(T[] newValues) {
   // TODO
}
```

#### delete 
Удаляет текущий элемент листа.
```java
// сигнатура метода
public void delete() {
   // TODO
}
```

#### connect 
Связывает текущий элемент листа с входящим to.
```java
// сигнатура метода
public void connect(List<T> to) {
   // TODO
}
```

#### getNext 
Возвращает следующий элемент листа.
```java
// сигнатура метода
public List<T> getNext() {
   // TODO
}
```

#### getPrev 
Возвращает предыдущий элемент листа.
```java
// сигнатура метода
public List<T> getPrev() {
  // TODO
}
```

#### setPrev 
Устанавливает предыдущий элемент текущему элементу листа.
```java
// сигнатура метода
public void setPrev(List<T> prev) {
  // TODO
}
```

#### setNext 
Устанавливает следующий элемент текущему элементу листа.
```java
// сигнатура метода
public void setNext(List<T> next) {
   // TODO
}
```

#### getValue 
Возвращает значение текущего элемента листа.
```java
// сигнатура метода
public T getValue() {
   // TODO
}
```