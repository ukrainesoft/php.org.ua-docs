---
navigation:
  - filters.string.md: « Рядкові фільтри
  - filters.compression.md: Компресійні фільтри »
  - index.md: PHP Manual
  - filters.md: Список доступних фільтрів
title: Перетворюючі фільтри
---
## Перетворюючі фільтри

Як і фільтри string.фільтри convert. вчиняють дії, що відповідають їхнім іменам. Для отримання додаткової інформації про конкретний фільтр зверніться до сторінки посібника відповідної функції.

## convert.base64-encode та convert.base64-decode

Використання цих фільтрів еквівалентно обробці всіх даних потоку функціями [base64encode()](function.base64-encode.md) і [base64decode()](function.base64-decode.md) відповідно . `convert.base64-encode` підтримує аргументи, передані як асоціативного масиву. Якщо вказано аргумент `line-length`, результат base64 буде поділений на шматки довгої `line-length` символи кожен. Якщо вказано аргумент `line-break-chars`, кожен шматок буде поділено вказаними символами. Ці параметри дають такий самий ефект, як і використання [base64encode()](function.base64-encode.md) у парі з [chunksplit()](function.chunk-split.md)

**Приклад #1 convert.base64-encode та convert.base64-decode**

```php
<?php
$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'convert.base64-encode');
fwrite($fp, "This is a test.\n");
fclose($fp);
/* Выведет:  VGhpcyBpcyBhIHRlc3QuCg==  */

$param = array('line-length' => 8, 'line-break-chars' => "\r\n");
$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'convert.base64-encode', STREAM_FILTER_WRITE, $param);
fwrite($fp, "This is a test.\n");
fclose($fp);
/* Выведет:  VGhpcyBp
          :  cyBhIHRl
          :  c3QuCg==  */

$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'convert.base64-decode');
fwrite($fp, "VGhpcyBpcyBhIHRlc3QuCg==");
fclose($fp);
/* Выведет:  This is a test.  */
?>
```

## convert.quoted-printable-encode та convert.quoted-printable-decode

Використання decode-версії цього фільтра еквівалентно обробці всіх даних потоку функцією [quotedprintabledecode()](function.quoted-printable-decode.md). Фільтр `convert.quoted-printable-encode` немає еквівалентної функції . `convert.quoted-printable-encode` підтримує аргументи, передані як асоціативного масиву. На додаток до аргументів, що підтримуються `convert.base64-encode` `convert.quoted-printable-encode` також підтримує boolean-аргументи `binary` і `force-encode-first`. . `convert.base64-decode` підтримує лише аргумент `line-break-chars` як підказка для чищення закодованих даних.

**Приклад #2 convert.quoted-printable-encode & convert.quoted-printable-decode**

```php
<?php
$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'convert.quoted-printable-encode');
fwrite($fp, "This is a test.\n");
/* Выведет:  =This is a test.=0A  */
?>
```

## convert.iconv.

Фільтри `convert.iconv.*` доступні, якщо включена підтримка [iconv](book.iconv.md) та їх використання аналогічно обробці потокових даних за допомогою [iconv()](function.iconv.md). Ці фільтри не підтримують параметри. Натомість очікується, що вихідне та цільове кодування були задані в імені фільтра таким чином: `convert.iconv.<input-encoding>.<output-encoding>` або `convert.iconv.<input-encoding>/<output-encoding>` (обидва варіанти семантично еквівалентні).

**Приклад # 3 convert.iconv.**

```php
<?php
$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'convert.iconv.utf-16le.utf-8');
fwrite($fp, "T\0h\0i\0s\0 \0i\0s\0 \0a\0 \0t\0e\0s\0t\0.\0\n\0");
fclose($fp);
/* Выведет: This is a test. */
?>
```
