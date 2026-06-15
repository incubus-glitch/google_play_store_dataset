# 📱 Google Play Store Classification Project

Проект посвящён задаче машинного обучения на реальном датасете Google Play Store. Цель — построить и сравнить модели, которые предсказывают, является ли приложение Free или Paid, на основе его метаданных.

---

## 🎯 Цель проекта

Построить модель бинарной классификации, которая по характеристикам приложения определяет его тип:

- Free
- Paid

---

## 📁 Структура проекта

google_play_store_dataset/
data/
googleplaystore.csv

notebooks/
classifier_googleplaystore.ipynb
pandas_for_students_base_v3.ipynb
pandas_for_students_pro_v3.ipynb

requirements.txt
README.md

---

## 📊 Описание данных

Используется датасет Google Play Store:

- App
- Category
- Rating
- Reviews
- Size
- Installs
- Type (target)
- Price
- Content Rating
- Genres
- Last Updated
- Current Ver
- Android Ver

---

## 🧹 Предобработка данных

- Удаление выбросов и дубликатов
- Заполнение пропусков (median / mode)
- Преобразование типов данных
- Feature engineering (дата → Year/Month/Day)
- OneHotEncoding категориальных признаков
- LabelEncoding target
- StandardScaler для линейных моделей

---

## 🤖 Модели

- Decision Tree
- Random Forest
- XGBoost
- Logistic Regression
- SVC

Использован GridSearchCV + 5-fold CV.

---

## 📈 Результаты

- XGBoost показал лучший баланс классов
- Random Forest и Logistic Regression смещены в сторону majority class
- Decision Tree переобучается
- SVC чувствителен к дисбалансу

---

## 🚀 Установка

git clone https://github.com/incubus-glitch/google_play_store_dataset.git
cd google_play_store_dataset
pip install -r requirements.txt

---

## ▶️ Запуск

jupyter notebook
открыть classifier_googleplaystore.ipynb

---

## 📦 requirements.txt

matplotlib==3.11.0
numpy==2.4.6
pandas==3.0.3
scikit-learn==1.9.0
scipy==1.17.1
seaborn==0.13.2
xgboost==3.2.0

---
