﻿Исправления 1
    1) 	Checkstyle проходит, но правила я ослабил.
    2) 	Код отформатировал внутренними средствми IDEA.
    3) 	Некоторые аргументы программы должны следовать друг за другом, например -p /SomePath/file.
	    Если даже я положу их LinkedHashSet с сохранением, порядка то нужно будет итерироваться по элементам чтобы
	    найти путь файла, следующий за ключом -p или -с.
	    Можно переписать с исользованием List и выигрыш в аккуратности будет только за счет методов contains(), indexOf().
    4)	Пустые методы в тестах убрал.
    5)	все операции с потоками ввода-вывода переписал через конструкции try-with-resources.

Исправления 2
    1)  Настроил checkstyle plugin на правила по умолчанию, пришлось отключить некоторые проверки
        с помощью SupressionFilter. Отключил проверку JavaDoc, MagicNumbers в некоторых местах,
        LineLength по всему проекту.
    2)  Все классы поместил в пакет hhtask.
    3)  Из кода метода main выделил два отдельных метода, отвечающие за шифрование-дешифрование.