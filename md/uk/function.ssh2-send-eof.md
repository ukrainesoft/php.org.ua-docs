---
navigation:
  - function.ssh2-scp-send.md: « ssh2\_scp\_send
  - function.ssh2-sftp-chmod.md: ssh2\_sftp\_chmod »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_send\_eof
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_send\_eof

(PECL ssh2 >= 1.3)

ssh2\_send\_eof - Відправляє EOF в потік

### Опис

```methodsynopsis
ssh2_send_eof(resource $channel): bool
```

Відправляє EOF у потік; зазвичай використовується для закриття стандартного введення, зберігаючи при цьому висновок та помилку. Наприклад, можна відправити дистанційному процесу деякі дані через стандартне введення, закрити його, щоб почати обробку, і як і раніше мати можливість зчитувати результати без створення додаткових файлів.

### Список параметрів

`channel`

Потік SSH; можна отримати за допомогою таких функцій, як [ssh2\_fetch\_stream()](function.ssh2-fetch-stream.md) або [ssh2\_connect()](function.ssh2-connect.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ssh2\_fetch\_stream()](function.ssh2-fetch-stream.md) \- отримання розширеного потоку даних
