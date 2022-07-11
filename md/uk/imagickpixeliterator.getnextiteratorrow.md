- [« ImagickPixelIterator::getIteratorRow](imagickpixeliterator.getiteratorrow.md)
- [ImagickPixelIterator::getPreviousIteratorRow »](imagickpixeliterator.getpreviousiteratorrow.md)

- [PHP Manual](index.md)
- [ImagickPixelIterator](class.imagickpixeliterator.md)
- Повертає наступний ряд ітератора пікселів

# ImagickPixelIterator::getNextIteratorRow

(PECL imagick 2, PECL imagick 3)

ImagickPixelIterator::getNextIteratorRow — Повертає наступний ряд
ітератора пікселів

### Опис

public **ImagickPixelIterator::getNextIteratorRow**(): array

**Увага**

На цей час ця функція ще була документована; для
ознайомлення доступний лише список аргументів.

Повертає наступний ряд як масиву пікселів з ітератора пікселів.

### Значення, що повертаються

Повертає наступний ряд у вигляді масиву об'єктів ImagickPixel, у випадку
Виникнення помилки видасть виключення ImagickPixelIteratorException.

### Приклади

**Приклад #1 Приклад використання
**ImagickPixelIterator::getNextIteratorRow()****

`<?phpfunction getNextIteratorRow($imagePath) {   $imagick = new \Imagick(realpath($imagePath)); $imageIterator==$imagick->getPixelIterator(); $count==0; while ($pixels = $imageIterator->getNextIteratorRow()) {        if (($count % 3) == 0) {            /* Походим по пикселям в строке (столбцы) */            foreach ($pixels as $column => $pixel ) {                /** @var $pixel \ImagickPixel */                if ($column % 2) {                    /* Красим каждый второй пиксель черным*/                    $pixel->setColor("rgba(0, 0, 0, 0)"); }              }             /* Синхронізуємо ітератор. Це необхідно для робити на кожній ітерації */            $imageIterator->syncIterator(); }        $count += 1; }   header("Content-Type:image/jpg"); echo $imagick;}?> `
