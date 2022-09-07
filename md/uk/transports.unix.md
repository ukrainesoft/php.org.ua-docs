---
navigation:
  - transports.inet.md: 'Інтернет-сокети: TCP, UDP, SSL та TLS'
  - types.comparisons.md: Таблица сравнения типов в PHP »
  - index.md: PHP Manual
  - transports.md: Список підтримуваних транспортних протоколів
title: 'Unix-сокети: UNIX та UDG'
---
## Unix-сокети: UNIX та UDG

`unix://` і `udg://`

-   `unix:///tmp/mysock`
-   `udg:///tmp/mysock`

`unix://` дає можливість використовувати unix-сокети, а `udg://` надає альтернативний спосіб передачі даних у них, з використанням протоколу користувача датаграм.

Unix-сокети, на відміну від Інтернет-сокетів, не вимагають вказівки порту. В разі [fsockopen()](function.fsockopen.md) параметр `portno` повинен дорівнювати 0.

> **Зауваження**: Unix-сокети не підтримуються у Windows.
