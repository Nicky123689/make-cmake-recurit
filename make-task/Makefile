CC = gcc
CFLAGS = -Wall -Wextra -Iinclude

calculator: main.o calculator.o logger.o
	$(CC) $(CFLAGS) -o $@ $^

main.o: src/main.c include/calculator.h include/logger.h
	$(CC) $(CFLAGS) -c $< -o $@

calculator.o: src/calculator.c include/calculator.h
	$(CC) $(CFLAGS) -c $< -o $@

logger.o: src/logger.c include/logger.h
	$(CC) $(CFLAGS) -c $< -o $@

.PHONY: clean
clean:
	rm -f calculator *.o
