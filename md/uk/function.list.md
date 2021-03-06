- [«ksort](function.ksort.md)
- [Natcasesort »](function.Natcasesort.md)

- [PHP Manual](index.md)
- [Функції для роботи з масивами](ref.array.md)
- Надає змінним зі списку значення подібно до масиву

# list

(PHP 4, PHP 5, PHP 7, PHP 8)

list — Надає змінним зі списку значення подібно до масиву

### Опис

**list**([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$var`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`...$vars` = ?): array

Подібно до [array()](function.array.md), це не функція, а мовна
конструкція. **list()** використовується для того, щоб присвоїти списку
змінних значення одну операцію. Рядки не можна розпакувати, а
висловлювання **list()** не можуть бути повністю порожніми.

> **Примітка**:
>
> До PHP 7.1.0, **list()** працювала лише з індексованими масивами
> і приймала числові індекси, починаючи з 0.

### Список параметрів

`var`
Змінна.



`vars`
Додаткові змінні.

### Значення, що повертаються

Повертає привласнений масив.

### Список змін

| Версія | Опис                                                                                                                      |
|--------|---------------------------------------------------------------------------------------------------------------------------|
| 7.3.0  | Додано підтримку присвоєння за посиланнями при деструктуруванні масиву.                                                   |
| 7.1.0  | Тепер можна задавати ключі **list()**. Це дозволяє розіменовувати асоціативні масиви та масиви з індексами не по порядку. |

### Приклади

**Приклад #1 Приклади використання **list()****

` <?php$info = array('кава', 'коричневий', 'кофеїн');// Скласти список всіх зміннихlist($drink, $color, $power) = $info;echo "$drink - $or, а $power робить його особливим.
";// Скласти список тільки деяких з ніхlist($drink, , $power) = $info;echo "У $drink є $power.
";// Або пропустити все, крім третійlist( , , $power) = $info;echo "Мені потрібний $power!
";// list() не працює з рядкамиlist($bar) = "abcde";var_dump($bar); // NULL?> `

**Приклад #2 Приклад використання **list()****

` <?php$result = $pdo->query("SELECT id, name FROM employees");while (list($id, $name) = $result->fetch(PDO::FETCH_NUM)) {    ech : $id, name: $name
";}?> `

**Приклад #3 Використання **list()** з індексами масивів**

` <?phplist($a, list($b, $c)) = array(1, array(2, 3));var_dump($a, $b, $c);?> `

int(1)
int(2)
int(3)

**Приклад #4 **list()** та порядок вказівки індексів**

Порядок, у якому індекси масиву використовуватимуться функцією
**list()**, не має значення.

` <?php$foo = array(2 => 'a', 'foo' => 'b', 0 => 'c');$foo[1] = 'd';list($x, $y , $z) = $foo;var_dump($foo, $x, $y, $z); `

Здійснює такий висновок (зверніть увагу, на порядок, у якому
елементи були перераховані в синтаксисі **list()** і порядок виведення):

array(4) {
[2]=>
string(1) "a"
["foo"]=>
string(1) "b"
[0]=>
string(1) "c"
[1]=>
string(1) "d"
}
string(1) "c"
string(1) "d"
string(1) "a"

**Приклад #5 **list()** з ключами**

Починаючи з PHP 7.1.0, для **list()** можна задавати конкретні ключі,
які можуть бути довільними висловлюваннями. Допустимо змішувати
рядкові та числові ключі. Однак елементи з ключами та без ключів не
можуть бути використані одночасно.

` <?php$data == [    ["id" => 1, "name" => 'Tom'],    ["id" => 2, "name" => 'Fred'],];foreach ($da as ["id" => $id, "name" => $name]) {    echo "id: $id, name: $name
";}echo PHP_EOL;list(1 => $second, 3 => $fourth) = [1, 2, 3, 4];echo "$second, $fourth
";

Результат виконання цього прикладу:

id: 1, name: Tom
id: 2, name: Fred

2, 4

### Дивіться також

- [each()](function.each.md) - Повертає поточну пару ключ/значення
з масиву та зміщує його покажчик
- [array()](function.array.md) - Створює масив
- [extract()](function.extract.md) - Імпортує змінні з
масиву до поточної таблиці символів
