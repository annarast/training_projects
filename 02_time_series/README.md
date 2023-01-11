**Описание задачи**  

Построить модель, которая будет прогнозировать количество заказов такси на следующий час.
Требования к модели: значение метрики RMSE на тестовой выборке должно быть не больше 48.   

**Источник данных** 

База исторических данных компании-агрегатора такси за полгода, в которой представлено количетсво заказов с шагом в 10 минут.
Данные содержатся в одном файле.

**Ключевые шаги в решении задачи:**

1. Анализ данных с целью подготовки датасета к обучению (выявление сезонности, обработка пропусков, аномалий, дубликатов).  
2. Анализ данных для понимания, какие признаки можно и нужно использовать для обучения моделей, а какие нет, а также какие признаки можно создать дополнительно на основе уже имеющихся данных. Создание новых признаков (календарные признаки, лаги, скользящее среднее).  
3. Подготовка датасета к обучению: разделение на выборки (без перемешивания).  
4. Выбор моделей для обучения, определение диапазонов гиперпараметров для последующего подбора оптимальных.  
5. Обучение моделей с подбором гиперпараметров, подбор гиперпараметров по лучшему значению RMSE на кросс-валидации (TimeSeriesSplit) с помощью GridSearchCV.  
6. Анализ полученных на разных моделях результатов, выбор лучшей модели с лучшими гиперпараметрами по максимальному значению метрики RMSE и проверка её работоспособности на тестовой выборке.

**Используемые библиотеки и технологии:**  
* pandas
* numpy  
* matplotlib
* seaborn
* sklearn
* lightgbm
* GridSearchCV
* TimeSeriesSplit
* random forest
* linear regression