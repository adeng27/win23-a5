
# objects = main.o addition.o division.o subtraction.o multiplication.o

# calculator: $(objects)
#     cc -o calculator $(objects)


# $(objects): %.o:%.c
#     cc -c $< -o $@

# clean:
#     rm -f calculator $(objects)

output: main.o addition.o division.o subtraction.o multiplication.o
	cc main.o addition.o division.o subtraction.o multiplication.o -o calculator

main.o: main.c
	cc  -c main.c

addition.o: addition.c
	cc  -c addition.c operations.h

subtraction.o: subtraction.c
	cc  -c subtraction.c operations.h

multiplication.o: multiplication.c
	cc  -c multiplication.c operations.h

division.o: division.c
	cc  -c division.c operations.h

operations.o: division.c subtraction.c addition.c multiplication.c
	cc -c division.c subtraction.c addition.c multiplication.c operations.h

clean:
	rm *.o "operations.h.gch" calculator