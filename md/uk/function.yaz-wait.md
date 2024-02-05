---
navigation:
  - function.yaz-syntax.md: « yaz\_syntax
  - book.zmq.md: Обмін повідомленнями 0MQ »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_wait
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_wait

(PHP 4 >= 4.0.1, PECL yaz >= 0.9.0)

yaz\_wait — Очікує на виконання запитів Z39.50 серверами

### Опис

```methodsynopsis
yaz_wait(array &$options = ?): mixed
```

Функція виконує мережну (блокуючу) дію до завершення запиту, підготовленого функціями [yaz\_connect()](function.yaz-connect.md) [yaz\_search()](function.yaz-search.md) [yaz\_present()](function.yaz-present.md) [yaz\_scan()](function.yaz-scan.md)and[yaz\_itemorder()](function.yaz-itemorder.md)

**yaz\_wait()** припиняє роботу та повертає результат після того, як усі сервери або завершать виконання всіх запитів або перервуть їх (у разі помилок).

### Список параметрів

`options`

Асоціативний масив параметрів:

`timeout`

Встановлює час очікування за секунди. Якщо сервер не відповідає після цього часу, він вважається неробочим і \*\*yaz\_wait()\*\*прекращает работу. По умолчанию ожидание составляет 15 секунд.

`event`

Має логічний тип.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`**в случае возникновения ошибки. В случае, если установлен параметр event, возвращает ресурс или**`false`\*\*в случае возникновения ошибки.
