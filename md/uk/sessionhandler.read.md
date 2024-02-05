---
navigation:
  - sessionhandler.open.md: '« SessionHandler::open'
  - sessionhandler.write.md: 'SessionHandler::write »'
  - index.md: PHP Manual
  - class.sessionhandler.md: SessionHandler
title: 'SessionHandler::read'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SessionHandler::read

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

SessionHandler::read — Зчитує дані сесії

### Опис

```methodsynopsis
public SessionHandler::read(string $id): string|false
```

Зчитує дані сесії зі сховища та повертає результат назад у PHP для внутрішньої обробки. Цей метод викликається автоматично, коли PHP стартує сесію (або автоматично або безпосередньо викликом. [session\_start()](function.session-start.md) з наступним викликом [SessionHandler::open()](sessionhandler.open.md)

Цей метод є обертанням внутрішнього обробника PHP, визначеного в параметрі ini-файлу [session.save\_handler](session.configuration.md#ini.session.save-handler) який встановлюється до того, як буде визначено оброблювач сесії викликом [session\_set\_save\_handler()](function.session-set-save-handler.md)

Якщо цей клас розширено шляхом успадкування, виклик батьківського методу `read` викликає обгортку для цього методу і, відповідно, виклик внутрішнього оброблювача. Це дозволяє методу бути перевантаженим, та/або перехопленим та відфільтрованим (наприклад для розшифровки, значення параметра `$data`, що повертає батьківський метод `read`

Для дополнительной информации смотрите документацию по методу[SessionHandlerInterface::read()](sessionhandlerinterface.read.md)

### Список параметрів

`id`

Ідентифікатор сесії, з якої необхідно рахувати дані.

### Значення, що повертаються

Повертає зашифрований рядок лічених даних. Якщо нічого не раховано, повертається **`false`**. Зверніть увагу, що це значення повертається до PHP для внутрішньої обробки.

### Дивіться також

-   Директива налаштування[session.serialize\_handler](session.configuration.md#ini.session.serialize-handler)
