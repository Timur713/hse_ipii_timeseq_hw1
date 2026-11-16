# ДЗ 1 — Online Retail

Выполнен пункт «Подготовка» из задания: окружение, Jupyter Notebook,
загрузка данных, знакомство с полями и выбор товара.
Весь код находится в [preparation.ipynb](preparation.ipynb).

Данные: [UCI Online Retail](https://archive.ics.uci.edu/dataset/352/online+retail),
D. Chen (2015), [DOI: 10.24432/C5BW33](https://doi.org/10.24432/C5BW33), CC BY 4.0.
Сначала Notebook загружает архив из интернета; при ошибке использует
`online+retail.zip` рядом с Notebook. Архив не включается в Git.

## Запуск

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python -m ipykernel install --prefix .venv --name hw1-retail --display-name "Python (hw1-retail)"
jupyter notebook preparation.ipynb
```

Выбрать ядро **Python (hw1-retail)** и выполнить **Restart Kernel and Run All Cells**.
Окружение проверено с Python 3.14.8.

## Результат подготовки

- В датасете 541 909 строк и 8 полей, период 01.12.2010–09.12.2011.
- Изучены типы и значения полей. Есть пропуски в Description и CustomerID;
  исходные записи сохраняются.
- Выбран **20725 — LUNCH BAG RED RETROSPOT**: положительные продажи
  в 298 днях и 13 календарных месяцах, 1 639 исходных строк товара.
- Товар с занятия **85123A** исключён.
- Будущий показатель — количество единиц Quantity, все страны.
  Агрегация, обработка отмен и возвратов и анализ ряда — следующие этапы.

## GitHub

Локальный Git-репозиторий инициализирован. Удалённый репозиторий пока не создан:
доступная интеграция GitHub не предоставляет создание репозитория, GitHub CLI отсутствует.
После создания пустого репозитория на GitHub его можно подключить:

```bash
git remote add origin <URL-репозитория>
git push -u origin main
```
