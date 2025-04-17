# poo_sistema_escolar

//clase persona
public class Person{
	protected String nombre;
	protected int edad;

	public Person(String nombre, int edad){
		this.nombre = nombre;
		this.edad = edad;
	}

	public void yourself(){
		System.out.println("Hola, me llamo " + nombre + " y tengo " + edad + " años.");
	}
}

//clase estudiante
public class Estudiante extends Person{
	private String matricula;
	private String carrera;

	public Estudiante(String nombre, int edad, String matricula, String carrera){
		super(nombre, edad);
		this.matricula = matricula;
		this.carrera = carrera;
	}

	@Override
	public void yourself(){
		super.yourself();
		System.out.println("Soy estudiante de " + carrera + " con matrícula " + matricula + ".");
	}
}

//Clase profesor hereda persona
public class Profesor extends Person{
	private String especialidad;
	private String grupo;

	public Profesor(String nombre, int edad, String especilidad, String grupo){
		super(nombre, edad);
		this.especialidad = especialidad;
		this.grupo = grupo;
	}

	@Override
	public void yourself(){
		super.yourself();
		System.out.println("Soy profesor de " + especialidad + " y enseño al grupo " + grupo + ".");
	}
}

//Clase principal metodo main
public class Main{
	public static void main(String[] args){
		
		Persona persona = new Person("Marco", 40);
		persona.yourself();
		System.out.println();

		Estudiante estudiante = new Estudiante("Ana", 20; "A012344", "Ingeniería en Computación");
		estudiante.yourself();
		System.out.println();

		Profesor profesor = new Profesor("Michelle", 23, "Quimica", "3A");
		profesor.yourself();
	}
}

