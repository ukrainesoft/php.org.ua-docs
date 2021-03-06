- [« Змінні ззовні PHP](language.variables.external.md)
- [Синтаксис »](language.constants.syntax.md)

- [PHP Manual](index.md)
- [Довідник мови](langref.md)
- Константи

# Константи

## Зміст

- [Синтаксис](language.constants.syntax.md)
- [Предвизначені константи](language.constants.predefined.md)
- [Магічні константи](language.constants.magic.md)

Константа – це ідентифікатор (ім'я) для простого значення. Як слід
з назви, це значення не може змінитися під час виконання скрипту
(крім [магічних констант](language.constants.magic.md), які на
насправді є константами). Константи чутливі до регістру.
За прийнятою угодою, імена констант завжди пишуться у верхній
регістрі.

> **Примітка**:
>
> До PHP 8.0.0 константи, визначені за допомогою функції
> [define()](function.define.md), могли бути нечутливими до
> регістру.

Ім'я константи має відповідати тим самим правилам іменування, як і
інші імена у PHP. Правильне ім'я починається з літери чи символу
підкреслення, за яким слідує будь-яка кількість букв, цифр і символів
підкреслення. Регулярний вираз для перевірки правильності імені
константи виглядає так: `^[a-zA-Z_\x80-\xff][a-zA-Z0-9_\x80-\xff]*$`

Можливо визначити константи за допомогою функції
[define()](function.define.md) зарезервованими або навіть
некоректними іменами, значення яких можуть бути отримані лише з
за допомогою [constant()](function.constant.md). Однак, робити це не
рекомендується.

**Підказка**

Дивіться також [Інструкція по імену](userlandnaming.md).

**Приклад #1 Правильні та неправильні імена констант**

` <?php// Правильні імена константdefine("FOO",     "щось");define("FOO2",   "що-то ще");define("FOO_BAR", "що-| / Неправильні імена константdefine("2FOO",   "щось");// Це вірне оголошення, але краще його не використовувати:// PHP одного разуможе зареєструвати на -то ");?> `

> **Примітка**: Поняття "літери" тут - це символи a-z, A-Z та інші
> символи з ASCII кодами від 128 до 255 (0x80-0xff).

Як і [superglobals](language.variables.predefined.md), константи
доступні з будь-якої області видимості. Константи можна використовувати з
будь-якого місця скрипта незалежно від області видимості. Детальну
інформацію про області видимості можна знайти
[тут](language.variables.scope.md).

> **Примітка**: Починаючи з PHP 7.1.0, константі класу можна оголошувати
> видимість захищена або закрита, роблячи її доступною тільки в
> ієрархічної області видимості класу, у якому визначено.
