---
navigation:
  - wddx.examples.md: « Приклади
  - ref.wddx.md: Функції WDDX »
  - index.md: PHP Manual
  - wddx.examples.md: Приклади
title: Приклади wddx
---
## Приклади wddx

Всі функції, що серіалізують змінні, використовують перший елемент масиву для визначення, у що повинен бути серіалізований масив, масив або структуру. Якщо перший елемент має рядковий ключ, тоді він буде серіалізований у структуру, інакше масив.

**Приклад #1 Серіалізація одного значення за допомогою WDDX**

```php
<?php
echo wddx_serialize_value("PHP to WDDX packet example", "PHP packet");
?>
```

Цей приклад створює:

```
<wddxPacket version='1.0'><header comment='PHP packet'/><data>
<string>PHP to WDDX packet example</string></data></wddxPacket>
```

**Приклад #2 Використання інкрементальних пакетів WDDX**

```php
<?php
$pi = 3.1415926;
$packet_id = wddx_packet_start("PHP");
wddx_add_vars($packet_id, "pi");

/* Предпожим, что $cities была заполнена из базы данных */
$cities = array("Austin", "Novato", "Seattle");
wddx_add_vars($packet_id, "cities");

$packet = wddx_packet_end($packet_id);
echo $packet;
?>
```

Цей приклад створює:

```
<wddxPacket version='1.0'><header comment='PHP'/><data><struct>
<var name='pi'><number>3.1415926</number></var><var name='cities'>
<array length='3'><string>Austin</string><string>Novato</string>
<string>Seattle</string></array></var></struct></data></wddxPacket>
```

> **Зауваження**
> 
> Рядки повинні бути закодовані в UTF-8; Для роботи з іншими кодуваннями спочатку перетворіть рядок за допомогою функції [мбconvertencoding()](function.mb-convert-encoding.html) [UConverter::transcode()](uconverter.transcode.md) або [iconv()](function.iconv.md)
