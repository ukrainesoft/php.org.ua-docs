- [«Вступ](oop5.intro.md)
- [Властивості »](language.oop5.properties.md)

- [PHP Manual](index.md)
- [Класи та об'єкти](language.oop5.md)
- Основи

## Основи

### class

Кожне визначення класу починається з ключового слова `class`, потім
слідує ім'я класу, і далі пара фігурних дужок, які укладають у
собі визначення властивостей та методів цього класу.

Ім'ям класу може бути будь-яке слово, за умови, що воно не входить до
Список [зарезервованих слів](reserved.md) PHP, починається з літери
або символу підкреслення і за яким слідує будь-яка кількість літер,
цифр або символів підкреслення. Якщо задати ці правила у вигляді
регулярного виразу, то вийде таке вираз:
`^[a-zA-Z_\x80-\xff][a-zA-Z0-9_\x80-\xff]*$`.

Клас може містити власні [константи](language.oop5.constants.md),
[змінні](language.oop5.properties.md) (називаються властивостями) та
функції (звані методами).

**Приклад #1 Просте визначення класу**

`<?phpclass SimpleClass{    // оголошення властивості    public $var = 'значення за замовчуванням'; // оголошення методу    public function displayVar() {        echo $this->var; }}?> `

Псевдозмінна `$this` доступна в тому випадку, якщо метод був викликаний
контекст об'єкта. `$this` - значення об'єкта, що викликає.

**Увага**

Виклик нестатичного методу статично викликає помилку
[Error](class.error.md). До PHP 8.0.0 це призвело б до повідомлення про
старіння, і `$this` не була б визначена.

**Приклад #2 Деякі приклади псевдо-змінної `$this`**

` <?phpclass A{    function foo()    {        if (isset($this)) {            echo '$this определена (';            echo get_class($this);            echo ")
";        } else {            echo "\$this не визначена.
";|||:|||||||||||||||||||||||||||(| ();$b->bar();B::bar();?> `

Результат виконання цього прикладу в PHP 7:

$this визначена (A)

Deprecated: Non-static method A::foo() не може бути названий статичне в %s on line 27
$this не визначено.

Deprecated: Non-static method A::foo() не може статися в %s on line 20
$this не визначено.

Deprecated: Non-static method B::bar() не може статися в %s on line 32

Deprecated: Non-static method A::foo() не може статися в %s on line 20
$this не визначено.

Результат виконання цього прикладу в PHP 8:

$this визначена (A)

Fatal error: Uncaught Error: Нестатичний метод A::foo() cannot be called statically in %s :27
Stack trace:
#0 {main}
thrown in %s on line 27

### new

Для створення екземпляра класу використовується директива `new`. новий
об'єкт завжди буде створений, за винятком випадків, коли він містить
[конструктор](language.oop5.decon.md), у якому визначено виклик
[виключення](language.exceptions.md) у разі виникнення помилки.
Рекомендується визначати класи до створення їх екземплярів (у деяких
це обов'язково).

Якщо з директивою `new` використовується рядок (string), що містить ім'я
класу, буде створено новий екземпляр цього класу. Якщо ім'я знаходиться
у просторі імен, воно має бути задано повністю.

> **Примітка**:
>
> У разі відсутності аргументів у конструктор класу, круглі дужки
> після назви класу можна опустити.

**Приклад #3 Створення екземпляра класу**

` <?php$instance = new SimpleClass();// Це та можна зробити з допомогою змінною:$className = 'SimpleClass';$instance = new $className(); // new SimpleClass()?> `

Починаючи з PHP 8.0.0, підтримується використання оператора `new` з
довільними висловлюваннями. Це дозволяє створювати складніші
екземпляри, якщо вираз представлений у вигляді рядка (string).
Вирази мають бути укладені у круглі дужки.

**Приклад #4 Створення екземпляра з використанням довільного
вирази**

У цьому прикладі ми показуємо кілька варіантів допустимих
довільних виразів, що становлять ім'я класу. Приклад виклику
функції, конкатенації рядків та константи **`::class`**.

` <?phpclass ClassA extends \stdClass {}class ClassB extends \stdClass {}class ClassC extends ClassB {}class ClassD extends ClassA {}function getSomeClass(): );var_dump(new ('Class' . 'B'));var_dump(new ('Class' . 'C'));var_dump(new (ClassD::class));?> `

Результат виконання цього прикладу в PHP 8:

object(ClassA)#1 (0) {
}
object(ClassB)#1 (0) {
}
object(ClassC)#1 (0) {
}
object(ClassD)#1 (0) {
}

У контексті класу можна створити новий об'єкт через `new self` та
`New parent`.

Коли відбувається присвоєння існуючого екземпляра класу нової
змінною, то ця змінна буде вказувати на цей самий екземпляр
класу. Те саме відбувається і при передачі екземпляра класу в
функцію. Копію вже створеного об'єкта можна створити через неї
[клонування](language.oop5.cloning.md).

