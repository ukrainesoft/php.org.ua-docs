---
navigation:
  - splfileobject.seek.md: '« SplFileObject::seek'
  - splfileobject.setflags.md: 'SplFileObject::setFlags »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::setCsvControl'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::setCsvControl

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

SplFileObject::setCsvControl — Встановлює символи роздільника, обгортання та екранування для CSV

### Опис

```methodsynopsis
public SplFileObject::setCsvControl(string $separator = ",", string $enclosure = "\"", string $escape = "\\"): void
```

Встановлює символи роздільника, обмежувача та екранування для CSV. Символ обмежувача використовується для розміщення значень полів. Наприклад, рядок 'рядок' обгорнутий в одиночні лапки (').

### Список параметрів

`separator`

Розділювач поля (тільки один однобайтовий символ).

`enclosure`

Обмежувач поля символ (лише один однобайтовий символ).

`escape`

Екрануючий символ (не більше одного однобайтового символу). Порожня стрічка (`""`) відключає пропрієтарний механізм екранування.

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 7.4.0 | Тепер параметр `escape` може приймати порожній рядок для вимкнення пропрієтарного механізму екранування. |

### Приклади

**Пример #1 Пример использования**SplFileObject::setCsvControl()\*\*\*\*

```php
<?php
$file = new SplFileObject("data.csv");
$file->setFlags(SplFileObject::READ_CSV);
$file->setCsvControl('|');
foreach ($file as $row) {
    list ($fruit, $quantity) = $row;
    // Что-то делаем со значениями
}
?>
```

Вміст data.csv

### Дивіться також

-   [SplFileObject::getCsvControl()](splfileobject.getcsvcontrol.md) \- Отримує символи роздільника, обгортання та екранування для CSV
-   [SplFileObject::fgetcsv()](splfileobject.fgetcsv.md) \- Отримати рядок із файлу та його розбір як поля CSV
