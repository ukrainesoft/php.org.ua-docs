---
navigation:
  - sessionidinterface.create-sid.md: '« SessionIdInterface::create\_sid'
  - sessionupdatetimestamphandlerinterface.updatetimestamp.md: 'SessionUpdateTimestampHandlerInterface::updateTimestamp »'
  - index.md: PHP Manual
  - book.session.md: Сесії
title: Інтерфейс SessionUpdateTimestampHandlerInterface
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс SessionUpdateTimestampHandlerInterface

(PHP 7, PHP 8)

## Вступ

**SessionUpdateTimestampHandlerInterface** - це інтерфейс, який визначає додаткові методи для створення користувальницького оброблювача сесії. Для надання користувальницького оброблювача сесії функції [session\_set\_save\_handler()](function.session-set-save-handler.md), Використовуючи її ООП реалізацію, клас повинен реалізовувати цей інтерфейс.

Зауважте, що callback-методи цього класу створені для внутрішніх викликів PHP і не призначені для викликів з вашого коду.

## Огляд класів

```classsynopsis

    
     interface SessionUpdateTimestampHandlerInterface {

    /* Методы */
    
   public updateTimestamp(string $id, string $data): bool
public validateId(string $id): bool

   }
```

## Зміст

-   [SessionUpdateTimestampHandlerInterface::updateTimestamp](sessionupdatetimestamphandlerinterface.updatetimestamp.md)— Оновити позначку часу
-   [SessionUpdateTimestampHandlerInterface::validateId](sessionupdatetimestamphandlerinterface.validateid.md) \- Перевірити ідентифікатор
