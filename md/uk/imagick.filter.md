- [« Imagick::extentImage](imagick.extentimage.md)
- [Imagick::flattenImages »](imagick.flattenimages.md)

- [PHP Manual](index.md)
- [Imagick](class.imagick.md)
- Опис

# Imagick::filter

(PECL imagick 3 \>= 3.3.0)

Imagick::filter — Опис

**Увага**

Функція оголошена *УСТАРШЕНОЮ* в Imagick 3.4.4. Покладатись на цю
функцію не рекомендується.

### Опис

public **Imagick::filter**([ImagickKernel](class.imagickkernel.md)
`$ImagickKernel`, int `$channel` = Imagick::CHANNEL_UNDEFINED): bool

Застосовує ядро згортки до зображення.

### Список параметрів

`ImagickKernel`
Примірник ImagickKernel, який представляє або одне ядро, або пов'язану
серію ядер.

`channel`
Надайте будь-яку коректну для вашого режиму каналу константу. Для
застосування до більш ніж одного каналу, комбінуйте [константи каналов](imagick.constants.md#imagick.constants.channel) за допомогою
побітових операторів. За промовчанням одно **`Imagick::CHANNEL_DEFAULT`**.
Зверніться до списку [констант каналов](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**.

### Приклади

**Приклад #1 Приклад використання **Imagick::filter()****

` <?phpfunction filter($imagePath) {   $imagick = new \Imagick(realpath($imagePath)); $matrix = [        [-1, 0, -1],        [0,  5,  0],        [-1, 0, ] $kernel= \ImagickKernel::fromMatrix($matrix); $strength==0.5; $kernel->scale($strength, \Imagick::NORMALIZE_KERNEL_VALUE); $kernel->addUnityKernel(1 - $strength); $imagick->filter($kernel); header("Content-Type: image/jpg"); echo $imagick->getImageBlob();}?> `
