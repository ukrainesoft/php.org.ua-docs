Публікуючі callback-функції

-   [« Callback-функции парсинга](yaml.callbacks.parse.html)
    
-   [Функции Yaml »](ref.yaml.html)
    
-   [PHP Manual](index.html)
    
-   [Callback-функции](yaml.callbacks.html)
    
-   Публікуючі callback-функції
    

## Публікуючі callback-функції

Публікуючі callback-функції викликаються тоді, коли за допомогою [yaml\_emit()](function.yaml-emit.html) або [yaml\_emit\_file()](function.yaml-emit-file.html) публікуються екземпляри зареєстрованих класів. У функцію передається об'єкт, що публікується. Callback-функція повинна повернути масив із двома ключами: "`tag`"і"`data`". Значення, пов'язане з ключем"`tag`" має бути рядком, що містить тег YAML для виведення. Значення, пов'язане з ключем "`data`" повинно бути закодовано як YAML та опубліковано замість перехопленого об'єкта.

**Приклад #1 Приклад публікуючої callback функції**

```php
<?php
class EmitExample {
  public $data;    // данные должны быть понятного pecl/yaml типа

  public function __construct ($d) {
    $this->data = $d;
  }

  /**
   * Публикующая callback-функция Yaml.
   *
   * Ожидается возвращение массива с двумя значениями 2:
   *   - 'tag': пользовательский тег для этой сериализации
   *   - 'data': значение для преобразование в yaml (массив, строка, логическое, число)
   *
   * @param object $obj Публикуемый объект
   * @return array Тег и замещающие данные для публикации
   */
  public static function yamlEmit (EmitExample $obj) {
    return array(
      'tag' => '!example/emit',
      'data' => $obj->data,
    );
  }
}

$emit_callbacks = array(
  'EmitExample' => array('EmitExample', 'yamlEmit')
);

$t = new EmitExample(array('a','b','c'));
$yaml = yaml_emit(
  array(
    'example' => $t,
  ),
  YAML_ANY_ENCODING,
  YAML_ANY_BREAK,
  $emit_callbacks
);
var_dump($yaml);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(43) "---
example: !example/emit
- a
- b
- c
...
"
```