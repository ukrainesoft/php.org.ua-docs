---
navigation:
  - imagick.clipimagepath.md: '« Imagick::clipImagePath'
  - imagick.clone.md: 'Imagick::clone »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::clipPathImage'
---
# Imagick::clipPathImage

(PECL imagick 2, PECL imagick 3)

Imagick::clipPathImage — Відсікти уздовж зазначеного контуру з профілем 8BIM

### Опис

```methodsynopsis
public Imagick::clipPathImage(string $pathname, bool $inside): bool
```

Відсікає зображення вздовж зазначеного контуру з профілем 8BIM, якщо воно надано. Наступні операції застосовуватимуться до внутрішнього контуру. Також може бути числом, якщо йому передує символ #. Це необхідно для роботи з пронумерованими контурами, наприклад "#1" для використання першого контуру.

### Список параметрів

`pathname`

Позначений контур

`inside`

Якщо встановлено **`true`**, то наступні операції застосовуватимуться до внутрішнього контуру. Інакше наступні операції будуть застосовуватися до зовнішнього контуру.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
