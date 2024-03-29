---
navigation:
  - ev.nowupdate.md: '« Ev::nowUpdate'
  - ev.resume.md: 'Ev::resume »'
  - index.md: PHP Manual
  - class.ev.md: Ev
title: 'Ev::recommendedBackends'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ev::recommendedBackends

(PECL ev >= 0.2.0)

Ev::recommendedBackends — Отримати бітову маску рекомендованих бекендів для даної платформи

### Опис

```methodsynopsis
final
   public
   static
   Ev::recommendedBackends(): int
```

Повертає набір всіх бекендів, вбудованих у використовувану `libev` і, також, рекомендованих для цієї платформи, у тому сенсі, що вони будуть працювати з більшістю типів дескрипторів файлів. Зазвичай цей список менший, ніж той, що повертається \*\*ev\_supported\_backends()\*\*К Прикладу,`kqueue` не працює на більшості систем `BSD` і не буде автовизначений, якщо ви примусово його не запросите. Це набір бекендів які опитуватиме `libev`якщо бекенд не заданий у явному вигляді.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає бітову маску, що містить [прапори бекенда](class.ev.md#ev.constants.watcher-backends), об'єднані за допомогою побітового *АБО*

### Приклади

**Приклад #1 Вбудовування одного циклу в інший**

```php
<?php
/*
* Попытаемся получить встраиваемый событийный цикл и встроить его в
* событийный цикл по умолчанию.
* Если это невозможно - используем цикл по умолчанию.
* Цикл по умолчанию хранится в $loop_hi, а встраиваемый в $loop_lo
* (который равен $loop_hi в случае, если нельзя использовать встраиваемый цикл).
*
* Приклад взят с сайта
* http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#Examples_CONTENT-9
*/
$loop_hi = EvLoop::defaultLoop();
$loop_lo = NULL;
$embed   = NULL;

/*
* Смотрим, есть ли хотя бы один подходящий бэкенд
* (флаг 0 означает автоопределение)
*/
$loop_lo = Ev::embeddableBackends() & Ev::recommendedBackends()
 ? new EvLoop(Ev::embeddableBackends() & Ev::recommendedBackends())
 : 0;

if ($loop_lo) {
 $embed = new EvEmbed($loop_lo, function () {});
} else {
 $loop_lo = $loop_hi;
}
?>
```

### Дивіться також

-   [EvEmbed](class.evembed.md)
-   [Ev::embeddableBackends()](ev.embeddablebackends.md) \- Повертає набір бекендів, які можна вбудувати в інші цикли подій
-   [Ev::supportedBackends()](ev.supportedbackends.md) \- Повертає набір бекендів, які підтримуються поточною конфігурацією libev
-   [Прапори бекенда](class.ev.md#ev.constants.watcher-backends)
-   [Приклади](ev.examples.md)
