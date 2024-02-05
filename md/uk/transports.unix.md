---
navigation:
  - transports.inet.md: 'Інтернет-сокети: TCP, UDP, SSL і TLS'
  - types.comparisons.md: Таблиці порівняння типів PHP »
  - index.md: PHP Manual
  - transports.md: Список підтримуваних транспортних протоколів
title: 'Unix-сокети: UNIX та UDG'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Unix-сокети: UNIX та UDG

`unix://`и`udg://`

-   `unix:///tmp/mysock`
-   `udg:///tmp/mysock`

`unix://` дає можливість використовувати unix-сокети, а `udg://` надає альтернативний спосіб передачі даних у них, з використанням протоколу користувача датаграм.

Unix-сокети, на відміну від Інтернет-сокетів, не вимагають вказівки порту. В разі [fsockopen()](function.fsockopen.md)параметр`portno` повинен дорівнювати 0.

> **Зауваження**: Unix-сокети не підтримуються у Windows.
