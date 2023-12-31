# Предсказание стоимости поддержанных автомобилей

## Стек

- EDA: `Matplotlib`, `pandas`, `seaborn`
- Подготовка данных и обучение моделей: `CatBoost`, `LightGBM`, `NumPy`, `scikit-learn`   

## Задача

Построить модель для определения рыночной стоимости подержанных автомобилей для сервиса по продаже автомобилей.

Модель будет использована в приложении, которое разрабатывется для привлечения новых клиентов.

Модель должна демонстировать качество прогноза `RMSE` не более 2500, а также быстрое время обучения и предсказания.

## Предоставленные данные

Историчекие данные сервиса о технических характеристиках, комплектации и ценах других автомобилей.

Согласно описанию к данным:

- `Brand` — марка автомобиля;
- `DateCrawled` — дата скачивания анкеты из базы;
- `DateCreated` — дата создания анкеты;
- `FuelType` — тип топлива;
- `Gearbox` — тип коробки передач;
- `Kilometer` — пробег (км);
- `LastSeen` — дата последней активности пользователя;
- `Model` — модель автомобиля;
- `NotRepaired` — была машина в ремонте или нет;
- `NumberOfPictures` — количество фотографий автомобиля;
- `PostalCode` — почтовый индекс владельца анкеты (пользователя);
- `Power` — мощность (л. с.);
- `Price` — цена в евро (**целевой признак**);
- `RegistrationMonth` — месяц регистрации автомобиля;
- `RegistrationYear` — год регистрации автомобиля;
- `VehicleType` — тип автомобильного кузова.

## Основные этапы работы

Работа над задачей включала семь этапов:

1. загрузка и изучение данных;
2. подготовка данных; 
3. подготовка выборок к обучению моделей;
4. обучение моделей;
5. анализ моделей;
6. повторное обучение моделей; и
7. выбор и тестирование лучшей модели.

## Результат работы

По результатам работы заказчику была предложена  модель `CatBoostRegressor`, которая показала на тестовой выборке `RMSE` 1539, что на 38% лучше целевого значения.
