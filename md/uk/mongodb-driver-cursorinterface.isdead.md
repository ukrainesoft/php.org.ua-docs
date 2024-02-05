---
navigation:
  - mongodb-driver-cursorinterface.getserver.md: '« MongoDB\\Driver\\CursorInterface::getServer'
  - mongodb-driver-cursorinterface.settypemap.md: 'MongoDB\\Driver\\CursorInterface::setTypeMap »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursorinterface.md: MongoDB\\Driver\\CursorInterface
title: 'MongoDB\\Driver\\CursorInterface::isDead'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\CursorInterface::isDead

(mongodb >=1.6.0)

MongoDB\\Driver\\CursorInterface::isDead — Перевірити, чи можна ще отримати з курсору результати

### Опис

```methodsynopsis
abstract public MongoDB\Driver\CursorInterface::isDead(): bool
```

Перевіряє, чи можна спробувати отримати з курсору результати. Спочатку курсор знаходиться в статусі "живий" (alive), але в наступних випадках може перейти в статус "мертвий" (dead):

-   При черговому вичитуванні не хвостового курсора не було повернено документ
-   Виникла помилка
-   Курсор прочитав останній батч до завершення
-   Курсор досяг встановленого ліміту

Це насамперед корисно під час роботи з хвостовими курсорами.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо запитати черговий результат не вийде або \*\*`false`\*\*якщо він ще "живий".

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Cursor::isDead()](mongodb-driver-cursor.isdead.md) \- Перевіряє, чи курсор вичерпано чи може містити додаткові результати
