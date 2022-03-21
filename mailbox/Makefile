#embedded linux course

CC:=gcc
CFLAGS = -O0 -Wall
LIBS = -lpthread
INCLUDE = -I include
SRC_PATH = src/
OBJ_PATH = build/

SRC=$(wildcard *.c)
OBJS=$(SRC:.c=.o)

all: app

$(OBJ_PATH)%.o: $(SRC_PATH)%.c
	$(CC) $(CFLAGS) -c $(INCLUDE) $< -o $@

$(OBJ_PATH)app: $(OBJ_PATH)$(OBJS)
	$(CC) $^ -o $@ $(LIBS)

clean:
	rm -f *.o app

.PHONY: all clean

