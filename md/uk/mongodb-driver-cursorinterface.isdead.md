Перевірити, чи можна ще отримати з курсору результати

-   [« MongoDB\\Driver\\CursorInterface::getServer](mongodb-driver-cursorinterface.getserver.html)
    
-   [MongoDB\\Driver\\CursorInterface::setTypeMap »](mongodb-driver-cursorinterface.settypemap.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\CursorInterface](class.mongodb-driver-cursorinterface.html)
    
-   Перевірити, чи можна ще отримати з курсору результати
    

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

Повертає **`true`**якщо запитати черговий результат не вийде або **`false`**якщо він ще "живий".

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Cursor::isDead()](mongodb-driver-cursor.isdead.html) - Перевіряє, чи курсор вичерпано чи може містити додаткові результати