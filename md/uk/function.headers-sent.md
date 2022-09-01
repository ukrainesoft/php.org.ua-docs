---
navigation:
  - function.headers-list.html: « headerslist
  - function.http-response-code.html: httpresponsecode »
  - index.html: PHP Manual
  - ref.network.html: Мережеві функції
title: headerssent
---
# headerssent

(PHP 4, PHP 5, PHP 7, PHP 8)

headerssent — Перевіряє, чи надіслано заголовки.

### Опис

```methodsynopsis
headers_sent(string &$filename = null, int &$line = null): bool
```

Перевіряє, чи надіслано заголовки.

Не можна надіслати додаткові рядки заголовків за допомогою функції [header()](function.header.html), якщо заголовки вже надіслано. Використовуючи цю функцію, можна попередити помилки, пов'язані з заголовками HTTP. Іншим варіантом є використання [буферизації висновку](ref.outcontrol.html)

### Список параметрів

`filename`

Якщо задані додаткові параметри `filename` і `line`, то функція **headerssent()** помістить ім'я вихідного файлу PHP та номер рядка, з якого починається виведення в змінні `filename` і `line`

`line`

Номер рядка, з якого починається виведення.

### Значення, що повертаються

Функція **headerssent()** поверне **`false`**, якщо HTTP-заголовки не були надіслані, або **`true`** якщо відправлені.

### Приклади

**Приклад #1 Приклад використання **headerssent()****

```php
<?php

// Если не было отправлено ни одного заголовка, то отправить один
if (!headers_sent()) {
    header('Location: http://www.example.com/');
    exit;
}

// Пример использования необязательных параметров file и line.
// Необходимо отметить, что $filename и $linenum передаются для дальнейшего использования.
// Не присваивайте им значения заранее.
if (!headers_sent($filename, $linenum)) {
    header('Location: http://www.example.com/');
    exit;

// Скорее всего, ошибка будет происходит здесь.
} else {

    echo "Заголовки уже были отправлены в $filename в строке $linenum\n" .
          "Невозможно перенаправить, пожалуйста, передите по этой <a " .
          "href=\"http://www.example.com\">ссылке</a>\n";
    exit;
}

?>
```

### Примітки

> **Зауваження**
> 
> Доступ до заголовків та їх висновок здійснюватиметься лише у випадку, якщо у SAPI є їх підтримка.

### Дивіться також

-   [проstart()](function.ob-start.html) - Включення буферизації виводу
-   [triggererror()](function.trigger-error.html) - Викликає помилку користувача/попередження/повідомлення
-   [headerslist()](function.headers-list.html) - Повертає список переданих заголовків (або готових до відправлення)
-   Дивіться інформацію щодо функції [header()](function.header.html) - Надсилання HTTP-заголовка для більш детальної інформації.