**Приклад #5 Привласнення об'єкта**

` <?php$instance = new SimpleClass();$assigned  =  $instance;$reference =& $instance;$instance->var = '$assigned буде мете це значення';$in // $instance і $reference стають nullvar_dump($instance);var_dump($reference);var_dump($assigned);?> `

Результат виконання цього прикладу:

NULL
NULL
object(SimpleClass)#1 (1) {
["var"]=>
string(30) "$assigned буде мати це значення"
}

Створювати екземпляри об'єкта можна двома способами:

**Приклад #6 Створення нових об'єктів**

` <?phpclass Test{    static public function getNew()    {        return new static; }}class Child extends Test{}$obj1 = new Test();$obj2 = new $obj1;var_dump($obj1 !== $obj2);$obj3 = Test::getNew(); );$obj4 = Child::getNew();var_dump($obj4 instanceof Child);?> `

Результат виконання цього прикладу:

bool(true)
bool(true)
bool(true)

Звернутися до властивості або методу щойно створеного об'єкта можна з
допомогою одного виразу:

**Приклад #7 Доступ до властивостей/методів щойно створеного об'єкта**

` <?phpecho (new DateTime())->format('Y');?> `

Результатом виконання цього прикладу буде щось подібне:

2016

> **Примітка**: До PHP 7.1 аргументи не мали значення, якщо не
> визначено функцію конструктора.

### Властивості та методи

Властивості та методи класу живуть у розділених "просторах імен", так
що можна мати якість і спосіб з тим самим ім'ям. Посилання як
на властивості, і на методи мають однакову нотацію, і виходить, що
отримаєте ви доступ до властивості або ж викличете метод - визначається
контекст використання.

**Приклад #8 Доступ до якості vs. виклик методу**

` <?phpclass Foo{    public $bar = 'властивість'; public function bar() {        return 'метод'; }}$obj = new Foo();echo $obj->bar, PHP_EOL, $obj->bar(), PHP_EOL; `

Результат виконання цього прикладу:

властивість
метод

Це означає, що викликати [анонімну функцію](functions.anonymous.md),
привласнену змінною, безпосередньо не вийде. Натомість властивість
має бути призначено, наприклад, змінною. Можна викликати таке
властивість безпосередньо, уклавши їх у дужки.

**Приклад #9 Виклик анонімної функції, що міститься у властивості**

`<?phpclass Foo{    public $bar; public| }; }}$obj = new Foo();echo ($obj->bar)(), PHP_EOL; `

Результат виконання цього прикладу:

42

### extends

Клас може успадковувати константи, методи та властивості іншого класу
використовуючи ключове слово `extends` у його оголошенні. Неможливо
успадковувати кілька класів, один клас може успадковувати лише один
базовий клас.

Наслідувані константи, методи та властивості можуть бути перевизначені (за
винятком випадків, коли метод або константа класу оголошені як
[final](language.oop5.final.md)) шляхом оголошення їх з тими ж
іменами, як і у батьківському класі. Існує можливість доступу до
перевизначеним методам або статичним властивостям шляхом звернення до них
через [parent::](language.oop5.paamayim-nekudotayim.md)

> **Примітка**: Починаючи з PHP 8.1.0, константи можна оголошувати
> Остаточними (final).

**Приклад #10 Просте успадкування класів**

`<?phpclass ExtendClass extends SimpleClass{    // Перевизначення методу батька    function displayVar()   {        echo "Расширення"
";         parent::displayVar();    }}$extended = new ExtendClass();$extended->displayVar();?> `

Результат виконання цього прикладу:

Розширений клас
значення за замовчуванням

#### Правила сумісності сигнатури

