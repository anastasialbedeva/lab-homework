# **Лабораторная работа (команда grep)**
### **Разминка (ее в отчет включать не нужно!)**
Для начала создадим небольшой текстовый файл, содержащий случайный текст, и научимся работать с текстовыми данными с помощью команды `grep`.

**1.Создайте файл text.txt с содержимым:**
```
cat > text.txt << EOF
The quick brown fox jumps over the lazy dog.
A journey of a thousand miles begins with a single step.
To be or not to be, that is the question.
All that glitters is not gold.
Fortune favors the brave.
EOF
```
**2.Попробуйте найти строки, содержащие слово "the":**
```
$grep "the" text.txt
```
**3.Используйте опцию -i для игнорирования регистра:**
```
$grep -i "the" text.txt
```
**4.Найдите строки, содержащие слово "is" как отдельное слово:**
```
$grep -w "is" text.txt
```
**5.Подсчитайте количество строк, где встречается слово "be":**
```
$grep -c "be" text.txt
```
Убедитесь, что вы освоили эти команды перед переходом к основной задаче.



## **Задание лабораторной работы (включается в отчет!)**
Напишите скрипт, который:

1. Принимает на вход текстовый файл и ключевое слово.
2. Выполняет следующие действия:
   
    -Выводит строки, содержащие ключевое слово.
   
    -Подсчитывает количество таких строк.
   
    -Выводит уникальные слова, которые встречаются в тех же строках, но не являются ключевым словом.
   
    -Сохраняет строки с ключевым словом в файл `output.txt`.

**Пример входных данных:**

Файл: `text.txt`

Ключевое слово: `the`

**Пример выполнения:**
```
./text_analyzer.sh text.txt the
```

**Пример выходных данных в консоли:**
```
Строки с ключевым словом:
The quick brown fox jumps over the lazy dog.
All that glitters is not gold.

Количество строк: 2
Уникальные слова (с частотой встречаемости):
1 lazy
1 dog
1 quick
1 brown
1 fox
1 jumps
1 over
1 all
1 glitters
1 not
1 gold
```

**Пример содержимого `output.txt`:**
```
The quick brown fox jumps over the lazy dog.
All that glitters is not gold.
```


### **Как успешно сдать работу?**

**1.Создайте публичный репозиторий.**
  
  Используйте "Use this template" -> "Create a new repository".
  
**2. Оформите отчет в формате .md:**

 - Описание задачи
 - Пошаговое объяснение
 - Скриншоты выполнения скрипта
 
  **3. Добавьте файл  `text.txt` и результат работы `output.txt` в репозиторий.**



## **Ресурсы**
[Команда grep в Linux](https://selectel.ru/blog/tutorials/grep-command-in-linux/)

[Синтансис bash](https://gist.github.com/Titiaiev/dcb7298389d1276b823bbc96e29f940d)

[Источник где можно найти все)](https://google.com)







