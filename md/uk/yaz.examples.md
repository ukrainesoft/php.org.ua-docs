---
navigation:
  - yaz.constants.md: « Обумовлені константи
  - ref.yaz.md: Функции YAZ »
  - index.md: PHP Manual
  - book.yaz.md: YAZ
title: Приклади
---
# Приклади

PHP/YAZ зберігає список з'єднань з адресатами (Z-Асоціація). Ресурс надає з'єднання з адресатом.

Приклад нижче демонструє особливість паралельного пошуку API. Якщо аргументи не передано, виводиться форма запиту; інакше (передані аргументи) відбувається пошук за адресами, вказаними у масиві `host`

**Приклад #1 Паралельний пошук за допомогою Yaz**

```php
<?php
$host=$_REQUEST[host];
$query=$_REQUEST[query];
$num_hosts = count($host);
if (empty($query) || count($host) == 0) {
    echo '<form method="get">
    <input type="checkbox"
    name="host[]" value="bagel.indexdata.dk/gils" />
        Тест GILS
    <input type="checkbox"
    name="host[]" value="localhost:9999/Default" />
        Локальный тест
    <input type="checkbox" checked="checked"
    name="host[]" value="z3950.loc.gov:7090/voyager" />
        Библиотека Конгресса
    <br />
    Запрос RPN:
    <input type="text" size="30" name="query" />
    <input type="submit" name="action" value="Поиск" />
    </form>
    ';
} else {
    echo 'Вы искали ' . htmlspecialchars($query) . '<br />';
    for ($i = 0; $i < $num_hosts; $i++) {
        $id[] = yaz_connect($host[$i]);
        yaz_syntax($id[$i], "usmarc");
        yaz_range($id[$i], 1, 10);
        yaz_search($id[$i], "rpn", $query);
    }
    yaz_wait();
    for ($i = 0; $i < $num_hosts; $i++) {
        echo '<hr />' . $host[$i] . ':';
        $error = yaz_error($id[$i]);
        if (!empty($error)) {
            echo "Ошибка: $error";
        } else {
            $hits = yaz_hits($id[$i]);
            echo "Всего результатов $hits";
        }
        echo '<dl>';
        for ($p = 1; $p <= 10; $p++) {
            $rec = yaz_record($id[$i], $p, "string");
            if (empty($rec)) continue;
            echo "<dt><b>$p</b></dt><dd>";
            echo nl2br($rec);
            echo "</dd>";
        }
        echo '</dl>';
    }
}
?>
```
