# Creando nuestro MakeFile para el Hello.c

#Variable donde indico las flags de "C" para el compiler. En este caso la version de C
CFLAGS = -std=c23

# Variable con el compilador a usar. En este caso "GCC"
COMPILER = gcc

# Variable con el .exe a ejecutar, la declaro del tipo simple porque sino mostrara en consola el resultado de la regla - linea 19.
EXE := hello.exe

# Con el caracter "@" evitamos mostrar en consola el comando a ejecutar, aunque ver el comando es muy util para una depuracion.
# Con el caracter ">" nosotros podemos indicar que vamos a redireccionar el resultado de compilacion a un archivo.<extension_inidicada>

# Regla para compilar y ejecutar. Resultado en un .txt 
file: $(EXE)
	@./$(EXE) > output.txt

# Regla para compilar y ejecutar. Resultado en consola
run: $(EXE)
	@./$(EXE)

# Regla compila el ejecutable, es llamada al hacer la regla run
$(EXE): hello.c
	@$(COMPILER) $(CFLAGS) hello.c -o $(EXE)

# Regla para limpiar los archivos basura de la compilacion
clean:
	rm -f $(EXE)