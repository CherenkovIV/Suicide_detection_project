# Применение алгоритмов машинного и глубокого обучения для индентификации сообщений потенциальных суицидентов
### Описание
Данная работа была выполнена в рамках ВКР по программе "Программные средства решения задач искусственного интеллекта". 
### Исходные данные
Датасет на Kaggle: https://www.kaggle.com/datasets/eldamar1717/depression-suicide-twits-ru

Данные представляют собой переведенные на русский язык сообщения с
Reddit, собранные с помощью Pushshift API. Сообщения относятся к трем
разделам:
- SuicideWatch - в данной теме люди рассказывают о своѐм состоянии,
о причинах, почему они хотят покончить с собой;
- depression - аналогично обсуждается депрессия. Несмотря на тесную
связь между депрессией и самоубийством, диагноз депрессии тем не
указывает на то, что человек обязательно покончит с собой [5]. Но с
целью увеличения количества образцов сообщений потенциальных
суицидентов решено считать сообщения из данного раздела также
частью сообщений потенциальных самоубийц;
- teenagers - сообщения на разные темы, второй класс в исходных
данных.

### Аннотация
Данная работа посвящена алгоритмам машинного и глубокого обучения и их применению для классификации текстовых данных. В качестве данных используются сообщения, часть из которых указывает на намерение пользователя, оставившего их, совершить самоубийство. Описываются
различные методы анализа и классификации текстовых сообщений с использованием программных средств. В работе приводятся результаты исследования исходных данных и практических применений различныхпрограммных средств (таких как нейронные сети различных архитектур или
более простые алгоритмы), а также оценивается их эффективность

### Введение
На сегодняшний день, в следствие цифровизации общества, средства искусственного интеллекта могут применяться в совершенно различных областях, опирающихся на большие данные. Даже традиционно гуманитарные дисциплины, такие как социология или психология, все чаще прибегают к
использованию алгоритмов машинного и глубокого обучения для решения
своих задач.
Одной из проблем, с которой эти две науки имеют дело, и которая особенно актуальна для России — это самоубийства. По состоянию на 2019 год, Россия входит в число лидеров по смертности от самоубийств (более 20 случаев на 100000 населения). При этом психиатрия признает, что нет ни одного клинического состояния, при котором человек был бы застрахован от суицидальных настроений.
С учетом этого и малой осведомленности людей о данной проблеме, становится актуальной и клинически востребованной идея привлечения инструментов машинного обучения для выявления скрытых
закономерностей, указывающих на намерение покончить с собой.
Во многих попытках самоубийства просматривается один паттерн. Перед тем как идти на смертельный риск, человек предупреждает о своѐм намерении, некоторого другого человека («спасителя»), от которого он желает получить любовь и внимание, в котором нуждается. С появлением интернета, у суицидентов появилась возможность обратиться в поисках «спасителя» не только к родственнику или близкому другу, но и ко всему миру, посредством социальных сетей и форумов. Такие сообщения могут отслеживаться различными алгоритмами для предоставления людям квалифицированной
помощи.
В данной работе мы рассмотрим некоторые программные средства искусственного интеллекта, решающие задачу классификации и сравним их точность на реальных сообщениях потенциальных суицидентов.

### Библиотеки

Необходимые библиотеки устанавливаются с помощью pip.
Пример для numpy:
```sh
pip install numpy
```
Для семантического анализа необходимо дополнительно загрузить модель deeppavlov

```sh
python -m deeppavlov install rusentiment_bert
```



