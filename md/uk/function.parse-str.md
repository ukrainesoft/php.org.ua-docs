Розбирає рядок на змінні

-   [« ord](function.ord.html)
    
-   [print »](function.print.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы со строками](ref.strings.html)
    
-   Розбирає рядок на змінні
    

# parsestr

(PHP 4, PHP 5, PHP 7, PHP 8)

parsestr — Розбирає рядок на змінні

### Опис

```methodsynopsis
parse_str(string $string, array &$result): void
```

Розбирає рядок `string`, яка повинна мати формат рядка запиту URL і надає значення змінним у поточному контексті (або заносить до масиву, якщо заданий параметр `result`

### Список параметрів

`string`

Вхідний рядок.

`result`

Якщо вказано другий параметр `result`, то замість присвоєння змінних у поточному контексті вони будуть збережені в цьому параметрі як елементи масиву.

**Увага**

Використовувати цю функцію без параметра `result` конче *НЕ РЕКОМЕНДУЄТЬСЯ*. Подібне використання оголошено *Застарілим* з PHP 7.2. Починаючи з PHP 8.0.0, параметр `result` є *обов'язковим*

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | `result` більше не є необов'язковим. |
|  | Використання **parsestr()** без другого параметра буде викликати помилку рівня **`E_DEPRECATED`** |

### Приклади

**Приклад #1 Використання **parsestr()****

```php
<?php
$str = "first=value&arr[]=foo+bar&arr[]=baz";

// Рекомендуемый подход
parse_str($str, $output);
echo $output['first'];  // value
echo $output['arr'][0]; // foo bar
echo $output['arr'][1]; // baz

// НЕ РЕКОМЕНДУЕТСЯ
parse_str($str);
echo $first;  // value
echo $arr[0]; // foo bar
echo $arr[1]; // baz
?>
```

Так як імена змінних PHP не можуть містити пробіли та точки, ці символи будуть замінені символом підкреслення. Такі ж правила накладаються на імена ключів у масиві `result`якщо він заданий.

**Приклад #2 Співвідношення імен **parsestr()****

```php
<?php
parse_str("My Value=Something");
echo $My_Value; // Something

parse_str("My Value=Something", $output);
echo $output['My_Value']; // Something
?>
```

### Примітки

> **Зауваження**
> 
> Усі змінні створюються (або заносяться до масиву) вже оброблені функцією [urldecode()](function.urldecode.html)

> **Зауваження**
> 
> Для отримання поточної `QUERY_STRING`, можна використовувати змінну [$\_SERVER\['QUERY\_STRING'\]](reserved.variables.server.html). Крім того, можливо ви захочете прочитати розділ про [переменных вне PHP](language.variables.external.html)

### Дивіться також

-   [parse\_url()](function.parse-url.html) - Розбирає URL та повертає його компоненти
-   [pathinfo()](function.pathinfo.html) - Повертає інформацію про шлях до файлу
-   [http\_build\_query()](function.http-build-query.html) - Генерує URL-кодований рядок запиту
-   [urldecode()](function.urldecode.html) - Декодування URL-кодованого рядка