# Name of the project
PROJECT_NAME = hbm

# Output directory
BUILD = build

# All source code files
SRC = main.c\
src/hbm.c\

# All test source files
TEST_SRC = src/hbm.c\
test/test_hbm.c

TEST_OUTPUT = $(BUILD)/Test_$(PROJECT_NAME).out

# All include folders with header files
INC	= -Iinc

PROJECT_OUTPUT = $(BUILD)/$(PROJECT_NAME).out

# Document files
DOCUMENTATION_OUTPUT = documentation/html

# Default target built
$(PROJECT_NAME):all

# Run the target even if the matching name exists
.PHONY: run clean test  doc all

all: $(SRC) $(BUILD)
	gcc $(SRC) $(INC) -o $(final).out -lm

# Call `make run` to run the application
run:$(PROJECT_NAME)
	./$(final).out

# Document the code using Doxygen
doc:
	make -C ./documentation



# Remove all the built files, invoke by `make clean`
clean:
	rm -rf $(BUILD) $(DOCUMENTATION_OUTPUT)

# Create new build folder if not present
$(BUILD):
	mkdir build
