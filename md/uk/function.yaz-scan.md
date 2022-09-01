---
navigation:
  - function.yaz-scan-result.html: « yazscanresult
  - function.yaz-schema.html: yazschema »
  - index.html: PHP Manual
  - ref.yaz.html: Функции YAZ
title: yazscan
---
# yazscan

(PHP 4> = 4.0.5, PECL yaz> = 0.9.0)

yazscan — Підготовка сканування

### Опис

```methodsynopsis
yaz_scan(    resource $id,    string $type,    string $startterm,    array $flags = ?): void
```

Функція готує запит сканування для встановленого з'єднання протоколу Z39.50.

Щоб надіслати запит сканування на сервер і отримати відповідь, потрібно викликати функцію [yazwait()](function.yaz-wait.html). Як запевняють [yazwait()](function.yaz-wait.html) викличте [yazerror()](function.yaz-error.html) для отримання помилки та [yazscanresult()](function.yaz-scan-result.html) для отримання результату.

### Список параметрів

`id`

Дескриптор з'єднання, повернутий [yazconnect()](function.yaz-connect.html)

`type`

В даний час підтримується тільки `rpn`

`startterm`

Початковий елемент для сканування

Форма, в якій представлений початковий елемент сканування, задається параметром `type`

Синтаксис цього параметра схожий на запит RPN, який описаний для [yazsearch()](function.yaz-search.html). Він складається з нуля чи більше операторних налаштувань `@attr`, За якими слідує єдина лексема.

`flags`

Цей необов'язковий параметр визначає додаткову інформацію для керування поведінкою сканування. З масиву прапорів доступні три індекси: `number` (кількість термів, що запитуються), `position` (позиція терма) та `stepSize` (Розмір кроку).

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Функція PHP, яка сканує заголовки**

```php
<?php
function scan_titles($id, $startterm)
{
  yaz_scan($id, "rpn", "@attr 1=4 " . $startterm);
  yaz_wait();
  $errno = yaz_errno($id);
  if ($errno == 0) {
    $ar = yaz_scan_result($id, $options);
    echo 'Scan ok; ';
    foreach ($options as $key => $val) {
      echo "$key = $val ";
    }
    echo '<br /><table>';
    while (list($key, list($k, $term, $tcount)) = each($ar)) {
      if (empty($k)) continue;
      echo "<tr><td>$term</td><td>$tcount</td></tr>";
    }
    echo '</table>';
  } else {
    echo "Сканирование не удалось. Ошибка: " . yaz_error($id) . "<br />";
  }
}
?>
```
