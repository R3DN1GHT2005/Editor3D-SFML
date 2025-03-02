# Compiler and flags
CXX = g++
CXXFLAGS = -c -O2 -std=c++17 -Wall -Wextra
LDFLAGS = -lsfml-graphics -lsfml-window -lsfml-system

# Source files and object files
SOURCES = main.cpp camera.cpp clock.cpp points_math.cpp save_and_load.cpp shape.cpp ui/button.cpp ui/text_box.cpp shapes/cube.cpp shapes/pyramid.cpp shapes/sphere.cpp shapes/cone.cpp shapes/cylinder.cpp
OBJECTS = $(SOURCES:.cpp=.o)
EXECUTABLE = main

# Default target
all: $(EXECUTABLE)

# Link object files to create the executable
$(EXECUTABLE): $(OBJECTS)
	$(CXX) $(OBJECTS) -o $@ $(LDFLAGS)

# Compile source files to object files
%.o: %.cpp
	$(CXX) $(CXXFLAGS) $< -o $@

# Clean up build files
clean:
	rm -f $(OBJECTS) $(EXECUTABLE) file.txt
