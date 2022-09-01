---
navigation:
  - sessionhandlerinterface.write.md: '« SessionHandlerInterface::write'
  - sessionidinterface.create-sid.html: 'SessionIdInterface::createsid »'
  - index.md: PHP Manual
  - book.session.md: Сессии
title: Інтерфейс SessionIdInterface
---
# Інтерфейс SessionIdInterface

(PHP 5> = 5.5.1, PHP 7, PHP 8)

## Вступ

**SessionIdInterface** - це інтерфейс, який визначає необов'язкові методи для створення користувача сесії. Для надання користувальницького оброблювача сесії функції [sessionsetsavehandler()](function.session-set-save-handler.html), Використовуючи її ООП реалізацію, клас повинен реалізовувати цей інтерфейс.

Зауважте, що callback-методи цього класу створені для внутрішніх викликів PHP і не призначені для викликів з вашого коду.

## Огляд інтерфейсів

```classsynopsis

     
    

    
     
      interface SessionIdInterface {

    /* Методы */
    
   public create_sid(): string

   }
```

## Зміст

-   [SessionIdInterface::createsid](sessionidinterface.create-sid.html) — Створити ідентифікатор сесії
