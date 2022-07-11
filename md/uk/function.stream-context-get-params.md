- [« stream_context_get_options](function.stream-context-get-options.md)
- [stream_context_set_default »](function.stream-context-set-default.md)

- [PHP Manual](index.md)
- [Функції для роботи з потоками](ref.stream.md)
- Отримує параметри із контексту

#stream_context_get_params

(PHP 5 \>= 5.3.0, PHP 7, PHP 8)

stream_context_get_params — Отримує параметри з контексту

### Опис

**stream_context_get_params**(resource `$context`): array

Повертає інформацію про параметри та опції з потоку або контексту.

### Список параметрів

`context`
Ресурс (resource) потоку чи ресурс (resource) [контексту](context.md)

### Значення, що повертаються

Повертає асоціативний масив, що містить усі опції та параметри
контексту.

### Приклади

**Приклад #1 Приклад використання **stream_context_get_params()****

Приклад простого використання

` <?php$ctx = stream_context_create();$params = array("notification" => "stream_notification_callback");stream_context_set_params($ctx, $params);var_dump(stream_context_get_)

Результатом виконання цього прикладу буде щось подібне:

array(2) {
["notification"]=>
string(28) "stream_notification_callback"
["options"]=>
array(0) {
}
}

### Дивіться також

- [stream_context_set_option()](function.stream-context-set-option.md) -
Встановлює опцію для потоку/обгортки/контексту
- [stream_context_set_params()](function.stream-context-set-params.md) -
Встановлює параметри потоку/обгортки/контексту
