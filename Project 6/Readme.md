**Классификация клиентов телеком компании**

**Задача:** На основе данных предложить клиенту тариф.

**Ключевые навыки:** классификация, подбор гиперпараметров, выбор модели МО

**Описание:** Оператор мобильной связи выяснил: многие клиенты пользуются архивными тарифами. 

Они хотят построить систему, способную проанализировать поведение клиентов и предложить пользователям один из новых тариф.

---

*Итоги исследования*

Для поиска лучшей модели было сделано:

Были подготовлены данные для обучения моделей: целевой признак "Покупательская активность" приведен к бинарному формату, удалены лишние столбцы

Были сформированы:

паплайны для кодирования и масштабирования категориальных и количественных признаков с помощью кодировщиков OneHotEncoder и OrdinalEncoder, и скейлеров MinMaxScaler и StandardScaler

пайплайны с моделями и с их гиперпараметрами

Была отражена таблица с результатами работы моделей и их лучшими параметрами. Данные были осортированы по убыванию лучшего значения метрики

По итогам отработки пайплайна лучшей моделью оказалсь SVC(kernel='linear', random_state=55) и Метрика ROC-AUC лучшей модели на кросс-валидации: 0.8990 На тестовой выборке Метрика Площадь ROC-кривой на тестовой выборке: 0.9108

Мы использовали один общий пайплайн для всех моделей и инструмент подбора гиперпараметров, который вернул нам лучшую модель