При перевизначенні методу його сигнатура має бути сумісна з
батьківським способом. В іншому випадку видається фатальна помилка або,
до PHP 8.0.0, генерується помилка рівня **`E_WARNING`**. Сигнатура
є сумісною, якщо вона відповідає правилам
[контраваріантності](language.oop5.variance.md), робить обов'язковим
параметр необов'язковий і якщо будь-які нові параметри є
необов'язковими. Це відомо як принцип підстановки Барбари Лисків або
скорочено LSP. Правила сумісності не поширюються на
[конструктор](language.oop5.decon.md#language.oop5.decon.constructor)
і сигнатуру `private` методів, вони не будуть видавати фатальну помилку в
у разі невідповідності сигнатури.

**Приклад #11 Сумісність дочірніх методів**

`<?phpclass Base{    public function foo(int $a) {       echo "Допустимо
";    }}class Extend1 extends Base{    function foo(int $a = 5)    {        parent::foo($a);    }}class Extend2 extends Base{    function foo(int $a, $b = 5)    {        parent: :foo($a);    }}$extended1 = new Extend1();$extended1->foo();$extended2 = new Extend2();$extended2->foo(1);

Результат виконання цього прикладу:

Допустимо
Допустимо

Наступні приклади демонструють, що дочірній метод видаляє
параметр або робить необов'язковий параметр обов'язковим, несумісний з
батьківським способом.

**Приклад #12 Фатальна помилка, коли дочірній метод видаляє параметр**

`<?phpclass Base{    public function foo(int $a = 5) {       echo "Допустимо
";    }}class Extend extends Base{   function foo()   {         parent::foo(1);    }} `

Результат виконання цього прикладу в PHP 8 аналогічний:

Fatal error: Declaration of Extend::foo() must be compatible with Base::foo(int $a = 5) у /in/evtlq on line 13

**Приклад #13 Фатальна помилка, коли дочірній метод робить
необов'язковий параметр є обов'язковим.**

`<?phpclass Base{    public function foo(int $a = 5) {       echo "Допустимо
";    }}class Extend extends Base{   function foo(int $a)    {        parent::foo($a);    }} `

Результат виконання цього прикладу в PHP 8 аналогічний:

Поміркований error: Declaration of Extend::foo(int $a) має бути надійним з Base::foo(int $a = 5) in /in/qJXVC on line 13

**Увага**

Перейменування параметра методу в дочірньому класі не є
несумісністю сигнатури. Однак це не рекомендується, оскільки
приведе до [Error](class.error.md) під час виконання, якщо
використовуються [іменовані аргументи](functions.arguments.md#functions.named-arguments).

**Приклад #14 Помилка при використанні іменованих аргументів та
параметрів, перейменованих у дочірньому класі**

` <?phpclass A { {   public function test($foo, $bar) {}}class B extends A {    public function test($a, $b) {}}$obj =      ::test()$obj->test(foo: "foo", bar: "bar"); // ПОМИЛКА! `

Результатом виконання цього прикладу буде щось подібне:

Fatal error: Uncaught Error: Unknown named parameter $foo in /in/XaaeN:14
Stack trace:
#0 {main}
thrown in /in/XaaeN on line 14

### ::class

Ключове слово `class` використовується для дозволу імені класу. Щоб
отримати повне ім'я класу `ClassName`, використовуйте `ClassName::class`.
Зазвичай це досить корисно під час роботи з класами, які використовують
[простір імен](language.namespaces.md).

**Приклад #15 Дозвіл імені класу**

` <?phpnamespace NS {   classClassClassName {    }   echo ClassName::class;}?> `

Результат виконання цього прикладу:

NS\ClassName

> **Примітка**:
>
> Дозвіл назв класу з використанням `::class` відбувається на етапі
> компіляції. Це означає, що на момент створення рядка з ім'ям
> класу автозавантаження класу не відбувається. Як наслідок, імена класів
> розкриваються, навіть якщо клас немає. Помилка у цьому випадку не
> Видається.
>
> **Приклад #16 Відсутня роздільна здатність імені класу**
>
> ` <?phpprint Does\Not\Exist::class;?> `
>
> Результат виконання цього прикладу:
>
> Does\Not\Exist

Починаючи з PHP 8.0.0, константа `::class` також може використовуватись для
об'єктів. Цей дозвіл відбувається під час виконання, а не під час
компіляції. Те саме, що і при виклику
[get_class()](function.get-class.md) для об'єкта.

**Приклад #17 Дозвіл імені об'єкта**

` <?phpnamespace NS {   classClassClassName {    }}$c = new ClassName();print $c::class;?> `

Результат виконання цього прикладу:

NS\ClassName

### Методи та властивості Nullsafe

Починаючи з PHP 8.0.0, до властивостей та методів можна також звертатися з
допомогою оператора "nullsafe": `?->`. Оператор nullsafe працює так само,
як доступ до властивості або методу, як зазначено вище, за винятком того,
що якщо розйменування об'єкта видає **`null`**, то буде повернено
**`null`**, а не викинуто виняток. Якщо розіменування є
частиною ланцюжка, решта ланцюжка пропускається.

Аналогічно висновку кожного звернення до
[is_null()](function.is-null.md), але компактніший.

**Приклад #18 Оператор Nullsafe**

` <?php// Починаючи з PHP 8.0.0, цей рядок: $result = = $ repository? -> getUser (5)? -> name; // Еквівалентна наступному блоку коду: result = null;} else {    $user = $repository->getUser(5); if (is_null($user)) {         $result = null; } else {        $result = $user->name; }}?> `

> **Примітка**:
>
> Оператор nullsafe найкраще використовувати, коли null вважається
> допустимим і очікуваним значенням для властивості, що повертається, або
> методу. Для індикації помилки краще викидати виняток.
