# Предсказание оттока клиентов телеком-оператора

В условиях высокой конкуренции удержание клиента становится критически важным для телекоммуникационных компаний. Цель данного проекта — построить модель машинного обучения, способную предсказывать вероятность ухода клиента, чтобы компания могла заранее предложить индивидуальные условия для его удержания.

## Описание проекта

Проведён анализ клиентской базы оператора связи "ТелеДом" с целью разработки предиктивной модели оттока на основе персональных характеристик абонентов, подключённых услуг и способов оплаты.

## Данные

Использовались четыре набора данных:
- `contract_new.csv` — информация о договоре (тип оплаты, ежемесячные и общие траты и пр.);
- `personal_new.csv` — персональные данные клиентов (пол, пенсионный статус, наличие партнёра и иждивенцев);
- `internet_new.csv` — информация об интернет-услугах (тип подключения, наличие антивируса, облачного хранилища, ТВ и пр.);
- `phone_new.csv` — данные о телефонной связи (наличие нескольких линий).

Все датасеты объединены по ключу `customerID`.

## Методы и критерии оценки

- Целевая метрика: ROC-AUC, с минимальным порогом качества 0.85;
- Учтён дисбаланс классов;
- Разделение выборки: `test_size=0.25`, `random_state=210425`;
- Проведено масштабирование, кодирование признаков, генерация новых признаков;
- Подбор гиперпараметров проведён хотя бы для одной из моделей.

## Результат

Построена модель, определяющая склонность клиента к оттоку на основе поведения и характеристик. Полученные результаты могут быть использованы для построения системы раннего реагирования и персонализированных предложений.

