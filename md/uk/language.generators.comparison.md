---
navigation:
  - language.generators.syntax.md: « Синтаксис генераторів
  - language.attributes.md: Атрибути »
  - index.md: PHP Manual
  - language.generators.md: Генератори
title: 'Порівняння генераторів з об''єктами класу [Iterator](class.iterator.md)'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Порівняння генераторів з об'єктами класу [Iterator](class.iterator.md)

Головна перевага генераторів – це їхня простота. Набагато менше шаблонного коду треба написати порівняно з реалізацією об'єкта класу [Iterator](class.iterator.md), і цей код набагато простіший і зрозуміліший. Наприклад, ця функція і клас роблять те саме.

```php
<?php
function getLinesFromFile($fileName) {
    if (!$fileHandle = fopen($fileName, 'r')) {
        return;
    }

    while (false !== $line = fgets($fileHandle)) {
        yield $line;
    }

    fclose($fileHandle);
}

// Против...

class LineIterator implements Iterator {
    protected $fileHandle;

    protected $line;
    protected $i;

    public function __construct($fileName) {
        if (!$this->fileHandle = fopen($fileName, 'r')) {
            throw new RuntimeException('Невозможно открыть файл "' . $fileName . '"');
        }
    }

    public function rewind() {
        fseek($this->fileHandle, 0);
        $this->line = fgets($this->fileHandle);
        $this->i = 0;
    }

    public function valid() {
        return false !== $this->line;
    }

    public function current() {
        return $this->line;
    }

    public function key() {
        return $this->i;
    }

    public function next() {
        if (false !== $this->line) {
            $this->line = fgets($this->fileHandle);
            $this->i++;
        }
    }

    public function __destruct() {
        fclose($this->fileHandle);
    }
}
?>
```

Однак за цю простоту доводиться платити: генератори можуть бути тільки односпрямованими ітераторами. Їх не можна перемотати після старту ітерації. Це також означає, що той самий генератор не можна використовувати кілька разів: генератор необхідно перестворювати щоразу, знову викликавши функцію генератора.

### Дивіться також

-   [Ітератори об'єктів](language.oop5.iterations.md)
