---
navigation:
  - function.curl-reset.html: « curlreset
  - function.curl-setopt.html: curlsetopt »
  - index.md: PHP Manual
  - ref.curl.md: Функции cURL
title: curlsetoptarray
---
# curlsetoptarray

(PHP 5> = 5.1.3, PHP 7, PHP 8)

curlsetoptarray — Встановлює кілька параметрів для сеансу cURL

### Опис

```methodsynopsis
curl_setopt_array(CurlHandle $handle, array $options): bool
```

Встановлює кілька параметрів для сеансу URL. Ця функція корисна під час встановлення великої кількості cURL-параметрів без необхідності постійно викликати [curlsetopt()](function.curl-setopt.md)

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curlinit()](function.curl-init.md)

`options`

Масив (array), що визначає параметри, що встановлюються, і їх значення. Ключі мають бути коректними константами для функції [curlsetopt()](function.curl-setopt.md) або їх цілими еквівалентами.

### Значення, що повертаються

Повертає **`true`**, якщо всі параметри успішно встановлено. Якщо не вдалося успішно встановити будь-який параметр, негайно повертається значення **`false`**, а наступні параметри в масиві `options` будуть проігноровані.

### список змін

| Версия | Описание |
| --- | --- |
|  | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |

### Приклади

**Приклад #1 Ініціалізація нової сесії cURL та завантаження веб-сторінки**

```php
<?php
// создание нового ресурса cURL
$ch = curl_init();

// установка URL и других соответствующих параметров
$options = array(CURLOPT_URL => 'http://www.example.com/',
                 CURLOPT_HEADER => false
                );

curl_setopt_array($ch, $options);

// загрузка URL и её выдача в браузер
curl_exec($ch);

// закрытие ресурса cURL и освобождение системных ресурсов
curl_close($ch);
?>
```

### Примітки

> **Зауваження**
> 
> Як і при роботі з [curlsetopt()](function.curl-setopt.md), передача масиву в параметр **`CURLOPT_POST`** закодує всі дані за допомогою *multipart/form-data*, тоді як передача URL-кодованого рядка використовуватиме кодування *application/x-www-form-urlencoded*

### Дивіться також

-   [curlsetopt()](function.curl-setopt.md) - Встановлює параметр для сеансу CURL
