- [« Аргументи функції](functions.arguments.md)
- [Звернення до функцій через змінні »](functions.variable-functions.md)

- [PHP Manual](index.md)
- [Функції](language.functions.md)
- Повернення значень

## Повернення значень

Значення повертаються за допомогою необов'язкового оператора.
Значення, що повертаються, можуть бути будь-якого типу, в тому числі це можуть бути
масиви та об'єкти. Повернення призводить до завершення виконання функції та
передачі управління назад до того рядка коду, в якому дана функція
була викликана. Для отримання більш детальної інформації ознайомтеся з
описом [return](function.return.md).

> **Примітка**:
>
> Якщо конструкція [return](function.return.md) не вказана, функція
> поверне значення **`null`**.

### Використання виразу return

**Приклад #1 Використання конструкції [return](function.return.md)**

`<?phpfunction square($num){    return $num * $num;}echo square(4); // виводить '16'.?> `

Функція не може повертати кілька значень, але аналогічного
результату можна досягти, повертаючи масив.

**Приклад #2 Повернення кількох значень як масиву**

`<?phpfunction small_numbers(){    return [0, 1, 2];}// Деструктуризація масиву буде збирати кожний елемент масиву індивідуально[$zero, s єдиною еквівалентною альтернативою було використання конструкції list().list($zero, $one, $two) = small_numbers();?> `

Для того щоб функція повертала результат за посиланням, вам необхідно
використовувати оператор & при описі функції, і при присвоєнні
змінної значення, що повертається:

**Приклад #3 Повернення результату за посиланням**

` <?phpfunction &returns_reference(){    return $someref;}$newref =& returns_reference();?> `

Для отримання більш детальної інформації про посилання зверніться до розділу
документації [Докладно про посилання](language.references.md).
