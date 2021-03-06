- [«Філософія](philosophy.parallel.md)
- [parallel.ootstrap »](parallel.bootstrap.md)

- [PHP Manual](index.md)
- [parallel](book.parallel.md)
- функціональний API

# Функціональний API

API [parallel\Runtime](class.parallel-runtime.md) забезпечує високу
ступінь контролю для досвідчених програмістів PHP і тих, хто добре знайомий
з написанням додатків, які використовують паралельні процеси.

Функціональний API забезпечує менший контроль в обмін на можливість
приймати рішення для програміста:

- всі виконувані середовища виконання завантажуються однаково

- планування визначається API, а не програмістом

[Parallel\run()](parallel.run.md) забезпечує гарантію того, що
завдання почне виконуватися паралельно, як тільки це дозволено
обмеженнями обладнання та операційної системи, без непотрібного
створення середовищ виконання. Для більшості програм слід віддавати
перевага функціональному API.

## Зміст

- [parallel ootstrap](parallel.bootstrap.md) — Початкове завантаження
- [Parallel\run](parallel.run.md) — Виконання
