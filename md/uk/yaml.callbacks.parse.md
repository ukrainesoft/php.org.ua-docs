Callback-функції парсингу

-   [« Callback-функции](yaml.callbacks.html)
    
-   [Публікуючі callback-функції »](yaml.callbacks.emit.html)
    
-   [PHP Manual](index.html)
    
-   [Callback-функции](yaml.callbacks.html)
    
-   Callback-функції парсингу
    

## Callback-функції парсингу

Callback-функцій (callback) для парсингу викликається функціями [yamlparse()](function.yaml-parse.html) [yamlparsefile()](function.yaml-parse-file.html) або [yamlparseurl()](function.yaml-parse-url.html) для виявлення зареєстрованого тега YAML. У callback-функцію передається значення тегованого запису, сам тег та прапори, що визначають скалярний тип запису. Функція Callback повинна повернути дані, які парсер YAML повинен використовувати для цього запису.

**Приклад #1 Приклад використання callback-функції парсингу**

```php
<?php
/**
 * Callback-функция парсинга для тегов yaml.
 * @param mixed $value Данные из файла yaml
 * @param string $tag Тег, для которого срабатывает функция
 * @param int $flags Стиль скаляра записи (смотрите YAML_*_SCALAR_STYLE)
 * @return mixed Значение, которое должен выдать парсер YAML
 */
function tag_callback ($value, $tag, $flags) {
  var_dump(func_get_args()); // отладка
  return "Hello {$value}";
}

$yaml = <<<YAML
greeting: !example/hello World
YAML;

$result = yaml_parse($yaml, 0, $ndocs, array(
    '!example/hello' => 'tag_callback',
  ));

var_dump($result);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(3) {
  [0]=>
  string(5) "World"
  [1]=>
  string(14) "!example/hello"
  [2]=>
  int(1)
}
array(1) {
  ["greeting"]=>
  string(11) "Hello World"
}
```