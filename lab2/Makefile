SOURCES := main.cpp aco.cpp ant.cpp
BIN := main
# Objs are all the sources, with .cpp replaced by .o
OBJS := $(SOURCES:.cpp=.o)

all: $(BIN)

exam: $(BIN)
	printf "ovX4.aco\n0\n8\n10\n1\n1\n0.99\n100\n5\n" | ./$(BIN)

check: $(BIN)
	printf "runall\n" | ./$(BIN)

.cpp.o:
	$(CC) $(CFLAGS) $(INCLUDES) -c $< -o $@

$(BIN): $(OBJS)
	g++ $(CFLAGS) -o $@ $^ $(LFLAGS) $(LIBS)

.PHONY: clean

clean:
	rm -f $(BIN) $(OBJS)
