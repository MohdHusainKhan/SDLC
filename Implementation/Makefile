PROJECT_NAME = SDLC

# Output directory
BUILD = build

# All source code files
SRC = src/ampacity.c\
src/Circular_Convo_FFT.c\
src/derating.c\
src/display.c\
src/division.c\
src/Equivalent_Impedance.c\
src/function.c\
src/maincode.c\
src/parallel.c\
src/Power_Factor.c\
src/series.c\
src/Source_Transformation.c\
src/Star_Delta_Conversion.c\
src/voltagedrop.c\


# All include folders with header files
INC	= -Iinc\
-Iunity\

TEST_OUTPUT = $(BUILD)/Test_$(PROJECT_NAME).out

# All include folders with header files
INC	= inc/cable.h\
inc/Circular_Convo_FFT.h\
inc/color.h\
inc/division.h\
inc/fun.h\
inc/parallel.h\
inc/Series_RLC.h\
inc/series.h\
inc/Source_Transformation.h\
inc/Star_Delta_Conversion.h\

#Library Inlcudes
#INCLUDE_LIBS = 
INCLUDE_LIBS = -lcunit

# Project Output name
PROJECT_OUTPUT= $(BUILD)/$(PROJECT_NAME).out

# Document files
DOCUMENTATION_OUTPUT = documentation/html

# Default target built
$(PROJECT_NAME):all

# Run the target even if the matching name exists
.PHONY: run clean test doc all

all: $(SRC) $(BUILD)
	gcc main.c $(SRC) $(INC) -o $(PROJECT_OUTPUT) -lm

# Call `make run` to run the application
run:$(PROJECT_NAME)
	./$(PROJECT_OUTPUT).out

# Document the code using Doxygen
doc:
	make -C ./documentation

# Build and run the unit tests
test:$(BUILD)
	gcc $(TEST_SRC) -o $(TEST_OUTPUT) $(INCLUDE_LIBS)
	./$(TEST_OUTPUT)




# Remove all the built files, invoke by `make clean`
clean:
	rm -rf $(BUILD) $(DOCUMENTATION_OUTPUT)

# Create new build folder if not present
$(BUILD):
	mkdir build
