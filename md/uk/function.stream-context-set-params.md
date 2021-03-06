- [« stream_context_set_option](function.stream-context-set-option.md)
- [stream_copy_to_stream »](function.stream-copy-to-stream.md)

- [PHP Manual](index.md)
- [Функції для роботи з потоками](ref.stream.md)
- Встановлює параметри потоку/обгортки/контексту

#stream_context_set_params

(PHP 4 \>= 4.3.0, PHP 5, PHP 7, PHP 8)

stream_context_set_params — Встановлює параметри для
потоку/обгортки/контексту

### Опис

**stream_context_set_params**(resource `$context`, array `$params`):
bool

Встановлює настройки для зазначеного контексту.

### Список параметрів

`context`
Потік або контекст, до якого будуть використані параметри.

`params`
Асоціативний масив параметрів, які будуть встановлені в наступному
формат: $params['paramname'] = "paramvalue";`.

| Параметр | Призначення                                        |
|----------|----------------------------------------------------|
| options  | Масив [опцій та параметрів контексту](context.md). |

**Підтримувані параметри**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Дивіться також

- [stream_notification_callback()](function.stream-notification-callback.md) -
Callback-функція для параметра контексту notification
