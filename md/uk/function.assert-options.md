---
navigation:
  - ref.info.md: « Опції PHP/інформаційні функції
  - function.assert.md: assert »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: assert\_options
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# assert\_options

(PHP 4, PHP 5, PHP 7, PHP 8)

assert\_options — Встановлення та отримання параметрів механізму перевірки тверджень

**Увага**

Функція оголошена *застарілої* починаючи з PHP 8.3.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
assert_options(int $option, mixed $value = ?): mixed
```

Задание значений настроек механизма проверки утверждений[assert()](function.assert.md)или получение их текущих значений.

> **Зауваження**: Использование**assert\_options()** не рекомендується на користь встановлення та отримання php.ini директив [zend.assertions](ini.core.md#ini.zend.assertions) і [assert.exception](info.configuration.md#ini.assert.exception) за допомогою [ini\_set()](function.ini-set.md) і [ini\_get()](function.ini-get.md)соответственно.

### Список параметрів

`option`

**Налаштування механізму перевірки тверджень**

| Настройка | INI-параметр | Значение по умолчанию | Опис |
| --- | --- | --- | --- |
| ASSERT\_ACTIVE | assert.active |  | включення механізму перевірки тверджень |
| ASSERT\_EXCEPTION | assert.exception |  | викидає [AssertionError](class.assertionerror.md) для кожного невдалого твердження |
| ASSERT\_WARNING | assert.warning |  | виведення попередження PHP для кожної невдалої перевірки |
| ASSERT\_BAIL | assert.bail |  | завершити виконання у разі невдалої перевірки |
| ASSERT\_QUIET\_EVAL | assert.quiet\_eval |  | відключити error\_reporting під час перевірки затвердження. Видалено з PHP 8.0.0. |
| ASSERT\_CALLBACK | assert.callback | **`null`**) . | Callback-функція, яку необхідно викликати для затвердження, що провалило перевірку |

`value`

Необов'язковий аргумент, нове значення налаштування.

У callback-функции, установленной с помощью\*\*`ASSERT_CALLBACK`\*\*или[assert.callback](info.configuration.md#ini.assert.callback), має бути наступна сигнатура:

```methodsynopsis
assert_callback(    string $file,    int $line,    ?string $assertion,    string $description = ?): void
```

`file`

Файл, у якому було викликано [assert()](function.assert.md)

`line`

Рядок, в якому був викликаний [assert()](function.assert.md)

`assertion`

До PHP 8.0.0 твердження, яке передавалося у функцію [assert()](function.assert.md), але якщо затвердження задано у вигляді рядка. (Якщо затвердження є логічною умовою, цей параметр буде порожнім рядком). Починаючи з PHP 8.0.0, цей параметр завжди **`null`**

`description`

Опис, яке було передано до [assert()](function.assert.md)

Передача порожнього рядка в `value` скидає assert callback.

### Значення, що повертаються

Повертає початкове значення налаштування.

### Помилки

Функція викидає [ValueError](class.valueerror.md), якщо параметр `option` не є допустимою опцією.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Функция**assert\_option()** оголошено застарілою. |
| 8.0.0 | Якщо параметр `option` не є допустимою опцією, тепер викидається помилка [ValueError](class.valueerror.md); раніше поверталося значення **`false`** |

### Приклади

**Пример #1 Пример использования**assert\_options()\*\*\*\*

```php
<?php
// Наша функция обработчик
// неудавшихся проверок
function function assert_failure($file, $line, $assertion, $message)
{
    echo "Проверка $assertion в $file на строке $line провалена: $message";
}

// Тестовая функция
function test_assert($parameter)
{
    assert(is_bool($parameter));
}

// настройки проверки
assert_options(ASSERT_ACTIVE,   true);
assert_options(ASSERT_BAIL,     true);
assert_options(ASSERT_WARNING,  false);
assert_options(ASSERT_CALLBACK, 'assert_failure');

// заведомо ошибочное утверждение
test_assert(1);

// Этот код не будет выполняться, пока ASSERT_BAIL
// равен true
echo 'Никогда не будет выведено';
?>
```

### Дивіться також

-   [assert()](function.assert.md) \- Перевіряє затвердження
