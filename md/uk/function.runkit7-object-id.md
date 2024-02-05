---
navigation:
  - function.runkit7-method-rename.md: « runkit7\_method\_rename
  - function.runkit7-superglobals.md: runkit7\_superglobals »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7\_object\_id
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# runkit7\_object\_id

(PECL runkit7 >= Unknown)

runkit7\_object\_id — Повертає дескриптор цілого об'єкта для цього об'єкта

### Опис

```methodsynopsis
runkit7_object_id(object $obj): int
```

Функція еквівалентна [spl\_object\_id()](function.spl-object-id.md)

Ця функція повертає унікальний ідентифікатор об'єкта. Ідентифікатор об'єкта є унікальним протягом усього часу існування об'єкта. Після знищення об'єкта його ідентифікатор може бути повторно використано інших об'єктів. Поведінка схожа на [spl\_object\_hash()](function.spl-object-hash.md)

### Список параметрів

`obj`

Будь-який об'єкт.

### Значення, що повертаються

Цілочисельний ідентифікатор, унікальний для кожного об'єкта, що існує в даний момент, і завжди однаковий для кожного об'єкта.

### Примітки

> **Зауваження** :
> 
> Коли об'єкт знищено, його ідентифікатор може бути використаний для інших об'єктів.

### Дивіться також

-   [spl\_object\_id()](function.spl-object-id.md) \- Отримати цілісний ідентифікатор об'єкта
