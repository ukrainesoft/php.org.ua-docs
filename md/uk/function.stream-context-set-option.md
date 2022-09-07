---
navigation:
  - function.stream-context-set-default.md: « streamcontextsetdefault
  - function.stream-context-set-params.md: streamcontextsetparams »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: streamcontextsetoption
---
# streamcontextsetoption

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

streamcontextsetoption — Встановлює опцію для потоку/обгортки/контексту

### Опис

```methodsynopsis
stream_context_set_option(    resource $stream_or_context,    string $wrapper,    string $option,    mixed $value): bool
```

```methodsynopsis
stream_context_set_option(resource $stream_or_context, array $options): bool
```

Встановлює опцію у вказаному контексті. Значення `value` встановлюється в `option` для `wrapper`

### Список параметрів

`stream_or_context`

Потік або ресурс контексту, до якого будуть використані опції.

`wrapper`

Ім'я обгортки (може відрізнятися від протоколу). Дивіться [опції та параметри контексту](context.md) для отримання списку параметрів потоку.

`option`

Ім'я опції.

`value`

Значення опції.

`options`

Опції, які будуть застосовані до `stream_or_context`

> **Зауваження**
> 
> Параметр `options` має бути асоціативним масивом асоціативних масивів у форматі `$arr['wrapper']['option'] = $value`
> 
> Зверніться до розділу [опції та параметри контексту](context.md), щоб отримати список опцій потоку.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
