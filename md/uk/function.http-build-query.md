---
navigation:
  - function.get-meta-tags.md: « getmetatags
  - function.parse-url.md: parseurl »
  - index.md: PHP Manual
  - ref.url.md: Функції URL
title: httpbuildquery
---
# httpbuildquery

(PHP 5, PHP 7, PHP 8)

httpbuildquery — Генерує URL-кодований рядок запиту

### Опис

```methodsynopsis
http_build_query(    array|object $data,    string $numeric_prefix = "",    ?string $arg_separator = null,    int $encoding_type = PHP_QUERY_RFC1738): string
```

Генерує URL-кодований рядок запиту наданого асоціативного (або індексованого) масиву.

### Список параметрів

`data`

Може бути масив чи об'єкт, що містить властивості.

Якщо `data` масив, то він може бути простою одномірною структурою або масивом масивів (який, у свою чергу, може містити інші масиви).

Якщо `data` об'єкт, тоді лише загальнодоступні властивості будуть включені до результату.

`numeric_prefix`

Якщо числові індекси використовуються в базовому масиві і цей параметр вказано, він буде доданий до числового індексу для елементів тільки в базовому масиві.

Це дозволяє забезпечити допустимі імена змінних, які пізніше дані будуть декодовані PHP або іншим CGI-додатком.

`arg_separator`

[argseparator.output](ini.core.md#ini.arg-separator.output) використовується як роздільник аргументів, але може бути перевизначений шляхом вказівки цього параметра.

`encoding_type`

За замовчуванням **`PHP_QUERY_RFC1738`**

Якщо `encoding_type` дорівнює **`PHP_QUERY_RFC1738`**, тоді кодування здійснюється за [» RFC 1738](http://www.faqs.org/rfcs/rfc1738) та типу контенту `application/x-www-form-urlencoded`, що передбачає, що пробіли кодуються як символи "плюс" (`+`

Якщо `enc_type` дорівнює **`PHP_QUERY_RFC3986`**, тоді кодування здійснюється відповідно до [» RFC 3986](http://www.faqs.org/rfcs/rfc3986), а пробіли будуть закодовані у відсотках (`%20`

### Значення, що повертаються

Повертає URL-кодований рядок.

### Приклади

**Приклад #1 Простий приклад використання **httpbuildquery()****

```php
<?php
$data = array(
    'foo' => 'bar',
    'baz' => 'boom',
    'cow' => 'milk',
    'null' => null,
    'php' => 'hypertext processor'
);

echo http_build_query($data) . "\n";
echo http_build_query($data, '', '&amp;');

?>
```

Результат виконання цього прикладу:

```
foo=bar&baz=boom&cow=milk&php=hypertext+processor
foo=bar&amp;baz=boom&amp;cow=milk&amp;php=hypertext+processor
```

**Приклад #2 Приклад використання **httpbuildquery()** із числовими індексами елементів.**

```php
<?php
$data = array('foo', 'bar', 'baz', null, 'boom', 'cow' => 'milk', 'php' => 'hypertext processor');

echo http_build_query($data) . "\n";
echo http_build_query($data, 'myvar_');
?>
```

Результат виконання цього прикладу:

```
0=foo&1=bar&2=baz&4=boom&cow=milk&php=hypertext+processor
myvar_0=foo&myvar_1=bar&myvar_2=baz&myvar_4=boom&cow=milk&php=hypertext+processor
```

**Приклад #3 Приклад використання **httpbuildquery()** з багатовимірними масивами**

```php
<?php
$data = array(
    'user' => array(
        'name' => 'Bob Smith',
        'age'  => 47,
        'sex'  => 'M',
        'dob'  => '5/12/1956'
    ),
    'pastimes' => array('golf', 'opera', 'poker', 'rap'),
    'children' => array(
        'bobby' => array('age'=>12, 'sex'=>'M'),
        'sally' => array('age'=>8, 'sex'=>'F')
    ),
    'CEO'
);

echo http_build_query($data, 'flags_');
?>
```

Результат виконання даних прикладів: (символи перенесені для зручності читання)

```
user%5Bname%5D=Bob+Smith&user%5Bage%5D=47&user%5Bsex%5D=M&
user%5Bdob%5D=5%2F12%2F1956&pastimes%5B0%5D=golf&pastimes%5B1%5D=opera&
pastimes%5B2%5D=poker&pastimes%5B3%5D=rap&children%5Bbobby%5D%5Bage%5D=12&
children%5Bbobby%5D%5Bsex%5D=M&children%5Bsally%5D%5Bage%5D=8&
children%5Bsally%5D%5Bsex%5D=F&flags_0=CEO
```

> **Зауваження**
> 
> Тільки числовий індексований елемент CEO в базовому масиві отримав префікс. Інші числові індекси, знайдені в pastimes, не вимагають рядкового префікса, щоб бути допустимими іменами змінних.

**Приклад #4 Приклад використання **httpbuildquery()** з об'єктом**

```php
<?php
class parentClass {
    public    $pub      = 'publicParent';
    protected $prot     = 'protectedParent';
    private   $priv     = 'privateParent';
    public    $pub_bar  = null;
    protected $prot_bar = null;
    private   $priv_bar = null;

    public function __construct(){
        $this->pub_bar  = new childClass();
        $this->prot_bar = new childClass();
        $this->priv_bar = new childClass();
    }
}

class childClass {
    public    $pub  = 'publicChild';
    protected $prot = 'protectedChild';
    private   $priv = 'privateChild';
}

$parent = new parentClass();

echo http_build_query($parent);
?>
```

Результат виконання цього прикладу:

```
pub=publicParent&pub_bar%5Bpub%5D=publicChild
```

### Дивіться також

-   [parsestr()](function.parse-str.md) - Розбирає рядок у змінні
-   [parseurl()](function.parse-url.md) - Розбирає URL та повертає його компоненти
-   [urlencode()](function.urlencode.md) - URL-кодування рядка
-   [arraywalk()](function.array-walk.md) - Застосовує задану користувачем функцію кожного елемента масиву
