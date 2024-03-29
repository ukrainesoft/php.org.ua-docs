---
navigation:
  - function.sys-get-temp-dir.md: « sys\_get\_temp\_dir
  - function.zend-thread-id.md: zend\_thread\_id »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: version\_compare
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# version\_compare

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

version\_compare — Порівнює два «стандартизовані» рядки з номером версії PHP

### Опис

```methodsynopsis
version_compare(string $version1, string $version2, ?string $operator = null): int|bool
```

**version\_compare()** порівнює два "PHP-стандартизовані" рядки з номерами версій.

Функція спочатку замінює підкреслення `_`, дефис`-`и знак плюса`+` на точку у рядках версій, а також додає точки до та після кожного символу, що не є числом. Наприклад, '4.3.2RC1' перетворюється на '4.3.2.RC.1'. Після цього порівнює частини рядків зліва направо. Якщо частина рядка містить спеціальні символи версій, вони обробляються так: `будь-який рядок, не знайдений у цьому списку` < `dev` < `alpha` `a` < `beta` `b` < `RC` `rc` < `#` < `pl` `p`. . Таким чином, можна порівнювати не тільки версії різних рівнів, на кшталт '4.1' і '4.1.2', а й специфічні версії, що включають статус розробки.

### Список параметрів

`version1`

Номер першої версії.

`version2`

Номер другої версії.

`operator`

Необов'язковий параметр `operator`. Можливі значення: `<` `lt` `<=` `le` `>` `gt` `>=` `ge` `==` `=` `eq` `!=` `<>` `ne`

Аргумент чутливий до регістру, тому значення мають бути в нижньому регістрі.

### Значення, що повертаються

По умолчанию функция**version\_compare()** повертає `-1`якщо перша версія менша за другу; коли вони рівні; , якщо друга менша за першу.

При использовании аргумента`operator` функція поверне **`true`**, якщо вираз відповідно до оператора вірний, і **`false`** в іншому випадку.

### Приклади

У прикладі нижче використовується константа \*\*`PHP_VERSION`\*\*Вона містить номер версії PHP, який виконує код.

**Приклад #1 Приклад використання** version\_compare()\*\*\*\*

```php
<?php
if (version_compare(PHP_VERSION, '7.0.0') >= 0) {
    echo 'Я использую PHP версии не ниже 7.0.0, моя версия: ' . PHP_VERSION . "\n";
}

if (version_compare(PHP_VERSION, '5.3.0') >= 0) {
    echo 'Я использую PHP версии не ниже 5.3.0, моя версия: ' . PHP_VERSION . "\n";
}

if (version_compare(PHP_VERSION, '5.0.0', '>=')) {
    echo 'Я использую PHP 5.0.0 или выше, моя версия: ' . PHP_VERSION . "\n";
}

if (version_compare(PHP_VERSION, '5.0.0', '<')) {
    echo 'Я до сих пор использую PHP 4, моя версия: ' . PHP_VERSION . "\n";
}
?>
```

### Примітки

> **Зауваження** :
> 
> Константа\*\*`PHP_VERSION`\*\* зберігає номер поточної версії PHP.

> **Зауваження** :
> 
> Зауважте, що дорелізні версії, такі як 5.3.0-dev, вважаються меншими за фінальні (види 5.3.0).

> **Зауваження** :
> 
> Спеціальні слова начебто `alpha`и`beta` чутливі до регістру. Рядки версій, які не дотримуються PHP-стандарту, потрібно наводити до нижнього регістру функцією [strtolower()](function.strtolower.md) до виклику **version\_compare()**

### Дивіться також

-   [phpversion()](function.phpversion.md) \- Отримує поточну версію PHP
-   [php\_uname()](function.php-uname.md) \- Повертає інформацію про операційну систему, на якій запущено PHP
-   [function\_exists()](function.function-exists.md) \- Повертає true, якщо вказана функція визначена
