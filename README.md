# Проектирование классов с использованием механизмов наследования, перегрузки операций ввода/вывода и присваивания в языке С++ для обработки файловых данных
<h3>Курсовой проект по дисциплине «Методы современного программирования»</h3>


> [ -> Пояснительная записка (описание разработанных функций, тестирование программы, код программы)](https://github.com/ktsmsnv/Methods-of-modern-programming/blob/3843cb8e3520e6c0161f0bb175e0824bb51ec36c/%D0%A1%D0%9C%D0%9F%20%D0%9A%D0%9F%20%D0%A1%D0%B0%D0%BC%D1%81%D0%BE%D0%BD%D0%BE%D0%B2%D0%B0%20%D0%95.%D0%9E.%20%D0%98%D0%92%D0%A2-321%2028%20%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82.docx)
>
> [ -> Код программы](https://github.com/ktsmsnv/Methods-of-modern-programming/blob/3843cb8e3520e6c0161f0bb175e0824bb51ec36c/%D0%A1%D0%9C%D0%9F%20%D0%9A%D0%9F.cpp)
> 
> Цель работы: в ходе решения поставленных задач ознакомиться и закрепить основные понятия программирования на языке высокого уровня С++, освоить навыки разработки классов на основе механизма наследования для различных видов обработки данных с использованием перегрузки операций.

> Задание: Спроектировать структуру PERSON, содержащую поля: фамилия и инициалы, район, адрес, телефон. Спроектировать структуру ABONENT, содержащую поле типа PERSON и дополнительно поля: номер договора, дата заключения, абонентская плата помесячно.

### Файл содержит информацию об абонентах кабельного телевидения. Требуется спроектировать класс, позволяющий обрабатывать эти данные. В классе должно быть предусмотрено, как минимум,  выполнение следующих видов обработки:

1.	Загрузка из файла;
2.	Сохранение результатов обработки в файлах;
3.	Добавление записи;
4.	Удаление записи;
5.	Вывод на экран дисплея данных и результатов обработки;
6.	Алфавитная сортировка по Ф.И.О.;
7.	Сортировка по дате заключения договора;
8.	Числовая сортировка по номеру договора;
9.	Перечень дат заключения с указанием количества договоров (результат отсортирован по дате заключения);
10.	Перечень районов с указанием количества абонентов (результат отсортирован по району);
11.	Поиск по абонентской плате (результат отсортирован по Ф.И.О.);
12.	Перечень абонентских плат с указанием числа абонентов с такой платой (результат отсортирован по численности);
13.	Поиск по адресу (результат отсортирован по дате заключения);
14.	Поиск по адресу (результат отсортирован по номеру договора);
15.	Поиск по Ф.И.О. информации об абоненте кабельного телевидения.

### Описание разработанных функций
<table>
	<tbody>
		<tr>
			<td width="220">
				<p>Название функции</p>
			</td>
			<td width="206">
				<p>Параметры функции</p>
			</td>
			<td width="211">
				<p>Назначение функции</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>main</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Главная подпрограмма, содержащая доступ к меню</p>
			</td>
		</tr>
		<tr>
			<td colspan="3" width="637">
				<p>&nbsp;Класс masA</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>masA</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Конструктор, задающий начальное значение</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>masA</p>
			</td>
			<td width="206">
				<p>masA&amp; z</p>
			</td>
			<td width="211">
				<p>Конструктор копирования</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>~masA</p>
			</td>
			<td width="206">
				<p>&nbsp;</p>
			</td>
			<td width="211">
				<p>Деструктор</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>masA &amp; operator=</p>
			</td>
			<td width="206">
				<p>(masA&amp; z)</p>
			</td>
			<td width="211">
				<p>Перегруженная операция присваивания</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>friend ostream operator &lt;&lt;</p>
			</td>
			<td width="206">
				<p>(ostream &amp;out, masA&amp; z)</p>
			</td>
			<td width="211">
				<p>Перегруженная операция вывода на экран</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>friend ofstream operator &lt;&lt;</p>
			</td>
			<td width="206">
				<p>(ofstream &amp;out, masA&amp; z)</p>
			</td>
			<td width="211">
				<p>Перегруженная операция вывода в файл</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>friend ifstream operator &gt;&gt;</p>
			</td>
			<td width="206">
				<p>(ifstream &amp;in, masA&amp; z)</p>
			</td>
			<td width="211">
				<p>Перегруженная операция ввода из файла</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>addAbonent</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Добавление записи</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>deleteAbonent</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Удаление записи</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>sortName</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Сортировка по Ф.И.О.</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>sortDat</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Сортировка по дате заключения договора</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>sortNumber</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Сортировка по номеру договора</p>
			</td>
		</tr>
		<tr>
			<td colspan="3" width="637">
				<p>Класс masB</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>masB</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Конструктор, задающий начальное значение</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>masB</p>
			</td>
			<td width="206">
				<p>(masB&amp; z)</p>
			</td>
			<td width="211">
				<p>Конструктор копирования</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>~ masB</p>
			</td>
			<td width="206">
				<p>&nbsp;</p>
			</td>
			<td width="211">
				<p>Деструктор</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>masB&amp; operator =</p>
			</td>
			<td width="206">
				<p>(masB&amp; z)</p>
			</td>
			<td width="211">
				<p>Перегруженная операция присваивания</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>friend ostream operator &lt;&lt;</p>
			</td>
			<td width="206">
				<p>(ostream &amp;out, masB&amp; z)</p>
			</td>
			<td width="211">
				<p>Перегруженная операция вывода на экран</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>friend ofstream operator &lt;&lt;</p>
			</td>
			<td width="206">
				<p>(ofstream &amp;out, masB&amp; z)</p>
			</td>
			<td width="211">
				<p>Перегруженная операция вывода в файл</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>makePerechRegions</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Создание перечня районов</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>makePerechDates</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Создание перечня дат заключения договоров</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>makePerechPlata</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Создание перечня абонентских плат</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>sortRegions</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Сортировка перечня районов по району</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>sortDates</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Сортировка перечня дат заключения по дате заключения</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>sortCount</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Сортировка перечня абонентских плат по численности</p>
			</td>
		</tr>
		<tr>
			<td colspan="3" width="637">
				<p>Класс masC</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>masC</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Конструктор, задающий начальное значение</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>masC</p>
			</td>
			<td width="206">
				<p>(masC&amp; z)</p>
			</td>
			<td width="211">
				<p>Конструктор копирования</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>~ masC</p>
			</td>
			<td width="206">
				<p>&nbsp;</p>
			</td>
			<td width="211">
				<p>Деструктор</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>masC&amp; operator =</p>
			</td>
			<td width="206">
				<p>(masC&amp; z)</p>
			</td>
			<td width="211">
				<p>Перегруженная операция присваивания</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>friend ostream operator &lt;&lt;</p>
			</td>
			<td width="206">
				<p>(ostream &amp;out, masC&amp; z)</p>
			</td>
			<td width="211">
				<p>Перегруженная операция вывода на экран</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>friend ofstream operator &lt;&lt;</p>
			</td>
			<td width="206">
				<p>(ofstream &amp;out, masC&amp; z)</p>
			</td>
			<td width="211">
				<p>Перегруженная операция вывода в файл</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>findPlata</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Поиск по абонентской плате</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>findAddress</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Поиск по адресу</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>findbyFIO</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Поиск по Ф.И.О.</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>sortPlataFIO</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Сортировка массива поиска по абонентской плате по Ф.И.О.</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>sortAddressDate</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Сортировка массива поиска по адресу по дате заключения договора</p>
			</td>
		</tr>
		<tr>
			<td width="220">
				<p>sortAddressNum</p>
			</td>
			<td width="206">
				<p>-</p>
			</td>
			<td width="211">
				<p>Сортировка массива поиска по адресу по номеру договора</p>
			</td>
		</tr>
	</tbody>
</table>
