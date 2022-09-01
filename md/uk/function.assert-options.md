---
navigation:
  - ref.info.md: « Опції PHP/інформаційні функції
  - function.assert.md: assert »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: assertoptions
---
# assertoptions

(PHP 4, PHP 5, PHP 7, PHP 8)

assertoptions — Встановлення та отримання параметрів механізму перевірки тверджень

### Опис

```methodsynopsis
assert_options(int $what, mixed $value = ?): mixed
```

Завдання значень параметрів механізму перевірки тверджень [assert()](function.assert.md) або одержання їх поточних значень.

> **Зауваження**: Починаючи з PHP 7.0.0, використання **assertoptions()** не рекомендується на користь встановлення та отримання php.ini директив [zend.assertions](ini.core.html#ini.zend.assertions) і [assert.exception](info.configuration.html#ini.assert.exception) за допомогою [iniset()](function.ini-set.html) і [iniget()](function.ini-get.html) відповідно.

### Список параметрів

`what`

**Налаштування механізму перевірки тверджень**

| Настройка | INI-параметр | Значение по умолчанию | Описание |
| --- | --- | --- | --- |
| ASSERTACTIVE | assert.active |  | включення механізму перевірки тверджень |
| ASSERTWARNING | assert.warning |  | виведення попередження PHP для кожної невдалої перевірки |
| ASSERTBAIL | assert.bail |  | завершити виконання у разі невдалої перевірки |
| ASSERTQUIETEVAL | assert.quieteval |  | відключити errorreporting під час перевірки затвердження |
| ASSERTCALLBACK | assert.callback | **`null`** | Callback-функція, яку необхідно викликати для затвердження, що провалило перевірку |

`value`

Необов'язковий аргумент, нове значення налаштування.

Callback-функція, встановлена ​​за допомогою **`ASSERT_CALLBACK`** або assert.callback, повинен мати наступний підпис:

```methodsynopsis
assert_callback(    string $file,    int $line,    string $assertion,    string $description = ?): void
```

`file`

Файл, у якому було викликано [assert()](function.assert.md)

`line`

Рядок, в якому був викликаний [assert()](function.assert.md)

`assertion`

Твердження, яке було передано до [assert()](function.assert.md), перетворений на рядок.

`description`

Опис, яке було передано до [assert()](function.assert.md)

Передача порожнього рядка в `value` скидає assert callback.

### Значення, що повертаються

Повертає вихідне значення налаштування або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **assertoptions()****

```php
<?php
// Наша функция обработчик
// неудавшихся проверок
function function assert_failure($file, $line, $assertion, $message)
{
    echo "Проверка $assertion в $file на строке $line провалена: $message";
}

// Тестовая функция
function test_assert($parameter)
{
    assert(is_bool($parameter));
}

// настройки проверки
assert_options(ASSERT_ACTIVE,   true);
assert_options(ASSERT_BAIL,     true);
assert_options(ASSERT_WARNING,  false);
assert_options(ASSERT_CALLBACK, 'assert_failure');

// заведомо ошибочное утверждение
test_assert(1);

// Этот код не будет выполняться, пока ASSERT_BAIL
// равен true
echo 'Никогда не будет выведено';
?>
```

### Дивіться також

-   [assert()](function.assert.md) - Перевіряє, чи є твердження false
