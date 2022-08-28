Перевіряє результат Extended Service

-   [« yaz\_error](function.yaz-error.html)
    
-   [yaz\_es »](function.yaz-es.html)
    
-   [PHP Manual](index.html)
    
-   [Функции YAZ](ref.yaz.html)
    
-   Перевіряє результат Extended Service
    

# yazесresult

(PHP 4> = 4.2.0, PECL yaz> = 0.9.0)

yazесresult — Перевіряє результат Extended Service

### Опис

```methodsynopsis
yaz_es_result(resource $id): array
```

Функція перевіряє останній повернутий сервером результат Extended Service. Extended Service ініціюється або за допомогою **yazitemorder()**, або за допомогою [yaz\_es()](function.yaz-es.html)

### Список параметрів

`id`

Ідентифікатор підключення, що повертається [yaz\_connect()](function.yaz-connect.html)

### Значення, що повертаються

Повертає масив із елементом `targetReference` для посилання на операцію Extended Service (згенерованої та повернутої з сервера).

### Дивіться також

-   [yaz\_es()](function.yaz-es.html) - готує Extended Service Request