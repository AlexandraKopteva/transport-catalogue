# cpp-transport-catalogue
Финальный проект: Транспортный справочник (Router)
Система хранит транспортные маршруты и обрабатывает запросы к ним:

Входные и выходные данные в JSON-формате.
Кроме JSON-файла на выходе может быть предоставлена карта маршрута(ов) в формате SVG.
Система предоставляет возможность поиска кратчайшего пути основанного на графах.
Возможность сериализации настроек и базы данных справочника через Google Protobuf.
Объекты при конструировании поддерживают цепочки вызовов (chaining), что позволяет превращать ошибки JSON формата в ошибки компиляции.
Используемые технологии, идиомы, элементы STL и стандарты языка
OOP
STL smart pointers
STL map/set unourdered
STL variang
STL optional
SVG inside XML output
CRTP (Curiously Recurring Template Pattern)
Chaining method
Fasade design pattern
Google Protocol Buffers
Directed Weighted Graph data structure
Static libraries (.LIB, .A)
CMake
C++17, С++20
Запуск программы
Приложение работает в 2-х режимах. Режим создания (наполнения) базы данных и режим запросов к ней.

Для наполнения базы данных можно создать файл в JSON-формате и перенаправить его в стандартный входной поток приложения. По умолчания данные поступают через stdin.
После наполнения базы данных мы можем создавать и обрабатывать запросы к ней. Входные данные поступают через стандартный потох stdout. Для удобства мы можем перенаправить данные в файл, чтобы иметь возможность работать с ним.
Формат входных данных
Входные данные принимаются из stdin в JSON формате.
