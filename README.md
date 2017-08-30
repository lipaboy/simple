# simple
======

Plan:
  
17) С++
	- Изучить, что попадает под any_range. Как реализовать контейнер, чтобы на него можно было бы указывать by any_range?
	- Пример BitContainer
  
5) Graphics Engine
  - Read about shaders
  - Read about lightings
  
7) Криптография. Криптостойкость генератора псевдослучайных чисел. 

16) LipaboyLibrary

1) Teaching
  - Diogen, "Ваш репетитор", Maximus or nothing
  
4) Dancing. Swing, Lindy-pop
  - Youtube lessons
  
6) History of Assassins

8) Перевод английский статей. 
	- On the Tension between Object-Orientied and Generic programming. Traslate this one.

9) Эллиптические кривые для криптографии

2) English or Spanish
  - Decide which one you'd like to learn and start. For example day through the day.

10) Errors and Problems it IT book
	- may be share with Arthur and Alexey (but you need to think about editing rules)
	- Правила для редактирования книги:
		- a) Вы можете добавлять новые статьи свободно, без ограничений.
		- б) Исправлять грамматические ошибки вашиг коллег также свободно.
		- в) Если вы считаете, что в статье вашего коллеги следует что-то изменить (кроме предыдущего пункта), напишите комментарий, но ни в коем случае ничего не исправляйте, так как можете вызвать недовольство автора данной статьи.
		- г) Если вы не дописали или недоредактировали свою статью, оставьте ЗАМЕТНУЮ надпись об этом (к пример "to be edited", "to be continued").
		- last) Приятного написания книги:)
	- Поискать аналоги в интернете
	
	Примеры:
	- // enable ADL (not necessary in our case, but good practice)
        - using std::swap;
	
13) Конквистадор как викторина. Плюс в том, что не нужно заморачиваться над сложностью ворпосов.

14) Рекомендации по музыке, фильмам и др. Плагины для браузеров.
14.2) Поиск друзей в радиусе. Важно, что приложение должно сообщать о геоданных друзей только тех, кто в радиусе. Иначе, получится слежка.

15) Задача про морячков. Применить метод от простого к сложному: уменьшать количество перемещаемых коробок. Начать с того, что капитан может переставить половину коробок. И так далее.
  
Advice:

a) Refresh your crypto algorithms
	- a.1) The open keys storage in docx
	- a.2) converse file from docx to txt (because it is faster)
	- a.3) add file on github (because yandex disk is slow)
	
b) Совет для любого серьёзного дела: 
	- b.1) Установи сроки (что тебе уже следует сделать к ним, или что узнать, в чём разобраться)
	- b.2) Старайся сильно не погружать в детали (либо опять же ставь сроки, сколько времени тратить на детали)
  
n) Не распыляйся


Not enough Finished:

1) Move semantics
	- Friend-functions? Not necessary. For yourself, if you want.
	- You don't need to use std::move into return.
	- But do you need to use it move-constructor?:
	- MyClass(vector<int> &&vec) { this->vec = std::move(vec); }
	- Big Four and Half (Copy-constructor, Destructor, Operator=, Move-constructor and Friend Swap)
	- No std::move anymore. Evolute to code:
	- MyClass(vector<int> &&vec) : MyClass() { swap(this->vec, vec); }	//no std:: !!!
	
	dumb_array& operator=(dumb_array other); // (1)

	Now, if other is being initialized with an rvalue, it will be move-constructed. Perfect. In the same way C++03 let us re-use our copy-constructor functionality by taking the argument by-value, C++11 will automatically pick the move-constructor when appropriate as well. (And, of course, as mentioned in previously linked article, the copying/moving of the value may simply be elided altogether.)
	
	- But it's not enough of std::move. Read article to clear: https://stackoverflow.com/questions/3106110/what-are-move-semantics/11540204#11540204

