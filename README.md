# 📦 DBHose Developer PyPI

Этот репозиторий автоматически собирает и предоставляет единый Python-пакетный индекс (совместимый с PEP 503) для dev-сборок из нескольких репозиториев организации **DNS Technologies**.

**Адрес индекса:** [https://dns-technologies.github.io/dbhose-dev-pip/](https://dns-technologies.github.io/dbhose-dev-pip/)

![Снимок страницы индекса](screenshot.png) *(Вы можете добавить скриншот вашей страницы)*

## 📋 Список доступных пакетов

На данный момент в индексе автоматически публикуются следующие пакеты:

*   [`light-compressor`](https://github.com/dns-technologies/light-compressor) — последняя версия: `0.1.0.dev0`
*   [`native-dumper`](https://github.com/dns-technologies/native-dumper) — последняя версия: `0.3.6.dev0`
*   [`nativelib`](https://github.com/dns-technologies/nativelib) — последняя версия: `0.2.3.dev1`
*   [`pgpack-dumper`](https://github.com/dns-technologies/pgpack_dumper) — последняя версия: `0.3.6.dev0`

Список автоматически обновляется при появлении новых релизов в исходных репозиториях.

## 🚀 Как использовать

Добавьте этот индекс как дополнительный источник пакетов (`extra-index-url`) при установке через `pip`.

### В командной строке

```bash
# Установка конкретного пакета
pip install --extra-index-url https://dns-technologies.github.io/dbhose-dev-pip/simple/ pgpack-dumper

# Установка с приоритетом вашего индекса (сначала ищет здесь, потом на PyPI)
pip install --index-url https://dns-technologies.github.io/dbhose-dev-pip/simple/ --extra-index-url https://pypi.org/simple pgpack-dumper
```

### В requirements.txt

```text
# requirements.txt
--extra-index-url https://dns-technologies.github.io/dbhose-dev-pip/simple/
pgpack-dumper
native-dumper
light-compressor
```

### В pyproject.toml (для Poetry)

```toml
[[tool.poetry.source]]
name = "dbhose-dev"
url = "https://dns-technologies.github.io/dbhose-dev-pip/simple/"
default = false
```
