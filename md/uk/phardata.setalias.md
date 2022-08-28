Функція заглушка (Phar::setAlias ​​не можна використовувати для PharData)

-   [« PharData::offsetUnset](phardata.offsetunset.html)
    
-   [PharData::setDefaultStub »](phardata.setdefaultstub.html)
    
-   [PHP Manual](index.html)
    
-   [PharData](class.phardata.html)
    
-   Функція заглушка (Phar::setAlias ​​не можна використовувати для PharData)
    

# PharData::setAlias

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::setAlias ​​— Функція заглушка (Phar::setAlias ​​не можна використовувати для PharData)

### Опис

```methodsynopsis
public PharData::setAlias(string $alias): bool
```

Незапускаються tar/zip-архіви не можуть мати псевдоніма, тому цей метод просто викидає виняток.

### Список параметрів

`alias`

Параметр ігнорується.

### Значення, що повертаються

### Помилки

Викидає виняток [PharException](class.pharexception.html)

### Дивіться також

-   [Phar::setAlias()](phar.setalias.html) - Встановити псевдонім для Phar-архіву