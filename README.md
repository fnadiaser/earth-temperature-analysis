# Изменение температуры поверхности Земли

Курсовая работа: подготовка и разведочный анализ исторических данных о температуре суши и океана.

## Данные
[Berkeley Earth, Kaggle](https://www.kaggle.com/datasets/berkeleyearth/climate-change-earth-surface-temperature-data):
- `GlobalTemperatures` — 3 192 месяца, 1750–2015;
- `GlobalLandTemperaturesByCountry` — 577 462 наблюдения, 243 страны;
- `GlobalLandTemperaturesByMajorCity` — 239 177 наблюдений.

## Что сделано
1. **Временные ряды:** даты переведены в `DatetimeIndex`.
2. **Пропуски:** в средней температуре суши (0,4%) заполнены временной интерполяцией; по странам (5,6%) — интерполяцией внутри каждой страны; показатели с 37,6% пропусков анализировались только на периоде, где они есть.
3. **Выбросы:** поиск по IQR; в данных по странам удалено менее 1,5% выбросов.
4. **Взаимосвязи:** распределения температур, связь температуры суши и океана, динамика по годам.

## Инструменты
Python · pandas · NumPy · Matplotlib · Seaborn · Plotly

## Как запустить
```bash
pip install pandas numpy matplotlib seaborn plotly
jupyter notebook earth_temperature.ipynb
```
CSV-файлы скачать с Kaggle по ссылке выше (в репозиторий не загружены из-за размера).
