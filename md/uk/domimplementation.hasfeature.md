- [« DOMImplementation::createDocumentType](domimplementation.createdocumenttype.md)
- [DOMNamedNodeMap »](class.domnamednodemap.md)

- [PHP Manual](index.md)
- [DOMImplementation](class.domimplementation.md)
- Перевірка, чи реалізована певна можливість у реалізації DOM

# DOMImplementation::hasFeature

(PHP 5, PHP 7, PHP 8)

DOMImplementation::hasFeature — Перевірка, чи реалізована певна
можливість у реалізації DOM

### Опис

public **DOMImplementation::hasFeature**(string `$feature`, string
`$version`): bool

Перевіряє, чи реалізує специфічну можливість `feature` реалізація
DOM.

Ви можете знайти список усіх можливостей у розділі
[» Узгодження](http://www.w3.org/TR/2000/REC-DOM-Level-2-Core-20001113/introduction.md#ID-Conformance)
стандарту DOM.

### Список параметрів

`feature`
Тестована можливість.

`version`
Номер версії тестованої можливості `feature`. У DOM level 2 це може бути
бути або `2.0`, або `1.0`.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Помилки

До PHP 8.0.0 метод *може* викликатись статично, але викличе помилку
**`E_DEPRECATED`**. Починаючи з PHP 8.0.0, виклик цього методу статично
викидає виняток [Error](class.error.md).

### Приклади

**Приклад #1 Тестування вашої реалізації DOM**

` <?php$features = array(  'Core'           => 'Core module',  'XML'            => 'XML module',  'HTML'           => 'HTML module',  'Views'          => 'Views module',  ' Stylesheets'    => 'Style Sheets module',  'CSS'            => 'CSS module',  'CSS2'           => 'CSS2 module',  'Events'         => 'Events module',  'UIEvents'       => 'User interface Events module ',  'MouseEvents'    => 'Mouse Events module',  'MutationEvents' => 'Mutation Events module',  'HTMLEvents'     => 'HTML Events module',  'Range'          => 'Range module',  'Traversal'      => 'Traversal module');foreach ($features as $key => $name) {  if (DOMImplementation::hasFeature($key, '2.0')) {    echo "Реалізує$
";  } else {    echo "Можливість $name відсутня
";  }}?> `

### Дивіться також

- [DOMNode::isSupported()](domnode.issupported.md) - Перевіряє,
чи підтримується можливість у певній версії
