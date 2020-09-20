## Rodion Sverdlov
***
### Contacts
e-mail: `R_Sverdlov_2001@mail.ru`
***
### Some information about me
`My main goal is to become a JavaScript developer. My strengths are hard work, perseverance and willingness to learn new technologies. I have already created projects in C ++, which calculated the length of service of the company's employees.`
***
### My skills
`C++ Basics`
`JS Basics`
`HTML Basics`
`CSS Basics`
***
### My Code
```C++
int main()
{
	setlocale(LC_ALL, "ru");
	Information Detal;
	//место для переменных
	int number;
	int NowMonth; // текущий месяц во втором кейсе при выводе
	int CodeDetali;
	int KolichestvoDetalei;
	int Month;
	string path;
	path = "10LABA.txt";
	bool exit = false;
	while (!exit)
	{
		cout << "Выберите функцию" << endl;
		cout << "1- заполнить список или добавить информацию" << endl;
		cout << "2- вывести информацию" << endl;
		cout << "3- очистить файл" << endl;
		cout << "4- выйти из программы" << endl;
		cin >> number;
		switch (number)
		{
		case 1: // добавить или заполнить список
		{
			ofstream file;
			file.open(path, ofstream::app);

			cout << "Введите код детали ";
			cin >> CodeDetali;
			Detal.Code = CodeDetali;

			cout << "Введите колличество выпущенных деталей ";
			cin >> KolichestvoDetalei;
			Detal.Kolichestvo = KolichestvoDetalei;

			cout << "Введите номер месяца выпуска детали ";
			cin >> Month;
			Detal.MonthNumber = Month;

			cout << endl;

			file << "Код: " << Detal.Code << endl;
			file << "Колличество: " << Detal.Kolichestvo << endl;
			file << "Номер месяца: " << Detal.MonthNumber << endl;

			file.close();
			break;
		}

		case 2: // Вывести информацию о продукции, выпущенной заданным цехом за последний месяц.
		{
			ifstream Rfile;
			Rfile.open(path);
			cout << "Введите номер текущего месяца ";
			cin >> NowMonth;
			Information NewStruct; // структура вывода

			while (Rfile.peek() != EOF) // Функция peek() используется с потоками ввода и возвращает следующий символ потока или EOF, если достигнут конец файла. peek() не удаляет символ из потока.
				//  eof() возвращает 1, если был достигнут конец файла
			{
				Rfile.ignore(4); Rfile >> Detal.Code; Rfile.get();  // Функция ignore() используется с потоками ввода. Она считывает и выбрасывает символы, пока не считает num символов
				Rfile.ignore(12); Rfile >> Detal.Kolichestvo; Rfile.get();
				Rfile.ignore(13); Rfile >> Detal.MonthNumber; Rfile.get();
				Rfile.get();
				if (NowMonth == Detal.MonthNumber)
				{
					NowMonth = Detal.MonthNumber;
					NewStruct = Detal;
				}
			}
			cout << endl;
			cout << "---------------ИНФОРМАЦИЯ--------------" << endl;
			cout << "Код детали: " << NewStruct.Code << "\n";
			cout << "Количество выпущенных деталей: " << NewStruct.Kolichestvo << "\n";
			cout << "Номер месяца выпуска детали: " << NewStruct.MonthNumber << "\n";
			cout << "---------------------------------------" << endl;
			system("pause");
			cout << endl;
			Rfile.close();
			break;
		}
```
### My Education
I am studying at `BSUIR` on the specialty Information Systems and Technologies
***
### My work expirience
***
### My English
My level of English is below intermediate. I had experience communicating with a native speaker.
