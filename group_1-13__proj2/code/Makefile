all: lexer parser
	g++ -Wno-write-strings *.c -o apes

lexer: lexer.l parser
	flex lexer.l
parser: parser.y
	bison -d parser.y

clean:
	-rm -f parser.tab.h
	-rm -f parser.tab.c
	-rm -f lex.yy.c
	-rm -f apes
