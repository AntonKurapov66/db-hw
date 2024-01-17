# Домашнее задание к занятию "Базы данных, их типы" - `Курапов Антон`

### Задание 1 СУБД
Кейс
Крупная строительная компания, которая также занимается проектированием и девелопментом, решила создать правильную архитектуру для работы с данными. Ниже представлены задачи, которые необходимо решить для каждой предметной области.
Какие типы СУБД, на ваш взгляд, лучше всего подойдут для решения этих задач и почему?

* 1.1. Бюджетирование проектов с дальнейшим формированием финансовых аналитических отчётов и прогнозирования рисков. СУБД должна гарантировать целостность и чёткую структуру данных.
* 1.2. Под каждый девелоперский проект создаётся отдельный лендинг, и все данные по лидам стекаются в CRM к маркетологам и менеджерам по продажам. Какой тип СУБД лучше использовать для лендингов и для CRM? СУБД должны быть гибкими и быстрыми.
* 1.3. Отдел контроля качества решил создать базу по корпоративным нормам и правилам, обучающему материалу и так далее, сформированную согласно структуре компании. СУБД должна иметь простую и понятную структуру.
* 1.4. Департамент логистики нуждается в решении задач по быстрому формированию маршрутов доставки материалов по объектам и распределению курьеров по маршрутам с доставкой документов. СУБД должна уметь быстро работать со связями.
### Решение 1
* Задание 1.1
	*  Думаю что здесь подойдет любая реляционная СУБД: MySQL, Postgres и тд.
* Задание 1.2
	*  Для лендинга можно использовать MongoDB, так как она будет обеспечивать гибкость. 
	*  Для CRM-систем, где ежедневно обрабатывается большой объем данных и очень большое количество транзакций я бы использовал Postgres,MySQL.	
* Задание 1.3
	*  Для данных задач я бы выбрал РСУБД. Так как они имеют понятную структуру и более понятны в использовании
* Задание 1.4
	*  В данном случае лучше использовать Сетевые БД , будет обеспечивать несколько связей для одного узла. Пример : Neo4j

### Задание 2. Транзакции
2.1. Пользователь пополняет баланс счёта телефона, распишите пошагово, какие действия должны произойти для того, чтобы транзакция завершилась успешно. Ориентируйтесь на шесть действий.
2.1.* Какие действия должны произойти, если пополнение счёта телефона происходило бы через автоплатёж?
### Решение 2
* Задание 2.1
	*  1.Указание суммы пополнения
	*  2.Ввод реквизитов банк.карты
	*  3.Проверка баланса карты на наличие суммы пополнения 
	*  4.Снятие денежных средств(суммы пополнения) с карты 
	*  5.Пополнение расч.счета сотовой компании
	*  6.Пополнение баланса телефона
* Задание 2.1*
	-будем учитывать что автоплатеж уже подключен-   
	*  1.Проверка баланса карты на наличие суммы пополнения 
	*  2.Снятие денежных средств(суммы пополнения) с карты 
	*  3.Пополнение расч.счета сотовой компании
	*  4.Пополнение баланса телефона

### Задание 3. SQL vs NoSQL
3.1. Напишите пять преимуществ SQL-систем по отношению к NoSQL.
### Решение 3
* Задание 3.1
	*  1.Базы данных SQL более надежны. Обеспечивает обработку больших объемов данных и транзакций без потери или повреждения базы данных.
	*  2.SQL предлагает широкую совместимость с другими системами. Работает со всеми ОС. Почти во всех языках программирования есть библиотеки для работы с SQL.
	*  3.Структурированный язык запросов который можно использовать для всех РСУБД. 
	*  4.SQL более расспространено и имеет более широкую поддержку и большее сообщество.
	*  5.Более удобный для погружения, язык запросов более ориентирован на пользователей.

### Задание 4. Кластеры
Необходимо производить большое количество вычислений при работе с огромным количеством данных, под эту задачу выделено 1000 машин.
На основе какого критерия будете выбирать тип СУБД и какая модель распределённых вычислений здесь справится лучше всего и почему?

### Решение 4

Думаю в качестве СУБД подойдет Apache Cassandra-распределённая NoSQL база данных, спроектированная для обработки больших объемов данных с высоким уровнем доступности и горизонтального масштабирования. А в качестве модели распределения вычислений использовал пиринговую архитектуру. В связке с Cassandra такая структура позволит быстро выполнять вычисления. 

