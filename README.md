![Сгу_Logo](https://user-images.githubusercontent.com/20648009/70866700-e6191d00-1f7d-11ea-8bc7-975041b73553.png)

###### Саратовской государственный университет им. Чернышевского
###### 4 курс | 2019 — 2020


# Программирование на Python.  Теоретическая часть

В данном документе представлен теоретический материал по курсу программирования на Python за четвертый курс в Саратовском Государственном университете.

Я дополнил его для общей целостности, чтобы он мог служить мне шпаргалкой при срочной необходимости в будущем.

**Преподаватель по теоретической и практической частям:** [Крусс Юлия Сергеевна](https://www.sgu.ru/person/kruss-yuliya-sergeevna)

## Содержание 

## Материал

### Типы данных

#### Словари

Словарь представляет собой "массив" с данными, где есть ключ и значение, которое ему соответствует. 

Простой словарь
```
idNames = {
  '0': 'Alex',
  '1': 'Anny',
  '2': 'Terry',
}

print(idNames)
print(idNames['1'])

namesSurnames = {
  'Alexander': 'Grigoriev',
  'Nikita': 'Matushin',
  'Terry', 'Jay',
}

print(namesSurnames)
print(namesSurnames['Alexander'])

```

Словарь посложнее
```
data = {
    'id': [0, 1, 2, 3],
    'name': ['alex', 'nikita', 'terry', 'lera'],
}

print(data)
print(data['id'])
print(data['id'][0])
```

### Установка и подключение модулей

Перед тем, чтобы использовать модуль, его нужно найти, скачать, а затем подключить в свой проект.

#### Основные команды

1. **Найти необходимый модуль**

Это можно сделать на сайте [pypi.org](https://pypi.org/)

2. **Посмотреть все установленные модули**

```
pip freeze
```

3. **Закачать модуль**

```
pip install <название модуля>

Например:
pip install numpy
```

### Модуль NumPy

#### Установка

Для скачивания пакета необходимо использовать следующую команду: 
```
pip install numpy
```

#### Подключение модуля и использование функций

Чтобы использовать данный модуль в своем проекте, его нужно подключить. Сделать это можно несколькими способами:

**Первый способ.**

```
import numpy
```

Использование функций проходит через < numpy. > 

```
print( numpy.floor(5.7) )
```

**Второй способ. Самый предпочтительный**

```
import numpy as np
```

Использование функций проходит через < np. > 

```
print( np.floor(5.7) )
```
**Третий способ**

```
from numpy import *
```
Использование функций проходит через из названия без numpy и np. 

```
print( floor(5.7) )
```

### Модуль matplotlib

### Модуль Pandas

Модуль Pandas предназначен для работы с большими данными. Он построен на основе библиотеки NumPy. 

Pandas позволяет формировать, изменять, читать и анализировать данные, а также собирать их с разных источников.

#### Установка, подключение и использование модуля

Скачивание

```
pip install pandas
```

Подключение

```
import pandas as pd
```

#### DataFrame

DataFrame — основной тип данных данного модуля. Его можно представить в виде двумерной матрицы, где строки и столбцы имеют имена.

##### Создание DataFrame
1. Создадим словарь с данными
```
import pandas as pd

data = {
    'id':       [0, 1, 2, 3],
    'name':     ['Alex', 'Anny', 'Nikita', 'Lera'],
    'birthday': ['22.05.1997', '11.10.1998', '17.05.1996', '8.10.1996'] 
}

print(data)
print()

print( str(data['id'][0]) + ' ' +
       str(data['name'][0]) + ' ' +
       str(data['birthday'][0]))
       

```

Создадим объект DataFrame и посмотрим его

```
df = pd.DataFrame(data, columns = ['id', 'name', 'birthday'])
print(df)
print()
```

#### Экспорт данных DataFrame -> CSV

CSV представляет обычный текстовый файл, первой строчкой в котором идет перечисление столбцов, а ниже представлены строки данных, разделенные через запятую для столбцов.

Экспорт созданного DataFrame выполняется через следующую команду:

```
df.to_csv('mydataframe.csv')
```

#### Импорт данных из CSV -> DataFrame 

Чтобы из CSV получить DataFrame, необходимо выполнить следующую команду

```
df = pd.read_csv('titanic.csv')

print(df)
```
