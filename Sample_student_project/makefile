biuld: KW

all: biuld clean biuld archive build doc

KW: main.o game.o othello.o 
	g++ -o KW main.o game.o othello.o 

main.o: main.cc
	g++ -c main.cc

game.o: game.cc game.h
	g++ -c game.cc

othello.o: othello.cc othello.h piece.h colors.h
	g++ -c othello.cc

clean:
	rm *.o

doc: doxygen -g *.cc *.h 

doczip: doc.tgz

doctgz: html/index.html
	tar cvzf dac.tgz html

archive:
	tar -cvf file.tar *
