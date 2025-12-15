# Define the target executable name
TARGET = main

# The default 'all' target builds the main program
all: $(TARGET)

# Rule to build the executable from the source file
$(TARGET): $(TARGET).c
	gcc -o $(TARGET) $(TARGET).c -Wall -g

# Phony target to clean up generated files
.PHONY: clean
clean:
	rm -f $(TARGET)