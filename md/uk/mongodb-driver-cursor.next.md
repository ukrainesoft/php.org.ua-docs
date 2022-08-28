Переміщує курсор на наступний результат

-   [« MongoDB\\Driver\\Cursor::key](mongodb-driver-cursor.key.html)
    
-   [MongoDB\\Driver\\Cursor::rewind »](mongodb-driver-cursor.rewind.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.html)
    
-   Переміщує курсор на наступний результат
    

# MongoDBDriverCursor::next

(mongodb >=1.9.0)

MongoDBDriverCursor::next — Переміщує курсор на наступний результат

### Опис

```methodsynopsis
public MongoDB\Driver\Cursor::next(): void
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Зсув поточної позиції до наступного результату в курсорі.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток [MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.html)
-   У разі невдалої аутентифікації кидає виняток [MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.html)

### Дивіться також

-   [Iterator::next()](iterator.next.html) - Переходить до наступного елементу