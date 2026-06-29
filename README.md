# ACTIVIDAD_FORMATIVA2_POO
AF2_POO
# Gestión de Estudiantes en Java
Aplicación simple desarrollada para demostrar los conceptos fundamentales de Programación Orientada a Objetos (POO): clases, objetos, atributos, métodos y constructores.

##  Objetivo
Crear una aplicación que permita gestionar estudiantes mediante:
- Declaración de clases
- Instanciación de objetos
- Uso de métodos y constructores
- Pruebas desde un programa principal

##  Estructura del proyecto
POO-Gestion-Estudiantes/
│
├── src/
│   ├── Estudiante.java
│   ├── GestorEstudiantes.java
│   └── Main.java
│
├── README.md
│
└── .gitignore
src/
├── Estudiante.java
├── GestorEstudiantes.java
└── Main.java

## 🧑‍🏫 Clases principales

### **Estudiante**
Representa a un estudiante con nombre, edad y matrícula.

### **GestorEstudiantes**
Administra una lista de estudiantes y permite agregarlos y mostrarlos.

### **Main**
Ejecuta el programa y prueba los métodos.

##  Conceptos aplicados
- Programación Orientada a Objetos
- Encapsulamiento
- Constructores
- Métodos
- Listas dinámicas (ArrayList)
- Instanciación de objetos

##  Ejecución
Compilar y ejecutar desde el IDE (IntelliJ, Eclipse o NetBeans):

javac Main.java
java Main

##  Publicación
Este repositorio forma parte de la actividad académica solicitada para demostrar el uso de POO y control de versiones con GitHub.

##  Referencias
- Oracle. (2024). *Java Documentation*. https://docs.oracle.com/javase
- Eckel, B. (2006). *Thinking in Java*. Prentice Hall.

public class Estudiante {
    private String nombre;
    private int edad;
    private String matricula;

    public Estudiante(String nombre, int edad, String matricula) {
        this.nombre = nombre;
        this.edad = edad;
        this.matricula = matricula;
    }

    public void mostrarInfo() {
        System.out.println("Nombre: " + nombre);
        System.out.println("Edad: " + edad);
        System.out.println("Matrícula: " + matricula);
    }

    public String getNombre() { return nombre; }
    public int getEdad() { return edad; }
    public String getMatricula() { return matricula; }
}
import java.util.ArrayList;

public class GestorEstudiantes {
    private ArrayList<Estudiante> lista = new ArrayList<>();

    public void agregarEstudiante(Estudiante e) {
        lista.add(e);
        System.out.println("Estudiante agregado correctamente.");
    }

    public void mostrarTodos() {
        for (Estudiante e : lista) {
            e.mostrarInfo();
            System.out.println("---------------------");
        }
    }
}
public class Main {
    public static void main(String[] args) {

        Estudiante e1 = new Estudiante("Ana López", 20, "A001");
        Estudiante e2 = new Estudiante("Luis Pérez", 22, "A002");

        GestorEstudiantes gestor = new GestorEstudiantes();

        gestor.agregarEstudiante(e1);
        gestor.agregarEstudiante(e2);

        gestor.mostrarTodos();
    }
}
# Archivos de IntelliJ
.idea/
*.iml

# Archivos de compilación
out/
bin/
*.class
