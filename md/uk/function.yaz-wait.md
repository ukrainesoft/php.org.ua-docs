---
navigation:
  - function.yaz-syntax.html: « yazsyntax
  - book.zmq.md: Обмін повідомленнями 0MQ »
  - index.md: PHP Manual
  - ref.yaz.md: Функции YAZ
title: yazwait
---
# yazwait

(PHP 4> = 4.0.1, PECL yaz> = 0.9.0)

yazwait — Очікує на виконання запитів Z39.50 серверами

### Опис

```methodsynopsis
yaz_wait(array &$options = ?): mixed
```

Функція виконує мережну (блокуючу) дію до завершення запиту, підготовленого функціями [yazconnect()](function.yaz-connect.html) [yazsearch()](function.yaz-search.html) [yazpresent()](function.yaz-present.html) [yazscan()](function.yaz-scan.html) and [yazitemorder()](function.yaz-itemorder.md)

**yazwait()** припиняє роботу та повертає результат після того, як усі сервери або завершать виконання всіх запитів або перервуть їх (у разі помилок).

### Список параметрів

`options`

Асоціативний масив параметрів:

`timeout`

Встановлює час очікування за секунди. Якщо сервер не відповідає після цього часу, він вважається неробочим і **yazwait()** припиняє роботу. За замовчуванням очікування становить 15 секунд.

`event`

Має логічний тип.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо встановлено параметр event, повертає ресурс або **`false`** у разі виникнення помилки.
