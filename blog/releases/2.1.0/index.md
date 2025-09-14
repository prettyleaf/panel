---
title: Release v2.1.0
authors: remnawave
tags: [release]
date: 2025-08-13
---

# Release v2.1.0

**🚧 Полное обновление обязательно 🚧**

Этот релиз содержит обновления всех компонентов Remnawave. Пожалуйста, внимательно ознакомьтесь с этим документом перед обновлением.

<!-- truncate -->

Хоть и новая версия панели _будет_ работать со старой версией Remnawave Node (до v2.1.0), мы настоятельно рекомендуем обновить Remnawave Node до версии v2.1.0.

## Remnawave Panel v2.1.0

### 🔄 Breaking Changes

- Через [API](/api#tag/users-controller/patch/api/users) более невозможно обновить статус пользователя на **LIMITED**, **EXPIRED**.

### Обновление

```bash
cd /opt/remnawave && docker compose pull remnawave && docker compose down && docker compose up -d && docker compose logs -f -t
```

## Remnawave Node v2.1.0

### 🔄 Breaking Changes

- Версия Remnawave Node v2.1.0 несовместима с версиями панели до v2.1.0.

### Прочие изменения

- Версия Xray Core обновлена до v25.8.3.

### Обновление

```bash
cd /opt/remnanode && docker compose pull remnanode && docker compose down && docker compose up -d && docker compose logs -f -t
```

## Remnawave Subscription Page v6.0.0

В версии v6.0.0 был обновлен формат `app-config.json` до новой версии, которая позволяет отключить неиспользуемые языки, а так же кастомизировать имя бренда и добавить логотип.

Встроенный в панель билдер был так же обновлен для поддержки нового формата `app-config.json`.

### Обновление

```bash
cd /opt/remnawave/subscription && docker compose pull && docker compose down && docker compose up -d && docker compose logs -f -t
```
