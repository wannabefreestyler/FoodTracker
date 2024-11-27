# Диаграмма вариантов использования

![Диаграмма вариантов использования](https://github.com/vladmoiseev/Vshop/blob/master/diagrams/img/useCase.png)

# Глоссарий

| Термин | Определение |
|:--|:--|
| Пользователь | Человек, использующий приложение для отслеживания своей калорийности и питания |
| Прием пищи | 	Группа продуктов или блюдо, которое пользователь добавляет в свой рацион |
| Ингредиент | Продукт, имеющий определенные калорийные и питательные характеристики |
| Закуска | Продукт или блюдо, добавляемое пользователем вне основных приемов пищи |
| Питательные значения | Набор данных, содержащий калории, белки, жиры и углеводы |

# Поток событий 

# Содержание
1 [Актёры](#actors)  
2 [Варианты использования](#use_case)  
2.1 [Добавить прием пищи](#Add_food)  
2.2 [Удалить прием пищи](#rRemove)  
2.3 [Добавить ингредиент](#Add_ingr)  
2.4 [Удалить ингредиент](#Remove_ingr)  
2.5 [Просмотреть дневной рацион](#Ratio)  
2.6 [Установить цель калорийности](#Goal)  
2.7 [Загрузить данные дня](#Load)  
2.8 [Сохранить данные дня](#Save)  

<a name="actors"/>

# 1 Актёры

| Актёр | Описание |
|:--|:--|
| Пользователь | Основной актёр, который взаимодействует с приложением для управления рационом и просмотра статистики |

<a name="use_case"/>

# 2 Варианты использования

<a name="Add_food"/>

## 2.1 Добавить прием пищи

**Описание.** Пользователь может создать новый прием пищи (например, завтрак, обед или ужин) и указать, что он ел.
**Предусловия.** Пользователь открыл экран добавления приема пищи..  
**Основной поток.**
1. Пользователь выбирает «Добавить прием пищи»;
2. Приложение отображает форму для ввода названия приема пищи;
3. Пользователь вводит название (например, «Завтрак»);
4. Приложение добавляет новый прием пищи в текущий день;
5. Вариант использования завершается.

<a name="Remove"/>

## 2.2 Удалить прием пищи

**Описание.** Пользователь может удалить ранее добавленный прием пищи.
**Предусловия.** Пользователь выбрал прием пищи для удаления.  
**Основной поток.**
1. Пользователь нажимает «Удалить прием пищи».
2. Приложение удаляет выбранный прием пищи из текущего дня.
3. Приложение обновляет информацию о дневной калорийности.
4. Вариант использования завершается.

<a name="Add_ingr"/>

## 2.3 Добавить ингредиент

**Описание.** Пользователь может добавить конкретный ингредиент с его питательными значениями в прием пищи.  
**Предусловия.** Пользователь выбрал прием пищи для добавления ингредиента.
**Основной поток.**
1. Пользователь выбирает «Добавить ингредиент».
2. Приложение отображает список ингредиентов или форму для их создания.
3. Пользователь выбирает ингредиент из списка или создает новый, указав питательные значения.
4. Приложение добавляет ингредиент в выбранный прием пищи.
5. Вариант использования завершается.

<a name="Remove_ingr"/>

## 2.4 Удалить ингредиент

**Описание.** Пользователь может удалить ранее добавленный ингредиент из приема пищи.  
**Предусловия.** Пользователь выбрал прием пищи и ингредиент для удаления.  
**Основной поток.**
1. Пользователь нажимает «Удалить ингредиент».
2. Приложение удаляет выбранный ингредиент из приема пищи.
3. Приложение обновляет калорийность приема пищи и дневного рациона.
4. Вариант использования завершается.

<a name="Ratio"/>

## 2.5 Просмотреть дневной рацион

**Описание.** Пользователь может увидеть общий отчет о потребленных калориях, белках, жирах и углеводах за день.
**Предусловия.** Пользователь находится на главном экране приложения.
**Основной поток.**
1. Пользователь выбирает «Дневной отчет».
2. Приложение отображает список приемов пищи и общее количество питательных значений за день.
3. Пользователь может просмотреть детали каждого приема пищи.
4. Вариант использования завершается.

<a name="Goal"/>

## 2.6  Установить цель калорийности

**Описание.** Пользователь может задать цель по калорийности для контроля своего рациона.  
**Предусловия.** Пользователь выбрал настройку цели калорийности.
**Основной поток.**
1. Пользователь вводит желаемое количество калорий.
2. Приложение сохраняет цель и отображает её на главном экране.
3. Приложение уведомляет пользователя при превышении цели.
4. Вариант использования завершается.


<a name="Load"/>

## 2.7 Загрузить данные дня

**Описание.** Пользователь может загрузить данные о рационе за определенный день.  
**Предусловия.** Пользователь выбрал дату из календаря.  
**Основной поток.**
1. Пользователь выбирает дату.
2. Приложение загружает данные из локального хранилища.
3. Приложение отображает приемы пищи и питательные значения за выбранный день.
4. Вариант использования завершается.

<a name="Save"/>

## 2.8 Сохранить данные дня

**Описание.** Приложение автоматически сохраняет данные о рационе за день в локальное хранилище.  
**Предусловия.** Пользователь завершил редактирование данных за день.
**Основной поток.**
1. Приложение сохраняет данные приема пищи, ингредиентов и питательных значений в файл.
2. Приложение уведомляет пользователя о сохранении (опционально).
3. Вариант использования завершается.