- [« Типізовані перерахування](language.enumerations.backed.md)
- [Статичні методи перерахувань »](language.enumerations.static-methods.md)

- [PHP Manual](index.md)
- [Перерахування](language.enumerations.md)
- Методи перерахувань

## Методи перерахувань

Перерахування (як чисті перерахування, так і типизовані
перерахування) можуть містити методи та можуть реалізовувати інтерфейси.
Якщо перелік реалізує інтерфейс, будь-яка перевірка типу для цього
інтерфейсу також прийматиме всі варіанти цього перерахування.

`<?phpinterface Colorful{    public function color(): string;}enum Suit implements Colorful{    case Hearts; case Diamonds; case Clubs; case Spades; // Виконує інтерфейсний контракт. public function color(): string    {        return match($this) {            Suit::Hearts, Suit::Diamonds => 'Красный',            Suit::Clubs, Suit::Spades => 'Чёрный'        }; }    // Не є частиною інтерфейсу; добре. public function shape(): string    {        return "Rectangle"; }}function paint(Colorful $c) { ... }paint(Suit::Clubs); //ПрацюєprintSuit::Diamonds->shape(); // виведе "Rectangle"?> `

У цьому прикладі у всіх чотирьох примірників `Suit` є два методи:
`color()` та `shape()`. Що стосується коду, що викликає, і перевірки типів,
вони ведуть себе так само, як і будь-який інший екземпляр об'єкта.

У типізованих переліках оголошення інтерфейсу йде після
оголошення типу.

`<?phpinterface Colorful{    public function color(): string;}enum Suit: string implements Colorful{    case Hearts = 'H'; case Diamonds = 'D'; case Clubs = 'C'; case Spades = 'S'; // Виконує інтерфейсний контракт. public function color(): string    {        return match($this) {            Suit::Hearts, Suit::Diamonds => 'Красный',            Suit::Clubs, Suit::Spades => 'Чёрный'        }; }}?> `

Усередині методу визначається змінна `$this`, яка посилається на
екземпляр варіанта.

Методи можуть бути як завгодно складними, але на практиці зазвичай
повертають статичне значення або
[match](control-structures.match.md) для `$this`, щоб надати
різні результати для різних випадків.

Зверніть увагу, що в цьому випадку було б краще визначити тип
перерахування `SuitColor` зі значеннями Red та Black та повернути його замість
цього. Однак це ускладнило цей приклад.

Вищезгадана ієрархія логічно схожа на наступну структуру класів
(хоча це не фактичний виконуваний код):

`<?phpinterface Colorful{    public function color(): string;}final class Suit implements UnitEnum, Colorful{   public const Hearts = new self(') public const Diamonds = new self('Diamonds'); public const Clubs = new self('Clubs'); public const Spades = new self('Spades'); private function __construct(public readonly string $name) {}    public function color(): string    {        return match($this) {            Suit::Hearts, Suit::Diamonds => 'Красный',            Suit::Clubs, Suit:: Spades=>>'Чорний'}; }    public function shape(): string    {        return "Прямокутник"; }    public static function cases(): array    {        // Неприпустимий метод, оскільки визначення методу cases() в перерахунках в| // Дивіться також розділ "Список значень". }}?> `

Методи можуть бути загальнодоступними, закритими або захищеними, хоча на
практиці закриті та захищені еквівалентні, оскільки спадкування не
допускається.
