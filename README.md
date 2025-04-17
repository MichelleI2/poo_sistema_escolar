# poo_sistema_escolar
//Clase persona
public class Person {
    protected String nombre;
    protected int edad;

        public Person(String nombre, int edad){
        this.nombre = nombre;
        this.edad = edad;
    }
        public void yourself(){
        System.out.println("Hola,mi nombre es" +nombre +"y tengo" +edad+ " años.");
    }
  }
public class Estudiante extends Person {
    private String matricula;
    private String carrera;

    public Estudiante(String nombre, int edad, String matricula, String carrera) {
        super(nombre, edad);
        this.matricula = matricula;
        this.carrera = carrera;
    }

    @Override
    public void yourself() {
        super.yourself();
        System.out.println("Soy estudiante de " + carrera + " con matrícula " + matricula + ".");
    }
}
//Clase Profesor que hereda de Persona
public class Profesor extends Person {
    private String especialidad;
    private String grupo;

    public Profesor(String nombre, int edad, String especialidad, String grupo) {
        super(nombre, edad);
        this.especialidad = especialidad;
        this.grupo = grupo;
    }
    @Override
    public void yourself() {
        super.yourself();
        System.out.println("Soy profesor de " + especialidad + " y enseño al grupo " + grupo + ".");
    }
}
//Clase principal con el método main
public class Main {
    public static void main(String[] args) {
        Person persona = new Person("Michaella", 40);
        persona.yourself();
        System.out.println();



    Estudiante estudiante = new Estudiante("Joshhh", 20, "A012345", "Ingeniería en Computación");
        estudiante.yourself();
        System.out.println();
 

    Profesor profesor = new Profesor("Josefina", 35, "Matemáticas", "3A");
        profesor.yourself();
    }
}
