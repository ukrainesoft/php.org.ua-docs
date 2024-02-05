---
navigation:
  - xsl.examples.md: « Приклади
  - xsl.examples-errors.md: Обробка помилок за допомогою функцій обробки помилок libxml »
  - index.md: PHP Manual
  - xsl.examples.md: Приклади
title: Файли collection.xml та collection.xsl для прикладів
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Файли collection.xml та collection.xsl для прикладів

Багато прикладів у цьому розділі документації містять обидва файли: XML і XSL. Ми будемо використовувати collection.xml та collection.xsl з наступним змістом:

**Приклад #1 collection.xml**

Fight for your mind Ben Harper 1995 Electric Ladyland Jimi Hendrix 1997

**Приклад # 2 collection.xsl**

<xsl:stylesheet version="1.0" xmlns:xsl="[http://www.w3.org/1999/XSL/Transform">](http://www.w3.org/1999/XSL/Transform%22%3E) <xsl:param name="owner" select="'Nicolas Eliaszewicz'"/> <xsl:output method="html" encoding="iso-8859-1" indent="no"/> <xsl:template match="collection"> Hey! Welcome to <xsl:value-of select="$owner"/>'s sweet CD collection! [xsl:apply-templates/](xsl:apply-templates/) <xsl:template match="cd">

# <xsl:value-of select="title"/>

## by <xsl:value-of select="artist"/> - <xsl:value-of select="year"/>

* * *
