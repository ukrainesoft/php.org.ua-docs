---
navigation:
  - function.stream-filter-prepend.md: « streamfilterprepend
  - function.stream-filter-remove.md: streamfilterremove »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: streamfilterregister
---
# streamfilterregister

(PHP 5, PHP 7, PHP 8)

streamfilterregister — реєструє потоковий фільтр, визначений користувачем

### Опис

```methodsynopsis
stream_filter_register(string $filter_name, string $class): bool
```

**streamfilterregister()** дозволяє реалізувати власний фільтр для будь-якого зареєстрованого потоку, що використовується з усіма іншими функціями файлової системи (такими як [fopen()](function.fopen.md) [fread()](function.fread.md) і т.д.).

### Список параметрів

`filter_name`

Назва фільтру, що реєструється.

`class`

Щоб реалізувати фільтр, вам потрібно визначити клас як розширення [phpuserfilter](class.php-user-filter.md) c цілим рядом функцій-членів. При виконанні операцій читання/запису на потоці, до якого прикріплений ваш фільтр, PHP передаватиме дані через ваш фільтр (і через будь-які інші фільтри, прикріплені до потоку), так що дані можуть бути змінені як потрібно. Вам необхідно реалізувати методи точно як описано в [phpuserfilter](class.php-user-filter.md). Інша реалізація призведе до непередбачуваної поведінки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

**streamfilterregister()** повертатиме \*\*`false`\*\*якщо фільтр з ім'ям `filter_name` вже визначено.

### Приклади

**Приклад #1 Фільтр для перекладу букв у верхній регістр у потоці foo-bar.txt**

Приклад нижче реалізує фільтр під назвою `strtoupper` на файловому потоці foo-bar.txt, який буде переводити в великі всі літери, які пишуться/читаються з цього потоку.

```php
<?php

/* Определяем наш класс фильтра */
class strtoupper_filter extends php_user_filter {
  function filter($in, $out, &$consumed, $closing)
  {
    while ($bucket = stream_bucket_make_writeable($in)) {
      $bucket->data = strtoupper($bucket->data);
      $consumed += $bucket->datalen;
      stream_bucket_append($out, $bucket);
    }
    return PSFS_PASS_ON;
  }
}

/* Регистрируем наш фильтр в  PHP */
stream_filter_register("strtoupper", "strtoupper_filter")
    or die("Не удалось зарегистрировать фильтр");

$fp = fopen("foo-bar.txt", "w");

/* Присоединяем зарегистрированный фильтр к только что открытому потоку */
stream_filter_append($fp, "strtoupper");

fwrite($fp, "Line1\n");
fwrite($fp, "Word - 2\n");
fwrite($fp, "Easy As 123\n");

fclose($fp);

/* Читаем содержимое снова
 */
readfile("foo-bar.txt");

?>
```

Результат виконання цього прикладу:

```
LINE1
WORD - 2
EASY AS 123
```

**Приклад #2 Реєстрація стандартного фільтра, що відповідає множинним іменам фільтрів.**

```php
<?php

/* Определяем наш класс фильтра */
class string_filter extends php_user_filter {
  var $mode;

  function filter($in, $out, &$consumed, $closing)
  {
    while ($bucket = stream_bucket_make_writeable($in)) {
      if ($this->mode == 1) {
        $bucket->data = strtoupper($bucket->data);
      } elseif ($this->mode == 0) {
        $bucket->data = strtolower($bucket->data);
      }

      $consumed += $bucket->datalen;
      stream_bucket_append($out, $bucket);
    }
    return PSFS_PASS_ON;
  }

  function onCreate()
  {
    if ($this->filtername == 'str.toupper') {
      $this->mode = 1;
    } elseif ($this->filtername == 'str.tolower') {
      $this->mode = 0;
    } else {
      /* Был вызван какой-то другой фильтр str.*,
         возвращаем ошибку, чтобы  PHP мог продолжить его поиск */
      return false;
    }

    return true;
  }
}

/* Регистрируем наш фильтр в  PHP */
stream_filter_register("str.*", "string_filter")
    or die("Не удалось зарегистрировать фильтр");

$fp = fopen("foo-bar.txt", "w");

/* Присоединяем зарегистрированный фильтр к только что открытому потоку
   Мы могли бы использовать здесь  str.tolower */
stream_filter_append($fp, "str.toupper");

fwrite($fp, "Line1\n");
fwrite($fp, "Word - 2\n");
fwrite($fp, "Easy As 123\n");

fclose($fp);

/* Читаем содержимое снова
 */
readfile("foo-bar.txt");
?>
```

Результат виконання цього прикладу:

```
LINE1
WORD - 2
EASY AS 123
```

### Дивіться також

-   [streamwrapperregister()](function.stream-wrapper-register.md) - реєструє обгортку URL, реалізовану у вигляді PHP-класу
-   [streamfilterappend()](function.stream-filter-append.md) - Прикріпити фільтр до потоку
-   [streamfilterprepend()](function.stream-filter-prepend.md) - Прикріплює фільтр до потоку
