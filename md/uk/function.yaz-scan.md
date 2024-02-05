---
navigation:
  - function.yaz-scan-result.md: « yaz\_scan\_result
  - function.yaz-schema.md: yaz\_schema »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_scan
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_scan

(PHP 4 >= 4.0.5, PECL yaz >= 0.9.0)

yaz\_scan — Підготовка сканування

### Опис

```methodsynopsis
yaz_scan(    resource $id,    string $type,    string $startterm,    array $flags = ?): void
```

Функція готує запит сканування для встановленого з'єднання протоколу Z39.50.

Щоб надіслати запит сканування на сервер і отримати відповідь, потрібно викликати функцію [yaz\_wait()](function.yaz-wait.md). Як запевняють [yaz\_wait()](function.yaz-wait.md) викличте [yaz\_error()](function.yaz-error.md)для получения ошибки и[yaz\_scan\_result()](function.yaz-scan-result.md)для получения результата.

### Список параметрів

`id`

Дескриптор з'єднання, повернутий [yaz\_connect()](function.yaz-connect.md)

`type`

В даний час підтримується тільки `rpn`

`startterm`

Початковий елемент для сканування

Форма, в якій представлений початковий елемент сканування, задається параметром `type`

Синтаксис цього параметра схожий на запит RPN, який описаний для [yaz\_search()](function.yaz-search.md). Він складається з нуля чи більше операторних налаштувань `@attr`, За якими слідує єдина лексема.

`flags`

Цей необов'язковий параметр визначає додаткову інформацію для керування поведінкою сканування. З масиву прапорів доступні три індекси: `number` (кількість термів, що запитуються), `position`(позиция терма) и`stepSize`(размер шага).

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Функція PHP, яка сканує заголовки**

```php
<?php
function scan_titles($id, $startterm)
{
  yaz_scan($id, "rpn", "@attr 1=4 " . $startterm);
  yaz_wait();
  $errno = yaz_errno($id);
  if ($errno == 0) {
    $ar = yaz_scan_result($id, $options);
    echo 'Scan ok; ';
    foreach ($options as $key => $val) {
      echo "$key = $val ";
    }
    echo '<br /><table>';
    while (list($key, list($k, $term, $tcount)) = each($ar)) {
      if (empty($k)) continue;
      echo "<tr><td>$term</td><td>$tcount</td></tr>";
    }
    echo '</table>';
  } else {
    echo "Сканирование не удалось. Ошибка: " . yaz_error($id) . "<br />";
  }
}
?>
```
