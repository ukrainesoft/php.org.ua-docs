---
navigation:
  - parallel-runtime.construct.md: '« parallel\\Runtime::\_\_construct'
  - parallel-runtime.close.md: 'parallel\\Runtime::close »'
  - index.md: PHP Manual
  - class.parallel-runtime.md: parallel\\Runtime
title: 'parallel\\Runtime::run'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Runtime::run

(0.8.0)

parallel\\Runtime::run — Виконання

### Опис

```methodsynopsis
public parallel\Runtime::run(Closure $task): ?Future
```

Планує паралельне виконання `task`

```methodsynopsis
public parallel\Runtime::run(Closure $task, array $argv): ?Future
```

Планує паралельне виконання `task`, передавая`argv` під час виконання.

### Список параметрів

`task`

Замикання ([Closure](class.closure.md)) зі специфічними характеристиками.

`argv`

Масив (array) аргументів із конкретними характеристиками, які будуть передані `task` під час виконання.

### Характеристики задачі

Замикання, заплановані для паралельного виконання, не повинні:

-   приймати або повертати значення за посиланням
-   приймати чи повертати внутрішні об'єкти (дивіться примітки)
-   виконувати обмежений набір інструкцій

У замиканнях, призначених для паралельного виконання, заборонено такі інструкції:

-   yield
-   use by-reference
-   declare class
-   declare named function

> **Зауваження** :
> 
> Вкладені замикання можуть використовувати yield або передачу значення посилання, але не повинні містити оголошення класів або іменованих функцій.

> **Зауваження** :
> 
> Жодні інструкції не заборонені у файлах, які можуть включати завдання.

### Аргументи характеристик

Аргументи не повинні:

-   містити посилання
-   утримувати ресурси
-   містити внутрішні об'єкти (дивіться примітки)

> **Зауваження** :
> 
> У разі ресурсів файлового потоку ресурс буде перетворено на файловий дескриптор і передано як ціле число (int), де це можливо, не підтримується у Windows.

### Примітки до внутрішніх об'єктів

Внутрішні об'єкти зазвичай використовують структуру, що налаштовується, яку не можна безпечно скопіювати за значенням, в PHP в даний час відсутній механізм для цього (без серіалізації), і тому можуть використовуватися тільки об'єкти, які не використовують структуру, що налаштовується.

Деякі внутрішні об'єкти не використовують структуру, що настроюється, наприклад, [parallel\\Events\\Event](class.parallel-events-event.md) і тому можуть використовуватись спільно.

Замикання - це особливий вид внутрішнього об'єкта, який підтримує копіювання за значенням, тому може використовуватись спільно.

Канали відіграють ключову роль у написанні паралельного коду і за потреби підтримують одночасний доступ і виконання, тому можуть використовуватися спільно.

**Увага**

Користувальницький клас, що розширює внутрішній клас, може використовувати структуру, що налаштовується, визначену внутрішнім класом, і в цьому випадку вони не можуть бути безпечно скопійовані за значенням і тому не можуть використовуватися спільно.

### Значення, що повертаються

**Увага**

Не можна ігнорувати повертається [parallel\\Future](class.parallel-future.md)якщо завдання містить оператор return або throw.

### Винятки

**Увага**

Викидає parallel\\Runtime\\Error\\Closed, якщо [parallel\\Runtime](class.parallel-runtime.md) було закрито.

**Увага**

Викидає parallel\\Runtime\\Error\\IllegalFunction, если`task` є замиканням, створеним із внутрішньої функції.

**Увага**

Викидає parallel\\Runtime\\Error\\IllegalInstruction, если`task` містить неприпустимі інструкції.

**Увага**

Викидає parallel\\Runtime\\Error\\IllegalParameter, если`task` приймає або `argv` містить неприпустимі змінні.

**Увага**

Викидає parallel\\Runtime\\Error\\IllegalReturn, если`task` повертається некоректно.
