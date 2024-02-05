---
navigation:
  - function.yaz-record.md: « yaz\_record
  - function.yaz-scan.md: yaz\_scan »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_scan\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_scan\_result

(PHP 4 >= 4.0.5, PECL yaz >= 0.9.0)

yaz\_scan\_result — Повернення результату сканування.

### Опис

```methodsynopsis
yaz_scan_result(resource $id, array &$result = ?): array
```

**yaz\_scan\_result()** повертає терми та асоційовану з ними інформацію, отримані з сервера останнім викликом функції [yaz\_scan()](function.yaz-scan.md)

### Список параметрів

`id`

Дескриптор з'єднання, повернутий [yaz\_connect()](function.yaz-connect.md)

`result`

Якщо заданий, цей масив міститиме додаткову інформацію із запиту сканування:

-   `number`\- Кількість повернутих елементів
    
-   `stepsize`\- Розмір кроку
    
-   `position`\- Позиція Терма
    
-   `status`\- Статус сканування
    

### Значення, що повертаються

Повертає масив (0..n-1), де n - кількість повернутих термів. Кожне значення масиву є парою, перший елемент якої - терм, другий - кількість результатів.
