# Game-LeftOneDead

 Эта игра - платформер, в котором герой должен справиться с ордой зомби разной силы, поведением и свойствами, постепенно продвигаясь по уровням.

Ниже представлены используемые патеррны проектирования.

#### ПАТТЕРН: builder

ИСПОЛЬЗОВАНИЕ: построение карты с переходом на уровни игры

ПОЧЕМУ: Карта - сложная структура с большим числом уровней, на которые можно перейти.  Также разным levels будет соответствовать различные особенности генерации объектов, форм, начальных расположений и прочего. 

#### ПАТТЕРН: abstract factory 

ИСПОЛЬЗОВАНИЕ: создание базы для произвольного Game Object

ПОДРОБНЕЕ: На следующем уровне иерархии предполагается использование prototype для создания базы юнитов и facades на последующем уровне для упрощения работы с классами юнитов (множество типов зомби, что показано на диаграмме ниже). 

ПОЧЕМУ: В нашей игре присутствует большое разветвление GameObjects, для которых необходима общая база, включающая основные свойства (например, координаты расположения) и при этом позволяет делегировать создание объекта подклассам.

#### ПАТТЕРН: prototype

ИСПОЛЬЗОВАНИЕ: создание базы юнитов 

ПОДРОБНЕЕ: На следующем уровне иерархии предполагается использование facades для упрощения работы с классами юнитов. (См диаграмму в этой же папке для наглядного представления).

ПОЧЕМУ: Все юниты имеют большое число общих параметров и методов, поэтому мы выбрали prototype для их клонирования и сокращения лишних действий и строчек кода

#### ПАТТЕРН: abstract factory

ИСПОЛЬЗОВАНИЕ: создание кнопок

ПОДРОБНЕЕ: Нам необходимы различные кнопки с простым и удобным созданием для легкого перемещения между уровнями

ПОЧЕМУ: Все кнопки имеют небольшое число методов, которые хотя бы частично отличаются, поэтому мы выбрали prototype



Для удобства сделана иерархия классов проекта с помощью сайта draw.io, представленная ниже.![Project](https://user-images.githubusercontent.com/79907936/109654536-57d58a80-7b73-11eb-9f78-4a8350609854.jpg)

Созданная иерархия классов позволяет быстро создавать новых персонажей и элементов интерфейса.


В файле requirements.txt указаны библиотеки, которые должны быть предустановлены для корректной работы программы.

# Description for player.
You are playing as a hero who has risen against an intimidating horde of zombies, thereby your aim is to crush them while remaining alive:) The control is quite simple: you are able to move using keys Left and Right, jump within Up key and shoot your foes down with Down key. Good luck! It will certainly help you:)

There are 4 types of zombies you will have to fight to.

Usual zombie - just ont bullet needed to kill him (her, haha). 

Fast zombie - as usual, but faster and stronger

cloning zombie - little zombie. Jumps. Makes his own copy every 2-3 seconds. Keep an eye on him (them, haha) 

Boss zombie - large zombie with a lot of hp (10, haha). Produces fast zombies.

# GamePlay screenshots
![image](https://user-images.githubusercontent.com/79907936/109774789-c79a5280-7c11-11eb-9034-23eb41f1c4ab.png)
![image](https://user-images.githubusercontent.com/79907936/109775027-0a5c2a80-7c12-11eb-95ad-e87ac4f9a9af.png)
![image](https://user-images.githubusercontent.com/79907936/109775135-2d86da00-7c12-11eb-918c-6242461bc413.png)

# User interface screenshots
![image](https://user-images.githubusercontent.com/79907936/109775512-a6863180-7c12-11eb-860f-79cf084d3372.png)
![image](https://user-images.githubusercontent.com/79907936/109775567-b4d44d80-7c12-11eb-96ee-c2a9bf64fd30.png)
![image](https://user-images.githubusercontent.com/79907936/109775607-c4ec2d00-7c12-11eb-9f9e-66d8b6f2782b.png)





