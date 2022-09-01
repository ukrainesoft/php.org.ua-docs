---
navigation:
  - function.ssh2-scp-send.html: « ssh2scpsend
  - function.ssh2-sftp-chmod.html: ssh2sftpchmod »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2sendeof
---
# ssh2sendeof

(PECL ssh2> = 1.3)

ssh2sendeof - Відправляє EOF в потік

### Опис

```methodsynopsis
ssh2_send_eof(resource $channel): bool
```

Відправляє EOF у потік; зазвичай використовується для закриття стандартного введення, зберігаючи при цьому висновок та помилку. Наприклад, можна відправити дистанційному процесу деякі дані через стандартне введення, закрити його, щоб почати обробку, і як і раніше мати можливість зчитувати результати без створення додаткових файлів.

### Список параметрів

`channel`

Потік SSH; можна отримати за допомогою таких функцій, як [ssh2fetchstream()](function.ssh2-fetch-stream.html) або [ssh2connect()](function.ssh2-connect.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ssh2fetchstream()](function.ssh2-fetch-stream.md) - отримання розширеного потоку даних
