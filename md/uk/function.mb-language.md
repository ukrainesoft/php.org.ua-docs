Встановлює/отримує поточну мову

-   [« mb\_internal\_encoding](function.mb-internal-encoding.html)
    
-   [mb\_list\_encodings »](function.mb-list-encodings.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с многобайтовыми строками](ref.mbstring.html)
    
-   Встановлює/отримує поточну мову
    

# мбlanguage

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

мбlanguage — Встановлює/отримує поточну мову

### Опис

```methodsynopsis
mb_language(?string $language = null): string|bool
```

Встановлює/отримує поточну мову.

### Список параметрів

`language`

Використовується для кодування електронних листів. Допустимі мови перелічені в наступній таблиці.[mb\_send\_mail()](function.mb-send-mail.html) використовує параметр для кодування електронної пошти.

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
| Спрощена китайська мова/zh-cn | ХЗ | BASE64 |  |
| Традиційна китайська мова/zh-tw | BIG-5 | BASE64 |  |

### Значення, що повертаються

Якщо аргумент `language` заданий та `language` має допустиме значення, функція повертає **`true`**. Інакше вона поверне **`false`**. Якщо `language` опущений або дорівнює **`null`**, функція поверне поточне значення мови як рядка (string).

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер параметр `language` може набувати значення **`null`** |

### Дивіться також

-   [mb\_send\_mail()](function.mb-send-mail.html) - Надсилання закодованого повідомлення