# Анализ комментариев интернет-магазина

### Описание проекта

Интернет-магазин «Викишоп» запускает новый сервис. Теперь пользователи могут редактировать и дополнять описания товаров, как в вики-сообществах. То есть клиенты предлагают свои правки и комментируют изменения других. Магазину нужен инструмент, который будет искать токсичные комментарии и отправлять их на модерацию.

Обучите модель классифицировать комментарии на позитивные и негативные. В вашем распоряжении набор данных с разметкой о токсичности правок.

Постройте модель со значением метрики качества F1 не меньше 0.75.

## Навыки и инструменты

- **python**
- **pandas**
- **numpy**
- **pymystem3**
- **spacy**
- nltk.corpus.**nltk_stopwords**
- sklearn.feature_extraction.text.**TfidfVectorizer**
- sklearn.linear_model.**LogisticRegression**
- sklearn.model_selection.**train_test_split**
- sklearn.model_selection.**RandomizedSearchCV**
- sklearn.metrics.**f1_score**
- sklearn.pipeline.**Pipeline**
- sklearn.compose.**ColumnTransformer**
- sklearn.tree.**DecisionTreeClassifier**
- lightgbm.**LGBMRegressor**
- catboost.**CatBoostClassifier**

## 

## Общий вывод

В ходе проекта:

Загрузили и подготовили данные. Был отмечен сильный дисбаланс классов в целевом признаке. Провели лемматизацию и очистку текста с помощью SpaCy. Рассчитали величины TF-IDF для создания признаков для обучения моделей

Были обучены три модели: LogisticRegression, DecisionTreeClassifier, CatBoostClassifier. С помощью RandomizedSearchCV нашли лучшую модель с метрикой LogisticRegression на тренировочной выборке f1 - 0.76.

На тестовой выборке получили метрику f1 - 0.76
