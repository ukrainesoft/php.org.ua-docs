---
navigation:
  - function.mcrypt-create-iv.md: « mcryptcreateверб
  - function.mcrypt-enc-get-algorithms-name.md: mcryptencgetalgorithmsname »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcryptdecrypt
---
# mcryptdecrypt

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptdecrypt — Розшифровує дані із заданими параметрами

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_decrypt(    string $cipher,    string $key,    string $data,    string $mode,    string $iv = ?): string|false
```

Розшифровує `data` та повертає отримане значення.

### Список параметрів

`cipher`

Одна з констант **`MCRYPT_ciphername`** або назва алгоритму у вигляді рядка.

`key`

Ключ, із яким шифрувалися дані. Якщо довжина заданого ключа не підходить до зазначеного шифру, функція видасть попередження і поверне **`false`**

`data`

Дані, які потрібно розшифрувати з використанням шифру `cipher` та режиму `mode`. Якщо розмір даних не кратний розміру блоку, вони будуть доповнені символами '`\0`

`mode`

Одна з констант **`MCRYPT_MODE_modename`**, або один з наступних рядків: "ecb", "cbc", "cfb", "ofb", "nofb" та "stream".

`iv`

Використовується для ініціалізації в режимах CBC, CFB, OFB, а також деяких алгоритмах в режимі STREAM. Якщо переданий IV розмір не підтримується режимом зчеплення або IV не був переданий, а режим зчеплення його вимагає, функція згенерує попередження про помилку та поверне **`false`**

### Значення, що повертаються

Повертає рядок із розшифрованими даними або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mcryptencrypt()](function.mcrypt-encrypt.md) - Шифрує текст із заданими параметрами
