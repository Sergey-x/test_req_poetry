Poetry
==============


Docs: https://python-poetry.org/docs

Полезное:
* https://habr.com/ru/articles/740376/

## 1. Установка


## 2. Базовое использование

### 2.1. Создание `pyproject.toml`:

```shell
poetry init
```


### 2.2. Активация виртуального окружения:
```shell
poetry shell
```

Все окружения лежат в `C:\Users\${username}\AppData\Local\pypoetry\Cache\virtualenvs`


### 2.3. Добавление зависимостей:

* Основные зависимости (аналог pip install)
    ```shell
    poetry add flake8
    ```

* Зависимости для разработки
    ```shell
    poetry add --group=dev flake8
    ```


### 2.4. Установка зависимостей из существующего файла `pyproject.toml`:

* Все зависимости (аналог pip install -r requirements.txt)
    ```shell
    poetry install
    ```

* Без зависимостей для разработки
    ```shell
    poetry install --without=dev
    ```


### 2.5. Установка зависимостей из wheels:
TODO

### 2.6. Выход из виртуального окружения

```shell
exit
```



## 3. Дополнительно:


### Конвертация в requirements.txt
* По умолчанию, без зависимостей для разработки

```shell
poetry export --without-hashes -o requirements.txt
```

* C зависимостями для разработки

```shell
poetry export --with=dev --without-hashes -o requirements.txt
```

### Конвертация из requirements.txt

```shell
poetry add `cat requirements.txt`
```



https://stackoverflow.com/questions/62764148/how-to-import-requirements-txt-from-an-existing-project-using-poetry
