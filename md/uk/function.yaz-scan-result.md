Повертає результат запиту сканування

-   [« yaz\_record](function.yaz-record.html)
    
-   [yaz\_scan »](function.yaz-scan.html)
    
-   [PHP Manual](index.html)
    
-   [Функции YAZ](ref.yaz.html)
    
-   Повертає результат запиту сканування
    

# yazscanresult

(PHP 4> = 4.0.5, PECL yaz> = 0.9.0)

yazscanresult — Повернення результату запиту сканування

### Опис

```methodsynopsis
yaz_scan_result(resource $id, array &$result = ?): array
```

**yazscanresult()** повертає терми та асоційовану з ними інформацію, отримані з сервера останнім викликом функції [yaz\_scan()](function.yaz-scan.html)

### Список параметрів

`id`

Дескриптор з'єднання, повернутий [yaz\_connect()](function.yaz-connect.html)

`result`

Якщо заданий, цей масив міститиме додаткову інформацію із запиту сканування:

-   `number` - Кількість повернутих елементів
    
-   `stepsize` - Розмір кроку
    
-   `position` - Позиція терму
    
-   `status` - Статус сканування
    

### Значення, що повертаються

Повертає масив (0..n-1), де n - кількість повернутих термів. Кожне значення масиву є парою, перший елемент якої - терм, другий - кількість результатів.