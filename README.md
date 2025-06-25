# RQLite

[![License](https://img.shields.io/badge/license-MIT)](LICENSE)
[![Build Status](https://github.com/LigeronAhill/sqlite/actions/workflows/ci.yml/badge.svg)](https://github.com/yourusername/rqlite/actions)

**RQLite** (Rust Query Lite) — это легковесная встраиваемая SQL-база данных, написанная на Rust, вдохновлённая SQLite.

## Особенности

- Поддержка подмножества SQL (SELECT, INSERT, CREATE TABLE и др.).
- Хранение данных в одном файле (как SQLite).
- Без сервера — работает как библиотека.
- ACID-транзакции (в планах).

## Пример использования (пока выдуманный)

```rust
use rqlite::Database;

let mut db = Database::open("test.db")?;
db.execute("CREATE TABLE users (id INTEGER, name TEXT);")?;
db.execute("INSERT INTO users VALUES (1, 'Alice');")?;
let results = db.execute("SELECT * FROM users;")?;
```
