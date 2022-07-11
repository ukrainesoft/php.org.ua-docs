- [«get_meta_tags](function.get-meta-tags.md)
- [parse_url »](function.parse-url.md)

- [PHP Manual](index.md)
- [Функції URL](ref.url.md)
- Генерує URL-кодований рядок запиту

# http_build_query

(PHP 5, PHP 7, PHP 8)

http_build_query — Генерує URL-кодований рядок запиту

### Опис

**http_build_query**(
array\|object `$data`,
string `$numeric_prefix` = "",
?string `$arg_separator` = **`null`**,
int `$encoding_type` = **`PHP_QUERY_RFC1738`**
): string

Генерує URL-кодований рядок запиту з наданого
асоціативного (або індексованого) масиву

### Список параметрів

`data`
Може бути масив чи об'єкт, що містить властивості.

Якщо `data` масив, то він може бути простою одномірною структурою або
масивом масивів (який, у свою чергу, може містити інші
масиви).

Якщо `data` об'єкт, тоді лише загальнодоступні властивості будуть включені до
результат.

`numeric_prefix`
Якщо числові індекси використовуються в базовому масиві та цей параметр
зазначений, то він буде доданий до числового індексу для елементів тільки в
базовий масив.

Це дозволяє забезпечити допустимі імена змінних, які пізніше
дані будуть декодовані PHP або іншим програмним забезпеченням CGI.

`arg_separator`
[arg_separator.output](ini.core.md#ini.arg-separator.output)
використовується як роздільник аргументів, але може бути
перевизначено шляхом зазначення цього параметра.

`encoding_type`
За промовчанням **`PHP_QUERY_RFC1738`**.

Якщо `encoding_type` дорівнює **`PHP_QUERY_RFC1738`**, тоді кодування
здійснюється за [» RFC 1738](http://www.faqs.org/rfcs/rfc1738) та типом
контенту `application/x-www-form-urlencoded`, що має на увазі, що
пробіли кодуються як символи "плюс" (`+`).

Якщо `enc_type` дорівнює **`PHP_QUERY_RFC3986`**, тоді кодування
здійснюється відповідно до [» RFC 3986](http://www.faqs.org/rfcs/rfc3986), а пробіли будуть закодовані в
відсотках (%20).

### Значення, що повертаються

Повертає URL-кодований рядок.

### Приклади

**Приклад #1 Простий приклад використання **http_build_query()****

` <?php$data = array(   'foo' => 'bar',   'baz' => 'boom',   'cow' => 'milk',    'null'  processor');echo http_build_query($data) . "
";echo http_build_query($data, '', '&');?> `

Результат виконання цього прикладу:

foo=bar&baz=boom&cow=milk&php=hypertext+processor
foo=bar&baz=boom&cow=milk&php=hypertext+processor

**Приклад #2 Приклад використання **http_build_query()** з числовими
індексами елементів.

` <?php$data = array('foo', 'bar', 'baz', null, 'boom', 'cow' => 'milk', 'php' => 'hypertext processor');echo http_build_quer $ data) . "
";echo http_build_query($data, 'myvar_');?> `

Результат виконання цього прикладу:

0=foo&1=bar&2=baz&4=boom&cow=milk&php=hypertext+processor
myvar_0=foo&myvar_1=bar&myvar_2=baz&myvar_4=boom&cow=milk&php=hypertext+processor

**Приклад #3 Приклад використання **http_build_query()** з багатовимірними
масивами**

` <?php$data = array(    'user' => array(        'name' => 'Bob Smith',        'age'  => 47,        'sex'  => 'M',        'dob'  => '5/ 12/1956'    ),   'pastimes' => array('golf', 'opera', 'poker', 'rap'),   'children' => array( b>=' > , 'sex'=>'M'),        'sally' => array('age'=>8, 'sex'=>'F')    ),    'CEO');echo http_$$'' );?> `

Результат виконання даних прикладів: (символи перенесені для зручності
читання)

user%5Bname%5D=Bob+Smith&user%5Bage%5D=47&user%5Bsex%5D=M&
user%5Bdob%5D=5%2F12%2F1956&pastimes%5B0%5D=golf&pastimes%5B1%5D=opera&
pastimes%5B2%5D=poker&pastimes%5B3%5D=rap&children%5Bbobby%5D%5Bage%5D=12&
children%5Bbobby%5D%5Bsex%5D=M&children%5Bsally%5D%5Bage%5D=8&
children%5Bsally%5D%5Bsex%5D=F&flags_0=CEO

> **Примітка**:
>
> Тільки числовий індексований елемент "CEO" у базовому масиві
> отримав префікс. Інші числові індекси, знайдені в pastimes, не
> вимагають рядкового префікса, щоб бути допустимими іменами
> Змінні.

**Приклад #4 Приклад використання **http_build_query()** з об'єктом**

` <?phpclass parentClass {    public    $pub      ==''publicParent'; protected $prot     = 'protectedParent'; private   $priv     = 'privateParent'; public   $pub_bar = null; protected $prot_bar = = null; private   $priv_bar = null; public function __construct(){        $this->pub_bar == new childClass(); $this->prot_bar==new childClass(); $this->priv_bar==new childClass(); }}class childClass {    public   $$pub =='publicChild'; protected $prot = 'protectedChild'; private   $priv = 'privateChild';}$parent = new parentClass();echo http_build_query($parent);?> `

Результат виконання цього прикладу:

pub=publicParent&pub_bar%5Bpub%5D=publicChild

### Дивіться також

- [parse_str()](function.parse-str.md) - Розбирає рядок у
змінні
- [parse_url()](function.parse-url.md) - Розбирає URL та повертає
його компоненти
- [urlencode()](function.urlencode.md) - URL-кодування рядка
- [array_walk()](function.array-walk.md) - Застосовує задану
користувачем функцію до кожного елементу масиву
