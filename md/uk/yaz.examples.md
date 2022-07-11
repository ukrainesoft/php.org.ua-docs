- [«Зумовлені константи](yaz.constants.md)
- [Функції YAZ »](ref.yaz.md)

- [PHP Manual](index.md)
- [YAZ](book.yaz.md)
- Приклади

# Приклади

PHP/YAZ зберігає список з'єднань з адресатами (Z-Асоціація). Ресурс же
надає з'єднання з адресатом.

Приклад нижче демонструє особливість паралельного пошуку API. Якщо
аргументи не передано, виводиться форма запиту; інакше (передані
аргументи) відбувається пошук за адресами, вказаними в масиві `host`.

**Приклад #1 Паралельний пошук за допомогою Yaz**

` <?php$host=$_REQUEST[host];$query=$_REQUEST[query];$num_hosts = count($host);if (empty($query) || count($host) == 0) { echo '<form method="get">    <input type="checkbox"    name="host[]"value="bagel.indexdata.dk/gils" />        "Тест []" value="localhost:9999/Default" />        Локальний тест| Бібліотека Конгресу                        <<<<< >    ';} else {    echo 'Ви шукали ' . htmlspecialchars($query) . '<br />'; for ($i = 0; $i < $num_hosts; $i++) {        $id[] = yaz_connect($host[$i]); yaz_syntax($id[$i], "usmarc"); yaz_range($id[$i], 1, 10); yaz_search($id[$i], "rpn", $query); }   yaz_wait(); for ($i = 0; $i < $num_hosts; $i++) {        echo '<hr />' . $host[$i] . ':'; $error==yaz_error($id[$i]); if (!empty($error)) {             echo "Помилка: $error"; } else {             $hits = yaz_hits($id[$i]); echo "Всього результатів $hits"; }        echo '<dl>'; for ($p = 1; $p <= 10;$$++) {            $rec = yaz_record($id[$i], $p, "string"); if (empty($rec)) continue; echo "<dt><b>$p</b></dt><dd>"; echo nl2br($rec); echo "</dd>"; }        echo '</dl>'; }}?> `
