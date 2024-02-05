---
navigation:
  - imagick.setpointsize.md: '« Imagick::setPointSize'
  - imagick.setregistry.md: 'Imagick::setRegistry »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setProgressMonitor'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::setProgressMonitor

(PECL imagick 3 >= 3.3.0)

Imagick::setProgressMonitor — Встановлює callback-функцію, яка буде викликатись під час обробки зображення Imagick

### Опис

```methodsynopsis
public Imagick::setProgressMonitor(callable $callback): bool
```

Встановлює callback-функцію, яка буде викликатись під час обробки зображення Imagick.

### Список параметрів

`callback`

Callback – функція прогресу для виклику. Вона повинна повернути true, якщо обробка зображення повинна продовжуватися, або false, якщо її потрібно скасувати. Параметр offset вказує на прогрес, а параметр span - загальний обсяг роботи, який необхідно виконати.

```methodsynopsis

       callback
      (
       mixed $offset
      , 
       mixed
        $span
      ): bool
```

**Застереження**

Значення, що передаються в callback-функцію, не узгоджені. Зокрема параметр span може збільшуватися під час обробки зображення. Через це обчислення прогресу виконання операції із зображенням у відсотках не є тривіальним.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Пример #1 Пример использования**Imagick::setProgressMonitor()\*\*\*\*

```php
<?php
        $abortReason = null;

        try {
            $imagick = new \Imagick(realpath($this->control->getImagePath()));
            $startTime = time();

            $callback = function ($offset, $span)  use ($startTime, &$abortReason) {
                if (((100 * $offset) / $span)  > 20) {
                    $abortReason = "Обработка достигла 20%";
                    return false;
                }

                $nowTime = time();

                if ($nowTime - $startTime > 5) {
                    $abortReason = "Обработка изображения заняла более 5 секунд";
                    return false;
                }
                if (($offset % 5) == 0) {
                    echo "Прогресс: $offset / $span <br/>";
                }
                return true;
            };

            $imagick->setProgressMonitor($callback);

            $imagick->waveImage(2, 15);

            echo "Длина данных: ".strlen($imagick->getImageBlob());
        }
        catch(\ImagickException $e) {
            if ($abortReason != null) {
                echo "Обработка изображения была прервана: ".$abortReason."<br/>";
            }
            else {
                echo "Поймано исключение ImagickException: ".$e->getMessage()." Тип исключения - ".get_class($e);
            }
        }

?>
```
