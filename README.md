<p align="center">
  <img src="https://img.shields.io/badge/статус-в%20разработке-yellow?style=for-the-badge&labelColor=gray" alt="Статус"/>
  <img src="https://img.shields.io/badge/версия-1.0.0-blue?style=for-the-badge&labelColor=gray" alt="Версия"/>
  <img src="https://img.shields.io/badge/лицензия-MIT-green?style=for-the-badge&labelColor=gray" alt="Лицензия"/>
  <img src="https://img.shields.io/badge/windows-10%2F11-purple?style=for-the-badge&labelColor=gray" alt="Windows"/>
</p>

<h1 align="center">Veto</h1>

<p align="center">
  <b>DPI Bypass Engine</b><br>
  Лёгкий движок для обхода DPI<br>
  Альтернатива zapret / nfqws
</p>

<p align="center">
  <a href="#-что-это">Русский</a> • <a href="#-what-is-this">English</a>
</p>

---

# 🇷🇺 Русский

> **⚠️ Статус: В разработке**
> Проект находится на ранней стадии разработки. API и функциональность могут измениться.

## Что это?

Veto — это самописный движок для обхода DPI (Deep Packet Inspection), разработанный как более лёгкая и быстрая альтернатива [zapret](https://github.com/Flowseal/zapret-discord-youtube). Движок использует WinDivert для перехвата пакетов на уровне ядра и применяет различные техники обхода глубокой инспекции пакетов.

## Возможности

| Модуль | Описание |
|--------|----------|
| **Fake** | Подмена TTL для обмана DPI |
| **Split** | Разделение TCP-сегментов |
| **Disorder** | Нарушение порядка TCP-сегментов |
| **Hostlists** | Маршрутизация по спискам доменов (835+ доменов) |
| **Lua** | Скриптинг стратегий обхода |
| **Config** | TOML конфигурация с профилями |
| **Capture** | Перехват пакетов через WinDivert |

## Сборка

```bash
# Требуется CMake 3.10+ и GCC/MinGW
build.bat
```

## Структура

```
veto/
├── include/           # Заголовочные файлы
├── src/
│   ├── core/          # Основной движок
│   ├── protocols/     # Парсинг протоколов
│   ├── attacks/       # Модули атак
│   ├── capture/       # Перехват через WinDivert
│   └── config/        # Конфигурация
├── lib/               # WinDivert библиотеки
├── files/             # Hostlist файлы (10 категорий)
├── strategies/        # Lua стратегии обхода
└── veto.conf          # Конфигурация
```

## Быстрый старт

```bash
# 1. Собрать
build.bat

# 2. Запустить (от администратора)
run-admin.bat

# 3. Или запустить с конкретным профилем
veto.exe --config veto.conf --profile youtube
```

## Лицензия

MIT License — свободное использование и модификация

---

# 🇬🇧 English

> **⚠️ Status: In Development**
> This project is in early development. API and functionality may change.

## What is this?

Veto is a custom DPI (Deep Packet Inspection) bypass engine, designed as a lighter and faster alternative to [zapret](https://github.com/Flowseal/zapret-discord-youtube). The engine uses WinDivert for kernel-level packet interception and applies various DPI bypass techniques.

## Features

| Module | Description |
|--------|-------------|
| **Fake** | TTL spoofing to deceive DPI |
| **Split** | TCP segment splitting |
| **Disorder** | TCP segment reordering |
| **Hostlists** | Domain-based routing (835+ domains) |
| **Lua** | Bypass strategy scripting |
| **Config** | TOML configuration with profiles |
| **Capture** | Packet interception via WinDivert |

## Building

```bash
# Requires CMake 3.10+ and GCC/MinGW
build.bat
```

## Project Structure

```
veto/
├── include/           # Header files
├── src/
│   ├── core/          # Core engine
│   ├── protocols/     # Protocol parsing
│   ├── attacks/       # Attack modules
│   ├── capture/       # WinDivert capture
│   └── config/        # Configuration
├── lib/               # WinDivert libraries
├── files/             # Hostlist files (10 categories)
├── strategies/        # Lua bypass strategies
└── veto.conf          # Configuration
```

## Quick Start

```bash
# 1. Build
build.bat

# 2. Run (as administrator)
run-admin.bat

# 3. Or run with a specific profile
veto.exe --config veto.conf --profile youtube
```

## License

MIT License — free to use and modify

---

<p align="center">
  <sub>Made by <a href="https://github.com/R3G1ST">R3G1ST</a></sub>
</p>
