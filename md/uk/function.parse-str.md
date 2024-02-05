---
navigation:
  - function.ord.md: « ord
  - function.print.md: print »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: parse\_str
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parse\_str

(PHP 4, PHP 5, PHP 7, PHP 8)

parse\_str — Розбирає рядок на змінні

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

Використовувати цю функцію без параметра `result`крайне*НЕ РЕКОМЕНДУЄТЬСЯ*. Подібне використання оголошено *Застарілим*с PHP 7.2. Начиная с PHP 8.0.0, параметр`result`является*обов'язковим*

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `result` більше не є необов'язковим. |
| 7.2.0 | Использование**parse\_str()** без другого параметра буде викликати помилку рівня **`E_DEPRECATED`** |

### Приклади

**Пример #1 Использование**parse\_str()\*\*\*\*

```php
<?php
$str = "first=value&arr[]=foo+bar&arr[]=baz";

// Рекомендуемый подход
parse_str($str, $output);
echo $output['first'];  // value
echo $output['arr'][0]; // foo bar
echo $output['arr'][1]; // baz

// НЕ РЕКОМЕНДУЕТСЯ
parse_str($str);
echo $first;  // value
echo $arr[0]; // foo bar
echo $arr[1]; // baz
?>
```

Так як імена змінних PHP не можуть містити пробіли та точки, ці символи будуть замінені символом підкреслення. Такі ж правила накладаються на імена ключів у масиві `result`якщо він заданий.

**Приклад #2 Співвідношення імен **parse\_str()****

```php
<?php
parse_str("My Value=Something");
echo $My_Value; // Something

parse_str("My Value=Something", $output);
echo $output['My_Value']; // Something
?>
```

### Примітки

> **Зауваження** :
> 
> Усі змінні створюються (або заносяться до масиву) вже оброблені функцією [urldecode()](function.urldecode.md)

> **Зауваження** :
> 
> Для получения текущей`QUERY_STRING`, можна використовувати змінну [$\_SERVER\['QUERY\_STRING'\]](reserved.variables.server.md). Крім того, можливо ви захочете прочитати розділ про [змінних поза PHP](language.variables.external.md)

### Дивіться також

-   [parse\_url()](function.parse-url.md) \- Розбирає URL та повертає його компоненти
-   [pathinfo()](function.pathinfo.md) \- Повертає інформацію про шлях до файлу
-   [http\_build\_query()](function.http-build-query.md) \- Генерує URL-кодований рядок запиту
-   [urldecode()](function.urldecode.md) \- Декодування URL-кодованого рядка
