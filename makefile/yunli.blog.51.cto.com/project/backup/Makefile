.PHONY: all clean

MKDIR = mkdir
RM = rm
RMFLAGS = -rf
CC = gcc

DIR_OBJS = objs
DIR_EXES = exes
DIRS = $(DIR_OBJS) $(DIR_EXES)
EXE = complicated.exe
SRCS = $(wildcard *.c)
OBJS = $(SRCS:.c=.o)
OBJS := $(addprefix $(DIR_OBJS)/, $(OBJS))

all:$(DIRS) $(EXE)

$(DIRS):
	$(MKDIR) $@

$(EXE):$(OBJS)
	$(CC) -o $@ $^

$(DIR_OBJS)/%.o: %.c
	$(CC) -o $@ -c $^


clean:
	$(RM) $(RMFLAGS) $(DIRS) $(EXE)
