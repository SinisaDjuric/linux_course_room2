#embedded linux course

CC:=gcc
CFLAGS = -O0 -Wall
LIBS = -lpthread
INCLUDE = -I include
SRC_PATH = src/
OBJ_PATH = build/

SRC=$(wildcard $(SRC_PATH)*.c)
SRC_TMP=$(notdir $(SRC))
OBJS_TMP=$(SRC_TMP:.c=.o)
OBJS=$(addprefix $(OBJ_PATH), $(OBJS_TMP))

all: app

$(OBJ_PATH)%.o: $(SRC_PATH)%.c
	$(CC) $(CFLAGS) -c $(INCLUDE) $< -o $@

$(OBJ_PATH)app: $(OBJ_PATH)$(OBJS)
	$(CC) $^ -o $@ $(LIBS)

clean:
	rm -f *.o app

.PHONY: all clean

