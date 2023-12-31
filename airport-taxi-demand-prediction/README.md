# Прогнозирование количества заказов такси в аэропорту

## Стек

- EDA: `Matplotlib`, `pandas`, `seaborn`, `statsmodels`<br>
- Подготовка данных и обучение моделей: `CatBoost`, `Optuna`, `scikit-learn`, `StatsForecast`, `XGBoost`

## Задача

Построить модель для прогнозирования количества заказов такси в аэропортах на следующий час для агрегатора такси.

На основе предсказаний модели планируется привлекать больше водителей в периоды пиковой нагрузки.

Модель должна демонстрировать качество прогноза `RMSE` не больше 48 на тестовой выборке размером 10% от исходных данных.

## Предоставленные данные

Исторические данные компании о заказах такси в аэропортах.

Согласно описанию к данным, количество заказов (целевой признак) — значения столбца `num_orders`.

## Основные этапы работы

Работа над задачей включала шесть этапов:

1. загрузка и первичное изучение данных;
2. подготовка данных для исследовательского анализа;
3. исследовательский анализ данных;
4. подготовка данных для обучения моделей;
5. обучение моделей; и
6. тестирование моделей.

## Результат работы

По результатам работы заказчику была предложена линейная модель `LinearRegression`, которая показала на тестовой выборке лучшее значение `RMSE` (35.14), что на 27% лучше целевого значения.        
