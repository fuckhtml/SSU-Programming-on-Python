![Сгу_Logo](https://user-images.githubusercontent.com/20648009/70866700-e6191d00-1f7d-11ea-8bc7-975041b73553.png)

###### Саратовской государственный университет им. Чернышевского
###### 4 курс | 2019 — 2020


# Программирование на Python.  Теоретическая часть

В данном документе представлен теоретический материал по курсу программирования на Python за четвертый курс в Саратовском Государственном университете.

Я дополнил его для общей целостности, чтобы он мог служить мне шпаргалкой при срочной необходимости в будущем.

**Преподаватель по теоретической и практической частям:** [Крусс Юлия Сергеевна](https://www.sgu.ru/person/kruss-yuliya-sergeevna)

## Содержание 

## Материал

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

В Pandas данные представлены в виде таблиц. 

#### Установка, подключение и использование модуля

Для скачивания пакета необходимо использовать следующую команду: 

```
pip install pandas
```

Чтобы использовать данный модуль в своем проекте, его нужно подключить. Сделать это можно несколькими способами:

```
import pandas as pd
```

#### DataFrame

DataFrame, основной тип данных данного модуля, можно представить в виде двумерной матрицы, где строки и столбцы имеют произвольные имена.

