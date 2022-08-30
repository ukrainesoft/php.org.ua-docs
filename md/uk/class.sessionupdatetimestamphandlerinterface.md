Інтерфейс SessionUpdateTimestampHandlerInterface

-   [« SessionIdInterface::createsid](sessionidinterface.create-sid.html)
    
-   [SessionUpdateTimestampHandlerInterface::updateTimestamp »](sessionupdatetimestamphandlerinterface.updatetimestamp.html)
    
-   [PHP Manual](index.html)
    
-   [Сессии](book.session.html)
    
-   Інтерфейс SessionUpdateTimestampHandlerInterface
    

# Інтерфейс SessionUpdateTimestampHandlerInterface

(PHP 7, PHP 8)

## Вступ

**SessionUpdateTimestampHandlerInterface** - це інтерфейс, який визначає додаткові методи для створення користувальницького оброблювача сесії. Для надання користувальницького оброблювача сесії функції [sessionsetsavehandler()](function.session-set-save-handler.html), Використовуючи її ООП реалізацію, клас повинен реалізовувати цей інтерфейс.

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

-   [SessionUpdateTimestampHandlerInterface::updateTimestamp](sessionupdatetimestamphandlerinterface.updatetimestamp.html) — Оновити позначку часу
-   [SessionUpdateTimestampHandlerInterface::validateId](sessionupdatetimestamphandlerinterface.validateid.html) - Перевірити ідентифікатор