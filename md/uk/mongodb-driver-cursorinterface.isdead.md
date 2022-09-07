---
navigation:
  - mongodb-driver-cursorinterface.getserver.md: '« MongoDBDriverCursorInterface::getServer'
  - mongodb-driver-cursorinterface.settypemap.md: 'MongoDBDriverCursorInterface::setTypeMap »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursorinterface.md: MongoDBDriverCursorInterface
title: 'MongoDBDriverCursorInterface::isDead'
---
# MongoDBDriverCursorInterface::isDead

(mongodb >=1.6.0)

MongoDBDriverCursor Interface::is Dead — Перевірити, чи можна ще отримати з курсора результати

### Опис

```methodsynopsis
abstract public MongoDB\Driver\CursorInterface::isDead(): bool
```

Перевіряє, чи можна спробувати отримати з курсору результати. Спочатку курсор перебуває у статусі "живий" (alive), але в наступних випадках може перейти в статус "мертвий" (dead):

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

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDBDriverCursor::isDead()](mongodb-driver-cursor.isdead.md) - Перевіряє, чи курсор вичерпано чи може містити додаткові результати
