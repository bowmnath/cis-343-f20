name = contact

all: runner
parser: ${name}.tab.c
scanner: lex.yy.c
runner: a.out


${name}.tab.c ${name}.tab.h: ${name}.y
	bison -d ${name}.y

lex.yy.c: ${name}.tab.h ${name}.lex
	flex ${name}.lex

a.out: ${name}.tab.c lex.yy.c
	clang ${name}.tab.c lex.yy.c

test:
	./a.out < test.${name}

clean:
	rm -f a.out *.tab.h *.tab.c *.yy.c *.o
