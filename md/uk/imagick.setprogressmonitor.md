- [« Imagick::setPointSize](imagick.setpointsize.md)
- [Imagick::setRegistry »](imagick.setregistry.md)

- [PHP Manual](index.md)
- [Imagick](class.imagick.md)
- Встановлює callback-функцію, яка буде викликатись під час
обробки зображення Imagick

# Imagick::setProgressMonitor

(PECL imagick 3 \>= 3.3.0)

Imagick::setProgressMonitor — Встановлює callback-функцію, яка
буде викликатися під час обробки зображення Imagick

### Опис

public
**Imagick::setProgressMonitor**([callable](language.types.callable.md)
`$callback`): bool

Встановлює callback-функцію, яка буде викликатись під час
обробки зображення Imagick.

### Список параметрів

`callback`
Callback – функція прогресу для виклику. Вона повинна повернути true, якщо
обробка зображення повинна продовжуватися, або false, якщо її потрібно
скасувати. Параметр offset вказує прогрес, а параметр span – загальний
обсяг роботи, який потрібно виконати.

callback (
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$offset`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$span` ): bool

**Застереження**
Значення, що передаються в callback-функцію, не узгоджені. Зокрема,
параметр span може збільшуватись під час обробки зображення. Через
цього обчислення прогресу виконання операції із зображенням
відсотках не є тривіальним.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**.

### Приклади

**Приклад #1 Приклад використання **Imagick::setProgressMonitor()****

` <?php        $abortReason = null; try {             $imagick = new \Imagick(realpath($this->control->getImagePath())); $startTime = time(); $callback = function ($offset, $span)  use ($startTime, &$abortReason) {                if (((100 * $offset) / $span)  > 20) {                    $abortReason = "Обработка достигла 20%"; return false; }                  $nowTime==time(); if ($nowTime - $startTime > 5) {                     $abortReason = "Обробка зображення зайняла більше| return false; }                 if (($offset % 5) == 0) {                           ¦¦¦¦ }                 return true; }; $imagick->setProgressMonitor($callback); $imagick->waveImage(2, 15); echo "Довжина даних: ".strlen($imagick->getImageBlob()); }        catch(\ImagickException $e) {            if ($abortReason != null) {                echo "Обработка изображения была прервана: ".$abortReason."<br/>"; }             else {                 echo "Впіймано виняток ImagickException: ".$e->getMessage( і| і| }        }}>
