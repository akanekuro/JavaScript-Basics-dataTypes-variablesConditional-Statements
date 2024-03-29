# JavaScript-Basics-dataTypes-variablesConditional-Statements-

#### Переменные
Переменная – это «именованное хранилище» для данных. Мы можем использовать переменные для хранения товаров, посетителей и других данных.

Для создания переменной в JavaScript используйте ключевое слово let.

Приведённая ниже инструкция создаёт (другими словами, объявляет) переменную с именем «message»:
```
let message;
```
Теперь можно поместить в неё данные (другими словами, определить переменную), используя оператор присваивания =:
```
let message;
message = 'Hello'; // сохранить строку 'Hello' в переменной с именем message
```
Языки программирования, в которых такое возможно, называются «динамически типизированными». Это значит, что типы данных есть, но переменные не привязаны ни к одному из них.

Переменные в JavaScript объявляются с использованием ключевого слова var, let или const, за которым следует имя переменной. Например:
```
var age;
let name;
```
var используется для объявления переменных, которые могут быть изменены.
let также используется для объявления переменных, но обладает блочной областью видимости и предпочтительнее var.
const используется для объявления переменных, значения которых не должны изменяться. После присвоения значения переменной с ключевым словом const, ее значение нельзя изменить.

#### Типы данных
JavaScript является слабо типизированным или динамическим языком. Это значит, что вам не нужно определять тип переменной заранее. Тип определится автоматически во время выполнения программы. Также это значит, что вы можете использовать одну переменную для хранения данных различных типов:
```
var foo = 42; // сейчас foo типа Number
foo = "bar"; // а теперь foo типа String
foo = true; // foo становится типа Boolean
```

##### Стандарт ECMAScript определяет 8 типов:
#### 6 типов данных являющихся примитивами:</br>
<pre>
Undefined (Неопределённый тип) : typeof instance === "undefined"</br>
Boolean (Булев, Логический тип) : typeof instance === "boolean"</br>
Number (Число) : typeof instance === "number"</br>
String (Строка) : typeof instance === "string"</br>
BigInt : typeof instance === "bigint"</br>
Symbol (en-US) (в ECMAScript 6) : typeof instance === "symbol"</br>
Null (Null тип ) : typeof instance === "object". Специальный примитив, используемый не только для данных 
но и в качестве указателя на финальную точку в Цепочке Прототипов;</br>
Object (Объект) : typeof instance === "object". Простая структура, используемая не только для хранения данных, 
но и для создания других структур, где любая структура создаётся с использованием ключевого слова new: 
new Object, new Array, new Map (en-US), new Set, new WeakMap, new WeakSet, new Date и множество других структур;

</pre>

#### Булевый тип данных
Булевый тип представляет логическую сущность и имеет два значения: true (истина) и false (ложь). Смотрите Boolean и Boolean для получения подробностей.
#### Null
Этот тип данных имеет всего одно значение: null. Смотрите null и Null для получения подробностей.
#### Undefined
Переменная, которой не было присвоено значение, будет иметь значение undefined. Смотрите undefined и undefined для получения подробностей.
#### Числа
В соответствии со стандартом ECMAScript, существует только один числовой тип, который представляет собой 64-битное число двойной точности согласно стандарту IEEE 754. Другими словами, специального типа для целых чисел в JavaScript нет. Это означает, что при числовых операциях вы можете получить неточное (округлённое) значение. В дополнение к возможности представлять числа с плавающей запятой, есть несколько символических значений: +Infinity (положительная бесконечность), -Infinity (отрицательная бесконечность), и NaN (не число).

# Условное ветвление: if, '?'
Иногда нам нужно выполнить различные действия в зависимости от условий.

Для этого мы можем использовать инструкцию if и условный оператор ?, который также называют оператором «вопросительный знак».

Инструкция «if»
Инструкция if(...) вычисляет условие в скобках и, если результат true, то выполняет блок кода.

Например:
```
let year = prompt('В каком году была опубликована спецификация ECMAScript-2015?', '');

if (year == 2015) alert( 'Вы правы!' );
```
В примере выше, условие – это простая проверка на равенство (year == 2015), но оно может быть и гораздо более сложным.

Преобразование к логическому типу
Инструкция if (…) вычисляет выражение в скобках и преобразует результат к логическому типу.

Давайте вспомним правила преобразования типов из главы Преобразование типов:

Число 0, пустая строка "", null, undefined и NaN становятся false. Из-за этого их называют «ложными» («falsy») значениями.
Остальные значения становятся true, поэтому их называют «правдивыми» («truthy»).
Таким образом, код при таком условии никогда не выполнится:
```
if (0) { // 0 is falsy
  ...
}
```
…а при таком – выполнится всегда:
```
if (1) { // 1 is truthy
  ...
}
```
Несколько условий: «else if»
Иногда нужно проверить несколько вариантов условия. Для этого используется блок else if.

Например:
```
let year = prompt('В каком году была опубликована спецификация ECMAScript-2015?', '');

if (year < 2015) {
  alert( 'Это слишком рано...' );
} else if (year > 2015) {
  alert( 'Это поздновато' );
} else {
  alert( 'Верно!' );
}
```
И так мы можем заметить что мы можем выполнять действия по определенным условиям


# Задание 1 Работа с переменными
Создайте переменную с именем name и присвойте ей ваше имя.</br>
Создайте переменную с именем age и присвойте ей ваш возраст.</br>
Создайте переменную с именем city и присвойте ей название вашего города.</br>
Выведите значения всех трех переменных на экран в виде сообщения в формате:</br>
Воспользуйтесь console.log() для вывода сообщения, включающего ваше имя.</br>
Выведите сообщение, содержащее ваш возраст.</br>
Ожидаемый результат ("Меня зовут [имя], мне [возраст] лет и я живу в городе [город].")</br>

# Задание 2 Типы данных

Задача:
Написать программу, которая определяет типы данных переменных с помощью оператора typeof в JavaScript и выводит результаты на экран.

Требования:
Создать несколько переменных различных типов данных, включая числа, строки, логические значения, массивы, объекты, значение null и неопределенное значение.
Для каждой переменной использовать оператор typeof для определения её типа данных.
Вывести результаты на экран с помощью функции console.log().
Убедиться, что результаты выводятся корректно и отражают типы данных переменных.
```
Результат
Тип данных переменной numberVariable: number
Тип данных переменной stringVariable: string
Тип данных переменной booleanVariable: boolean
Тип данных переменной arrayVariable: object
Тип данных переменной objectVariable: object
Тип данных переменной nullVariable: object
Тип данных переменной undefinedVariable: undefined

```
# Задание 3 Условия
#### 3.1 Напишите условие задания если пользователь старше 18 лет чтобы он выводил в консоль сообщение о том что пользователь старше 18 лет, если нет то сообщение должно быть что он несовершеннолетний 
#### 3.2
```
// Шаг 1: Запрос числа у пользователя
var userInput = prompt("Введите число:");

// Шаг 2: Преобразование строки в число
var number = parseInt(userInput);

// Шаг 3: Проверка числа на четность
if (number % 2 === 0) {
    // Число четное
    alert("Число " + number + " четное.");
} else {
    // Число нечетное
    alert("Число " + number + " нечетное.");
}
```
напишите и попытайтесь понять данный код и написать анлогичный











