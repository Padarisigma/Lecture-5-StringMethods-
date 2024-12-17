# Lecture-5-StringMethods
# Now we say about string and numbers methods in JS
### Overview 
* String
* Methods
* Number


У нас есть три способа создание типа стринг такие как:
 1. Double quotes 
   ``` js 
   let doubleQuotes = "hello";
   ```
2. Single Quotes 
``` js 
let SingleQuotes= 'hello';
```
3. Backticks 
``` js 
let backticks = `hello ${2+2}` // `Hello 4`
```

## What is a method in a JS?
*Метод — это блок кода, который выполняется только при вызове. Вы можете передавать данные, известные как
в метод. Методы используются для выполнения определенных действий, и они также бывают
известны как функции.*

1. Methods String :
   * CharAt(), at()
   * toString() - dont have parametr 
   * concat ()
   * trim()
   * includes()
   * indexOf() , lastIndexOf()
   * replace(), replaceAll()
   * substring(), slice
   * split
   * toLowerCase(), toUpperCase() <br> <br>
2. Methods number :
   * Math.floor()
   * math.ceil()
   * math.round()
   * math.abs()
   * math.max() && math.min()
   * math.pow()
   * math.sqrt()
   * math.random()
   * isNan()
  

*Это одни из часто используемых, теперь поговорим о них подробнее.*

1. charAt() and at()- по сути они выполняют одинаковую функцию, только at() может принимать отрицательные числа. Сама их функция заключаетс в том что мы можем с определенного текста, слова при помощи индексов выбрать и вывести нам нужную букву.
``` js 
let text="hello, world";
console.log(text.charAt(2)); // выведет l, первую l 

let text="hello, world";
console.log(text.at(-1)); // выведет последнюю букву, в этом и вся разница.
```

2. toString - Метод toString() возвращает строку, представляющую
объект. По умолчанию toString() не принимает
Параметры, то есть конвертирует все примитивные виды в string.
``` js 
let text=99;
console.log(typeof text.toString()) // нам выведет 99 только с типом string
``` 
3. concat() - Метод concat() соединяет две или более строк. Тем
concat() возвращает новую строку. Команда concat()
не изменяет исходную строку.
``` js 
let text1= 'izzy'
let text='hello'
console.log(text1.concat(" ", text)); // izzy hello
``` 

4. trim() - Метод trim() удаляет пробелы в обоих случаях
стороны предложений. Метод trim() не изменяет внутри исходной строки только справа и слева.
``` js 
let text='           izzy        '
console.log(text.trim()) // izzy
```
5. includes()- Метод includes() возвращает true, если строка содержит
указанная строка. В противном случае он возвращает false. 
``` js 
let text='hello world'
let result=text.includes('izzy')
console.log(result) // false, because in text we dont have izzy
```
6. indexOf() and lastIndexOf() - Метод indexOf() возвращает позицию
первого вхождения значения в строку. Метод indexOf()
возвращает -1, если значение не найдено. Метод
indexOf() чувствителен к регистру.
LastIndexOf- берет последную букву и выводит его индекс.
``` js 
let text='hello world'
console.log(text.indexOf('w')) // 6
console.log(text.indexOf('lo')) // 3
console.log(text.indexOf('f')) // -1
``` 
7. replace() - Метод replace() возвращает новую строку с замененными
значениями. Метод replace() ищет
строку на предмет значения или регулярного выражения. Метод replace() не изменяет исходную строку
``` js 
let text='izzy'
console.log(text.replace('izzy', 'izzat')) // izzat 
```
8. substring() and slice() - работают они одинаково только вот принимает отрицательные числа. Метод substring(start,end) извлекает символы,
между двумя индексами (позициями), из строки и
возвращает подстроку. Метод substring() извлекает
символы от начала до конца (исключая). Метод substring()
не изменяет исходную строку. Если начало
больше конца, аргументы меняются местами: (4, 1) = (1, 4).
Значения начала или конца меньше 0 обрабатываются как 0
``` js 
let text='hello world'
console.log(text.substring(1,4)) // ell 

let text='hello world'
console.log(text.slice(-5,-1)) // orld 
``` 
9. toUpperCase() and toLowercase - аппер выводит все слова с большой буквы, а ловер с маленькими, все различие между ними.
``` js 
let text='IzIIz'
console.log(text.toUpperCase())// IZIIZ


let text='IzIIz'
console.log(text.toLowerCase())// iziiz
```

10. И наверное самая нужная мета это split() - Метод split() разбивает строку на массив подстрок. Метод split() возвращает новый массив. Метод split() не изменяет исходную строку. Если в качестве разделителя используется (" "), строка разбивается между словами.
``` js 
let text="hello izzat how are u"
console.log(text.split()) // все предложение возьмет в один элемент массива ["hello izzat how are u"]

console.log(text.split(" ")) // тут уже все предложение делит пробелы, так что тут оно каждый слово берет как отдельный элемент массива ["hello", 'izzat', ' how ', 'are', 'u']

console.log(text.split("")) // тут уже каждую букву берет как отдельный элемент массива.
``` 

*Также внутри могут быть разные элементы и исходя из этих элементов этот метод будет делить их на отдельные части массива. Сверху я показал только пробел, исходя из пробела наш текст делился на части в массиве.*


# *Cпасибо за внимание*
