# Для работы с файлами данного формата необходимо
# установить утилиту make. На Windows это можно
# сделать при помощи пакетного менеджера Chocolatey:
# https://chocolatey.org/install

# После установки утилиты choco для установки
# утилиты make достаточно выполнить следующую
# команду: choco install make

# Инструкция для выключения отладочных сообщений.
# Название команды. Использование: make pract1
# Вызов компилятора GCC. Установка на Windows:
# https://osdn.net/projects/mingw/

project:
	gcc -std=c99 -Wall -Wpedantic -o dist/project.exe project.c
	./dist/project.exe
install emsdk:
	cd .. && git clone https://github.com/emscripten-core/emsdk.git
	cd ../emsdk 
		&& emsdk install latest && emsdk activate latest 
		&& emsdk_env.bat 
		&& emcc ../kis-project/project.c -o project.html
	npm i http-server -g
runserver:
	cd ../emsdk && http-server