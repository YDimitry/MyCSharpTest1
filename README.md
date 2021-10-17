From https://docs.microsoft.com/ru-ru/dotnet/core/tutorials/library-with-visual-studio-code
~~~bash
dotnet new sln

dotnet new classlib -o MyClassLib
~~~
Команда -o или --output задает расположение для размещения созданных выходных данных.

добавить проект библиотеки в решение
~~~bash
dotnet sln add MyClassLib/MyClassLib.csproj

dotnet build

dotnet new console -o MyProgramm

dotnet sln add MyProgramm/MyProgramm.csproj
~~~
Добавление ссылки на проект
~~~bash
dotnet add MyProgramm/MyProgramm.csproj reference MyClassLib/MyClassLib.csproj
~~~
Запуск приложения
~~~bash
dotnet run --project MyProgramm/MyProgramm.csproj
~~~
