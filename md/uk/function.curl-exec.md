---
navigation:
  - function.curl-escape.md: « curlescape
  - function.curl-file-create.md: curlfilecreate »
  - index.md: PHP Manual
  - ref.curl.md: Функции cURL
title: curlexec
---
# curlexec

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

curlexec — Виконує запит cURL

### Опис

```methodsynopsis
curl_exec(CurlHandle $handle): string|bool
```

Запрошує cURL.

Ця функція повинна викликатись після ініціалізації сеансу та встановлення всіх необхідних параметрів.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curlinit()](function.curl-init.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Однак, якщо [установлена](function.curl-setopt.md) опція **`CURLOPT_RETURNTRANSFER`**, при успішному завершенні буде повернено результат, а при невдачі - **`false`**

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.md). Використовуйте [оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

> **Зауваження**
> 
> Зверніть увагу, що коди стану відповіді, що вказують на помилки (наприклад, `404 Not found`), не розглядаються як невдача. Функція [curlgetinfo()](function.curl-getinfo.md) може використовуватись для перевірки таких помилок.

### список змін

| Версия | Описание |
| --- | --- |
|  | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |

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

-   [curlmultiexec()](function.curl-multi-exec.md) - Запускає приєднання поточного дескриптора cURL
