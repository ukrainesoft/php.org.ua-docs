- [«mb_detect_encoding](function.mb-detect-encoding.md)
- [mb_encode_mimeheader »](function.mb-encode-mimeheader.md)

- [PHP Manual](index.md)
- [Функції для роботи з багатобайтовими рядками](ref.mbstring.md)
- Встановлення/отримання списку кодувань для механізмів визначення
кодування

#mb_detect_order

(PHP 4 \>= 4.0.6, PHP 5, PHP 7, PHP 8)

mb_detect_order — Встановлення/отримання списку кодувань для механізмів
визначення кодування

### Опис

**mb_detect_order**(array\|string\|null `$encoding` = **`null`**):
array\|bool

В `encoding` задається порядок, у якому механізми автоматичного
визначення кодувань їх перевірятимуть.

### Список параметрів

`encoding`
`encoding` - масив (array) або рядок, в якому перераховані кодування
через кому. Дивіться [Підтримувані кодування](mbstring.supported-encodings.md).

Якщо 'encoding' опущений, функція поверне поточний список кодувань як
масиву.

Ця установка впливає на роботу функцій
[mb_detect_encoding()](function.mb-detect-encoding.md) та
[mb_send_mail()](function.mb-send-mail.md).

В `mbstring` на даний момент реалізовані наступні фільтри для
визначення кодувань. Якщо послідовність байт у вихідному рядку не
буде відповідати жодному з перерахованих кодувань, визначення
кодування завершиться невдачею.

`UTF-8`, `UTF-7`, `ASCII`, `EUC-JP`, `SJIS`, `eucJP-win`, `SJIS-win`,
`JIS`, `ISO-2022-JP`

Кодування ISO-8859-*, mbstring завжди визначає як ISO-8859-*.

Для кодувань `UTF-16`, `UTF-32`, `UCS2` та `UCS4` автоматичне
визначення завжди завершуватиметься невдачею.

### Значення, що повертаються

При установці порядку визначення кодування, залежно від
успішності, повертає **`true`** або **`false`**.

При отриманні порядку визначення кодування повертається
відсортований масив кодувань.

### Список змін

| Версія | Опис                                                     |
|--------|----------------------------------------------------------|
| 8.0.0  | Тепер параметр encoding може набувати значення **null**. |

### Приклади

**Приклад #1 Приклад використання **mb_detect_order()****

` <?php/* Установка порядку визначення в виді упорядкованого списку */mb_detect_order("eucjp-win,sjis-win,UTF-8");/* Установка списку кодувань в від  ;$ary[] = "JIS";$ary[] = "EUC-JP";mb_detect_order($ary);/* Висновок поточного списку кодувань */echo implode(", ", mb_detect_order

**Приклад #2 Приклад марного порядку визначення**

; Завжди визначає як ISO-8859-1
detect_order = ISO-8859-1, UTF-8

; Завжди визначає як UTF-8, тому що ASCII/UTF-7
; є підмножиною UTF-8
detect_order = UTF-8, ASCII, UTF-7

### Дивіться також

- [mb_internal_encoding()](function.mb-internal-encoding.md) -
Встановлення/отримання внутрішнього кодування скрипту
- [mb_http_input()](function.mb-http-input.md) - Визначення
кодування символів вхідних даних HTTP-запиту
- [mb_http_output()](function.mb-http-output.md) -
Встановлення/отримання кодування символів виводу HTTP
- [mb_send_mail()](function.mb-send-mail.md) - Надсилання
закодованого повідомлення
