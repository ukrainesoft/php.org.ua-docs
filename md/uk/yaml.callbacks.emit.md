- [« Callback-функції парсингу](yaml.callbacks.parse.md)
- [Функції Yaml»](ref.yaml.md)

- [PHP Manual](index.md)
- [Callback-функції](yaml.callbacks.md)
- Публікуючі callback-функції

## Публікуючі callback-функції

Публікуючі callback-функції викликаються тоді, коли за допомогою
[yaml_emit()](function.yaml-emit.md) або
[yaml_emit_file()](function.yaml-emit-file.md) публікуються екземпляри
зареєстрованих класів. У функцію передається об'єкт, що публікується.
Callback-функція має повернути масив із двома ключами: "`tag`" та
"'Data". Значення, пов'язане з ключом "tag" має бути рядком,
містить тег YAML для виведення. Значення, пов'язане з ключем "data"
має бути закодовано як YAML та опубліковано замість перехопленого
об'єкт.

**Приклад #1 Приклад публікуючої callback-функції**

`<?phpclass EmitExample {  public $data; // дані мусять бути зрозумілого pecl/yaml типу  public function __construct ($d) {    $this->data = $d; }  /**   * Публікуюча callback-функція Yaml. *   * Ожидается возвращение массива с двумя значениями 2:   *   - 'tag': пользовательский тег для этой сериализации   *   - 'data': значение для преобразование в yaml (массив, строка, логическое, число)   *   * @param object $obj Публикуемый объект * @return array Тег и замещающие данные для публикации   */  public static function yamlEmit (EmitExample $obj) {    return array(      'tag' => '!example/emit',      'data' => $obj->data,    ); }}$emit_callbacks = array( 'EmitExample' => array('EmitExample', 'yamlEmit'));$t = new EmitExample(array('a','b','c'));$yaml = (  array(   'example' => $t,  ), YAML_ANY_ENCODING, YAML_ANY_BREAK, $emit_callbacks);var_dump($yaml);?> `

Результатом виконання цього прикладу буде щось подібне:

string(43) "---
example: !example/emit
- a
- b
- c
...
"
