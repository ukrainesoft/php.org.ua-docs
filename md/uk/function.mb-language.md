---
navigation:
  - function.mb-internal-encoding.md: « mb\_internal\_encoding
  - function.mb-list-encodings.md: mb\_list\_encodings »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_language
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_language

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_language — Встановлює/отримує поточну мову

### Опис

```methodsynopsis
mb_language(?string $language = null): string|bool
```

Встановлює/отримує поточну мову.

### Список параметрів

`language`

Функцією кодують повідомлення електронної пошти. Допустимі мови перелічені в наступній таблиці. Функція [mb\_send\_mail()](function.mb-send-mail.md) використовує параметр для кодування електронної пошти.

| Язык | Кодировка | Кодирование | Псевдоним |
| --- | --- | --- | --- |
| Німецька мова/de (German) | ISO-8859-15 | Quoted-Printable | Німецька мова (Deutsch) |
| Англійська мова/en | ISO-8859-1 | Quoted-Printable |  |
| Вірменська мова/hy | ArmSCII-8 | Quoted-Printable |  |
| Японська мова/ja | ISO-2022-JP | BASE64 |  |
| Корейська мова/ko | ISO-2022-KR | BASE64 |  |
| neutral | UTF-8 | BASE64 |  |
| Російська мова/ua | KOI8-R | Quoted-Printable |  |
| Турецька мова/tr | ISO-8859-9 | Quoted-Printable |  |
| Українська мова/ua | KOI8-U | Quoted-Printable |  |
| uni | UTF-8 | BASE64 | Універсальний |
| Спрощена китайська мова/zh-cn | HZ | BASE64 |  |
| Традиційна китайська мова/zh-tw | BIG-5 | BASE64 |  |

### Значення, що повертаються

Якщо параметр `language` заданий та припустимо, функція повертає **`true`**. Інакше вона поверне **`false`**. Якщо параметр `language` опущений або дорівнює **`null`**, функція поверне поточне значення мови як рядка (string).

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер параметр `language` може набувати значення **`null`** |

### Дивіться також

-   [mb\_send\_mail()](function.mb-send-mail.md) \- Надсилає закодований електронний лист
