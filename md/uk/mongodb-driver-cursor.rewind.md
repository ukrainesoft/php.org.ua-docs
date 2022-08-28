Переміщує курсор до першого результату

-   [« MongoDB\\Driver\\Cursor::next](mongodb-driver-cursor.next.html)
    
-   [MongoDB\\Driver\\Cursor::setTypeMap »](mongodb-driver-cursor.settypemap.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.html)
    
-   Переміщує курсор до першого результату
    

# MongoDBDriverCursor::rewind

(mongodb >=1.9.0)

MongoDBDriverCursor::rewind — Переміщує курсор до першого результату

### Опис

```methodsynopsis
public MongoDB\Driver\Cursor::rewind(): void
```

Якщо курсор просунувся далі своєї першої позиції, його перемістити до першого результату не вийде.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`null`**

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток [MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.html)
-   У разі невдалої аутентифікації кидає виняток [MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.html)
-   Кидає виняток [MongoDB\\Driver\\Exception\\LogicException](class.mongodb-driver-exception-logicexception.html) якщо метод був викликаний після просування курсору далі за свою першу позицію.

### Дивіться також

-   [Iterator::rewind()](iterator.rewind.html) – Повертає ітератор на перший елемент