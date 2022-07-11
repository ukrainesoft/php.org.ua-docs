- [«ImagickDraw](class.imagickdraw.md)
- [ImagickDraw::annotation »](imagickdraw.annotation.md)

- [PHP Manual](index.md)
- [ImagickDraw](class.imagickdraw.md)
- Регулює поточну матрицю афінного перетворення

# ImagickDraw::affine

(PECL imagick 2, PECL imagick 3)

ImagickDraw::affine — Регулює поточну матрицю афінного
перетворення

### Опис

public **ImagickDraw::affine**(array `$affine`): bool

**Увага**

На цей час ця функція ще була документована; для
ознайомлення доступний лише список аргументів.

Коригує поточну матрицю афінного перетворення із зазначеною
матрицею афінного перетворення.

### Список параметрів

`affine`
Параметри афінної матриці

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::affine()****

` <?phpfunction affine($strokeColor, $fillColor, $backgroundColor) {    $draw = new \ImagickDraw(); $draw->setStrokeWidth(1); $draw->setStrokeOpacity(1); $draw->setStrokeColor($strokeColor); $draw->setFillColor($fillColor); $draw->setStrokeWidth(2); $PI = 3.141592653589794; $angle==60 * $PI / 360; //Масштабування координат креслення. $affineScale== array("sx" => 1.75, "sy" => 1.75, "rx" => 0, "ry" => 0, "tx" => 0, ty" =>> //Зсув координат креслення. $affineShear== array("sx" => 1, "sy" => 1, "rx" => sin($angle), "ry" => -sin($angle), "tx" => 0, " ty" => 0); //Поворот координат креслення. Афінна матриця зсуву дає    //неправильно масштабовані креслення. $affineRotate== array("sx" => cos($angle), "sy" => cos($angle), "rx" => sin($angle), "ry" => -sin($angle), "tx" => 0, "ty" => 0,); //Зміщення малюнку    $affineTranslate = array("sx" => 1, "sy" => 1, "rx" => 0, "ry" => 0, "tx" =>> ); //Единична афінна матриця   $affineIdentity = array("sx" => 1, sy" => 1, "rx" => 0, "ry= => 0, "tx" > 0); $examples==[$affineScale,$affineShear,$affineRotate,$affineTranslate,$affineIdentity,]; $count==0; foreach ($examples as $example) {        $draw->push(); $draw->translate(($count %2) * 250, intval($count / 2) * 250); $draw->translate(100, 100); $draw->affine($example); $draw->rectangle(-50, -50, 50, 50); $draw->pop(); $ count++; }    //Створення об'єкта зображення, в можна перетворити команди малювання. $image = new \Imagick(); $image->newImage(500, 750, $backgroundColor); $image->setImageFormat("png"); //Перетворення команд малювання в об'єкті ImagickDraw    //в зображення. $image->drawImage($draw); //Відображення зображення в браузері   header("Content-Type:image/png"); echo $image->getImageBlob();}?> `
