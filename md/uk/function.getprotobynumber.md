Отримує ім'я протоколу за номером

-   [« getprotobyname](function.getprotobyname.html)
    
-   [getservbyname »](function.getservbyname.html)
    
-   [PHP Manual](index.html)
    
-   [Мережеві функції](ref.network.html)
    
-   Отримує ім'я протоколу за номером
    

# getprotobynumber

(PHP 4, PHP 5, PHP 7, PHP 8)

getprotobynumber — Отримує ім'я протоколу за номером

### Опис

```methodsynopsis
getprotobynumber(int $protocol): string|false
```

Функція **getprotobynumber()** повертає ім'я протоколу за номером, вказаним у параметрі `protocol` згідно з /etc/protocols.

### Список параметрів

`protocol`

Номер протоколу.

### Значення, що повертаються

Повертає ім'я протоколу у вигляді рядка або **`false`** у разі виникнення помилки.

### Дивіться також

-   [getprotobyname()](function.getprotobyname.html) - Отримує номер протоколу на ім'я