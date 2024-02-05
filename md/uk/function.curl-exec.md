---
navigation:
  - function.curl-escape.md: « curl\_escape
  - function.curl-getinfo.md: curl\_getinfo »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_exec
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_exec

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

curl\_exec — Виконує запит cURL

### Опис

```methodsynopsis
curl_exec(CurlHandle $handle): string|bool
```

Запрошує cURL.

Ця функція повинна бути викликана після ініціалізації сеансу та встановлення всіх необхідних параметрів.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curl\_init()](function.curl-init.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Однак, якщо [встановлена](function.curl-setopt.md)опция\*\*`CURLOPT_RETURNTRANSFER`\*\*, при успішному завершенні буде повернено результат, а при невдачі - **`false`**

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Логічний тип](language.types.boolean.md)Используйте[оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

> **Зауваження** :
> 
> Зверніть увагу, що коди стану відповіді, що вказують на помилки (наприклад, `404 Not found`), не розглядаються як невдача. Функція [curl\_getinfo()](function.curl-getinfo.md) може використовуватись для перевірки таких помилок.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |

### Приклади

**Приклад #1 Завантаження веб-сторінки**

```php
<?php
// создание нового cURL ресурса
$ch = curl_init();

// установка URL и других необходимых параметров
curl_setopt($ch, CURLOPT_URL, "http://www.example.com/");
curl_setopt($ch, CURLOPT_HEADER, 0);

// загрузка страницы и выдача её браузеру
curl_exec($ch);

// завершение сеанса и освобождение ресурсов
curl_close($ch);
?>
```

### Дивіться також

-   [curl\_multi\_exec()](function.curl-multi-exec.md) \- Запускає приєднання поточного дескриптора cURL
