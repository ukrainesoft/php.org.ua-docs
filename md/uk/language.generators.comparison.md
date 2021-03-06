- [« Синтаксис генераторів](language.generators.syntax.md)
- [Атрибути »](language.attributes.md)

- [PHP Manual](index.md)
- [Генератори](language.generators.md)
- Порівняння генераторів з об'єктами класу Iterator

## Порівняння генераторів з об'єктами класу [Iterator](class.iterator.md)

Головна перевага генераторів – це їхня простота. Значно менше
шаблонного коду треба написати, порівняно з реалізацією об'єкта класу
[Iterator](class.iterator.md), і цей код набагато простіший і
зрозумілий. Наприклад, ця функція і клас роблять те саме.

` <?phpfunction getLinesFromFile($fileName) {    if (!$fileHandle = fopen($fileName, 'r')) {        return; }   while (false !== $line = fgets($fileHandle)) {        yield $line; }   fclose($fileHandle);}//Проти...class LineIterator implements Iterator {   protected $fileHandle; protected$line; protected$i; Public function __construct($fileName) {                         }    }    public function rewind() {        fseek($this->fileHandle, 0); $this->line==fgets($this->fileHandle); $this->i = 0; }    public function valid() {        return false !== $this->line; }    public function current() {        return $this->line; }    public function key() {        return $this->i; }    public function next() {        if (false !== $this->line) {             $this->line =| $this->i++; }    }    public function __destruct() {        fclose($this->fileHandle); }}?> `

Проте за цю простоту доводиться платити: генератори можуть
бути лише односпрямованими ітераторами. Їх не можна перемотати назад
після старту ітерації. Це також означає, що той самий генератор
не можна використовувати кілька разів: генератор необхідно перестворювати
щоразу, знову викликавши функцію генератора.

### Дивіться також

- [Ітератори об'єктів](language.oop5.iterations.md)
