---
navigation:
  - ref.yaz.md: « Функції YAZ
  - function.yaz-ccl-conf.md: yaz\_ccl\_conf »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_addinfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_addinfo

(PHP 4 >= 4.0.1, PECL yaz >= 0.9.0)

yaz\_addinfo — Повертає додаткову інформацію у разі виникнення помилки

### Опис

```methodsynopsis
yaz_addinfo(resource $id): string
```

Повертає додаткову інформацію у разі виникнення помилки останнього запиту до сервера.

З деякими серверами ця функція може повернути той самий рядок, що і функція [yaz\_error()](function.yaz-error.md)

### Список параметрів

`id`

Дескриптор з'єднання, що повертається функцією [yaz\_connect()](function.yaz-connect.md)

### Значення, що повертаються

Рядок містить додаткову інформацію про помилку або порожнє значення, якщо остання операція пройшла успішно або немає додаткової інформації від сервера.

### Дивіться також

-   [yaz\_error()](function.yaz-error.md) \- Повертає опис помилки
-   [yaz\_errno()](function.yaz-errno.md) \- Повертає номер помилки
