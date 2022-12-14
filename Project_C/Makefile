project:
	gcc -std=c99 -Wall -Wpedantic -o dist/project.exe project.c
	./dist/project.exe
installemsdk:
	cd ../emsdk && emsdk install latest && emsdk activate latest && emsdk_env.bat 
	emcc ../Project_C/project.c -o project.html
	npm i http-server -g
runserver:
	cd ../emsdk && http-server
