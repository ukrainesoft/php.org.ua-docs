---
navigation:
  - function.yaz-record.html: « yazrecord
  - function.yaz-scan.html: yazscan »
  - index.md: PHP Manual
  - ref.yaz.md: Функции YAZ
title: yazscanresult
---
# yazscanresult

(PHP 4> = 4.0.5, PECL yaz> = 0.9.0)

yazscanresult — Повернення результату запиту сканування

### Опис

```methodsynopsis
yaz_scan_result(resource $id, array &$result = ?): array
```

**yazscanresult()** повертає терми та асоційовану з ними інформацію, отримані з сервера останнім викликом функції [yazscan()](function.yaz-scan.md)

### Список параметрів

`id`

Дескриптор з'єднання, повернутий [yazconnect()](function.yaz-connect.md)

`result`

Якщо заданий, цей масив міститиме додаткову інформацію із запиту сканування:

-   `number` - Кількість повернутих елементів
    
-   `stepsize` - Розмір кроку
    
-   `position` - Позиція терму
    
-   `status` - Статус сканування
    

### Значення, що повертаються

Повертає масив (0..n-1), де n - кількість повернутих термів. Кожне значення масиву є парою, перший елемент якої - терм, другий - кількість результатів.
