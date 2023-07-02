# Прогнозирование ухода клиентов оператора связи

## Задача

Построить для оператора связи модель, которая будет прогнозировать уход клиентов.

На основе предсказаний модели планируется предлагать таким «уходящим» клиентам промокоды и специальные условия.

Модель должна демонстировать качество прогноза `AUC-ROC` не ниже `0.85`. Дополнительная метрика — `Accuracy`.

## Предоставленные данные

Полученные из разных источников персональные данные о некоторых клиентах и информация об их тарифах и договорах в форме четырех файлов:

- `contract.csv` — информация о клиентских договорах;
- `personal.csv` — персональные данные клиентов;
- `internet.csv` — информация об оказываемых клиентам интернет-услугах;
- `phone.csv` — информация об оказываемых клиентам услугах телефонии.

## Основные этапы работы

Работа над задачей включала шесть этапов:

1. загрузка и первичное изучение данных;
2. подготовка данных для исследовательского анализа;
3. исследовательский анализ данных;
4. подготовка данных для обучения моделей;
5. обучение моделей; и
6. тестирование моделей.

## Результат работы

По результатам работы заказчику были предложены три модели (каждая из которых продемонстировала качество прогноза `AUC-ROC` на тестовой выборке не ниже `0.85`):

- модель `StackingClassifier` как лучшая по метрикам `AUC-ROC` (`0.9207`) и `Accuracy` (`0.8751`);
- модель `CatBoostClassifier`, наиболее точно предсказывающая уход клиентов; и
- модель `XGBClassifier`, наиболее полно предсказывающая «уходящих» клиентов (среди моделей, показавших значение `AUC-ROC` выше целевого значения).