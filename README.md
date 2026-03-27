# 📦 DBHose Developer PyPI

Этот репозиторий автоматически собирает и предоставляет единый Python-пакетный индекс (совместимый с PEP 503) для dev-сборок из нескольких репозиториев организации **DNS Technologies**.

**Адрес индекса:** [https://dns-technologies.github.io/dbhose-dev-pip/](https://dns-technologies.github.io/dbhose-dev-pip/)

## 📋 Список доступных пакетов

На данный момент в индексе автоматически публикуются следующие пакеты:

*   [`light-compressor`](https://github.com/dns-technologies/light_compressor)
*   [`csvpack`](https://github.com/dns-technologies/csvpack)
*   [`pgcopylib`](https://github.com/dns-technologies/pgcopylib)
*   [`pgpack`](https://github.com/dns-technologies/pgpack)
*   [`nativelib`](https://github.com/dns-technologies/nativelib)
*   [`base-dumper`](https://github.com/dns-technologies/base_dumper)
*   [`native-dumper`](https://github.com/dns-technologies/native_dumper)
*   [`pgpack-dumper`](https://github.com/dns-technologies/pgpack_dumper)
*   [`dbhose-utils`](https://github.com/dns-technologies/dbhose_utils)
*   [`dbhose-airflow`](https://github.com/dns-technologies/dbhose_airflow)

Версии автоматически обновляются при появлении новых релизов в исходных репозиториях.

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
