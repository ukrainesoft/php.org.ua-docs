---
navigation:
  - gnupg.examples.md: « Приклади
  - ref.gnupg.md: GnuPG Функції »
  - index.md: PHP Manual
  - gnupg.examples.md: Приклади
title: Прозоре підписування тексту
---
## Прозоре підписування тексту

Це приклад створення чистого підпису надісланого тексту.

**Приклад #1 Процедурний приклад створення чистого підпису GnuPG**

```php
<?php
// инициализация GnuPG
$res = gnupg_init();
// на самом деле не нужно. Clearsign по умолчанию
gnupg_setsignmode($res, GNUPG_SIG_MODE_CLEAR);
// добавить ключ для подписания с паролем 'test'
gnupg_addsignkey($res, "8660281B6051D071D94B5B230549F9DC851566DC", "test");
// подписывание
$signed = gnupg_sign($res, "просто тест");
echo $signed;
?>
```

**Приклад #2 Об'єктно-орієнтований приклад створення чистого підпису GnuPG**

```php
<?php
// новый класс
$gnupg = new gnupg();
// на самом деле не нужно. Clearsign по умолчанию
$gnupg->setsignmode(gnupg::SIG_MODE_CLEAR);
// добавить ключ для подписания с паролем 'test'
$gnupg->addsignkey("8660281B6051D071D94B5B230549F9DC851566DC", "test");
// подписывание
$signed = $gnupg->sign("просто тест");
echo $signed;
?>
```

**Приклад #3 keylistiterator**

Цей модуль також поставляється з Iterator для ключів.

```php
<?php
// создаём новый итератор для включения в список всех открытых ключей, которые соответствуют 'example'
$iterator = new gnupg_keylistiterator("example");
foreach($iterator as $fingerprint => $userid){
    echo $fingerprint." -> ".$userid."\n";
}
?>
```
