---
navigation:
  - function.runkit7-method-rename.html: « runkit7methodrename
  - function.runkit7-superglobals.html: runkit7superglobals »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7objectід
---
# runkit7objectід

(PECL runkit7> = Unknown)

runkit7objectid — Повертає дескриптор цілого об'єкта для цього об'єкта

### Опис

```methodsynopsis
runkit7_object_id(object $obj): int
```

Функція еквівалентна [splobjectid()](function.spl-object-id.html)

Ця функція повертає унікальний ідентифікатор об'єкта. Ідентифікатор об'єкта є унікальним протягом усього часу існування об'єкта. Після знищення об'єкта його ідентифікатор може бути повторно використано інших об'єктів. Поведінка схожа на [splobjecthash()](function.spl-object-hash.html)

### Список параметрів

`obj`

Будь-який об'єкт.

### Значення, що повертаються

Цілочисельний ідентифікатор, унікальний для кожного об'єкта, що існує в даний момент, і завжди однаковий для кожного об'єкта.

### Примітки

> **Зауваження**
> 
> Коли об'єкт знищено, його ідентифікатор може бути використаний для інших об'єктів.

### Дивіться також

-   [splobjectid()](function.spl-object-id.html) - Отримати цілісний ідентифікатор об'єкта
