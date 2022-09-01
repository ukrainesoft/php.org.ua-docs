---
navigation:
  - ref.yaz.md: « Функции YAZ
  - function.yaz-ccl-conf.html: yazcclconf »
  - index.md: PHP Manual
  - ref.yaz.md: Функции YAZ
title: yazaddinfo
---
# yazaddinfo

(PHP 4> = 4.0.1, PECL yaz> = 0.9.0)

yazaddinfo — Повертає додаткову інформацію у разі виникнення помилки

### Опис

```methodsynopsis
yaz_addinfo(resource $id): string
```

Повертає додаткову інформацію у разі виникнення помилки останнього запиту до сервера.

З деякими серверами ця функція може повернути той самий рядок, що і функція [yazerror()](function.yaz-error.html)

### Список параметрів

`id`

Дескриптор з'єднання, що повертається функцією [yazconnect()](function.yaz-connect.html)

### Значення, що повертаються

Рядок містить додаткову інформацію про помилку або порожнє значення, якщо остання операція пройшла успішно або немає додаткової інформації від сервера.

### Дивіться також

-   [yazerror()](function.yaz-error.html) - Повертає опис помилки
-   [yazerrno()](function.yaz-errno.html) - Повертає номер помилки
