# Definimos el compilador que vamos a usar
CC = gcc

# Definimos las banderas para el compilador
CFLAGS = -Wall -std=c99 -Iinclude

# Definimos los archivos fuente
SRC = src/main.c src/funciones.c

# Definimos el archivo de prueba
TEST_SRC = tests/test.c src/funciones.c

# Definimos el nombre del ejecutable
EXEC = programa
TEST_EXEC = test_programa

# El objetivo principal (por defecto) será compilar el código
all: $(EXEC)

# El objetivo para compilar el ejecutable
$(EXEC): $(SRC)
	$(CC) $(CFLAGS) $(SRC) -o $(EXEC)

# El objetivo para compilar y ejecutar las pruebas
test: $(TEST_EXEC)
	./$(TEST_EXEC)

$(TEST_EXEC): $(TEST_SRC)
	$(CC) $(CFLAGS) $(TEST_SRC) -o $(TEST_EXEC)

# Limpiar archivos compilados
clean:
	rm -f $(EXEC) $(TEST_EXEC)

# Otros objetivos
.PHONY: all clean test
