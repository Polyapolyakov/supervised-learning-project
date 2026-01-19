# supervised-learning-project
Проект «Обучение с учителем»

# структура проекта:
**1) Файлы - исходники:**
- market_file.csv;
- market_money.csv;
- market_time.csv;
- money.csv
**2) Файл - проект:**
supervised_learning_project.ipynb

# работа с проектом
supervised_learning_project.ipynb → открыть с помощью → Jupyter Notebook

# установка библиотек и вспомогательных модулей
Работа проекта предусматривает установку следующих библиотек:
- pip install --upgrade pip setuptools wheel
- pip install numpy pandas scipy matplotlib seaborn
- pip install phik --no-deps
- pip install packaging joblib
- pip install shap
- pip install scikit-learn

# описание изменений:
**1) "Стартовые" настройки:**
- лучшей моделью определена модель логистической регрессии LogisticRegression (random_state=42) с использованием L1-регуляризации, с гиперпараметром регуляризации С, равном 3;
-  метрика ROC-AUC - метрика оценки качества модели - на тренировочной выборке (при кросс-валидации) составила 0.8945169136078226, на тестовой выборке - 
0.9023030011234153.
**2) При добавлении параметра n_iter=60 в RandomizedSearchCV**:
- лучшей моделью определена модель логистической регрессии LogisticRegression (random_state=42) с использованием L1-регуляризации, с гиперпараметром регуляризации С, равном 1;
-  метрика ROC-AUC - метрика оценки качества модели - на тренировочной выборке (при кросс-валидации) составила 0.8958151440696895, на тестовой выборке - 
0.9025036109773712.
**3) При изменении параметра "'models__C': range(1, 5)" на "'models__C': range(1, 5)" в настройка гипперпараметров модели LogisticRegression**:
 - получены результаты, анологичные п. 2.