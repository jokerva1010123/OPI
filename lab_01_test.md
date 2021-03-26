Для создания страницы достаточно записать конструкцию вида `[название ссылки](имя
страницы)`.
# 1. Оформление текста
Параграф - это несколько предложений, которые "примыкают" друг к другу (т.е. между
ними не должно быть пустой строки).
Это все еще первый параграф, хотя это предложение расположено на новой строке.
Это уже второй параграф. Между параграфами - пустая строка.
Вот таким способом *можно* **менять** ~~стиль~~ шрифта.
# 2. Оформление кода на каком-нибудь языке
```c
int test(int a)
{
printf("%d\n", a);
}
```
```
Здесь внутри *форматирование* **wiki** не работает.
```
# 3. Ссылки на разные ресурсы.
Чтобы все заработало указанные объекты должны уже существовать в вашем репозитории
или GitLab.
#1 - ссылка на issue
!1 - ссылка на merge request
XYZ - ссылка на номер ревизии (XYZ нужно поменять но номер ревизии из вашего
репозитория)
[файл](.gitignore)
URL-адрес можно вставить просто https://www.google.com, а можно сделать
[красиво](https://www.google.com)
# 4. Оформление списков и таблиц
1. Элемент списка 1
2. Элемент списка 2
* подсписок 1
* подсписок 2 (размер вложенности имеет значение как в python)
2. Элемент списка 3 (в начале не ошибка, а особенность)
4. Элемент списка 4

|Столбец 1|Столбец 2|
|---------|---------|
|1 |2 |

# 5. Что нужно изучить самостоятельно

### 1. Как добавлять рисунки.

Добавить рисунок в Wiki можно 2способами:

1. В правом нижнем углу воспользоваться кнопкой "Attach a file"
2. Сделать ссылку вручную: поставить восклицательный знак, в квадратных скобках подпись к изображению, в круглых - ссылку на изображение (ссылку можно указывать на разные картинки, в интернете, на жестком диске)

```![подпись](ссылка)```

Пример:
![sea](https://www.nastol.com.ua/download.php?img=201508/1440x900/nastol.com.ua-144315.jpg)
### 2. Как сделать оглавление.

```
# Contest
1. [First paragraph](#first)
2. [Second paragraph](#second)
    1. [Second First](#SF)
3. [Etc](#etc)

## First paragraph<a name="first"></a>
Some infirmation
## Second pararaph<a name="second"></a>
Some information
### Second First<a name="SF"></a>
Some information
## Etc <a name="etc"></a>
Some information
```
Что будет видно:

# Contest
1. [First paragraph](#first)
2. [Second paragraph](#second)
    1. [Second First](#SF)
3. [Etc](#etc)

## First paragraph<a name="first"></a>
Some infirmation
## Second pararaph<a name="second"></a>
Some information
### Second First<a name="SF"></a>
Some information
## Etc <a name="etc"></a>
Some information


### 3. Как добавить ссылки для перехода между страницами wiki.

```[Link to Documtation](documentation)```
В квадратных скобках имя ссылки, в круглых - фрагмент будет ссылаться на *documentation* страницу в корне вашей вики.

Ссылка на отчет по "Лабораторная работа 1": 
[lab_01](lab_01)

### 4. Как писать комментарии.

```
[comment]: <> (Comment)

[//]: # (Comment)
```

[comment]: <> (Comment)

[//]: # (Comment)

### 5. Стили оформления таблиц.

1. Первая строка содержит заголовки, разделенные «pipe» (|).

2. Вторая строка отделяет заголовки от ячеек и должна содержать три или более тире.

3. Третья и все последующие строки содержат значения ячеек.
   
   3.1 Не могут быть ячейки, разделенные на множество строк в Markdown, они должны храниться в одной строке, но они могут быть очень длинными. 
   
   3.2 Размеры ячеек могут не совпадать. Они гибкие, но должны быть разделены трубами (|).
   
   3.3 Ячейки могут быть пустыми

```| header 1 | header 2 | header 3 |
| ---      |  ------  |---------:|
| cell 1   | cell 2   | cell 3   |
| cell 4 | cell 5 is longer | cell 6 is much longer than the others, but that's ok. It will eventually wrap the text when the cell is too large for the display size. |
| cell 7   |          | cell   9 |
```
Что будет видно:

| header 1 | header 2 | header 3 |
| ---      |  ------  |---------:|
| cell 1   | cell 2   | cell 3   |
| cell 4 | cell 5 is longer | cell 6 is much longer than the others, but that's ok. It will eventually wrap the text when the cell is too large for the display size. |
| cell 7   |          | cell   9 |