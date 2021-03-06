- [« Imagick::stripImage](imagick.stripimage.md)
- [Imagick::swirlImage »](imagick.swirlimage.md)

- [PHP Manual](index.md)
- [Imagick](class.imagick.md)
- Опис

# Imagick::subImageMatch

(PECL imagick 3 \>= 3.3.0)

Imagick::subImageMatch — Опис

### Опис

public **Imagick::subImageMatch**([Imagick](class.imagick.md)
`$Imagick`, array `&$offset` = ?, float `&$similarity` = ?):
[Imagick](class.imagick.md)

Виконує пошук фрагмента зображення у поточному зображенні та повертає
другорядне зображення, в якому точний збіг є
повністю білим, а якщо жоден з пікселів не збігається - чорним,
в іншому випадку - деяким проміжним рівнем сірого. Ви також
Ви можете передати необов'язкові параметри bestMatch і similarity. Після
виклику функції similarity буде встановлено на "score" подібності між
другорядним зображенням та відповідною позицією на великому
зображенні, bestMatch міститиме асоціативний масив з елементами
x, y, width, height, які описують збігається область.

### Список параметрів

`Imagick`

`offset`

`similarity`
Нове зображення, що відображає ступінь подібності кожного пікселя.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **Imagick::subImageMatch()****

`<?phpfunction subImageMatch($imagePath) {   $imagick = new \Imagick(realpath($imagePath)); $imagick2==clone$imagick; $imagick2->cropimage(40, 40, 250, 110); $imagick2->vignetteimage(0, 1, 3, 3); $ similarity = = null; $bestMatch==null; $comparison==$imagick->subImageMatch($imagick2, $bestMatch, $similarity); $comparison->setImageFormat('png'); header("Content-Type: image/png"); echo $imagick->getImageBlob();}?> `
