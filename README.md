# ArreglosEstudiantes
import java.util.*; public class Notas  { public static void main(String[] args) {

	Scanner sc = new Scanner(System.in);
	
	String[] alumno = new String[10];
	String[] apellido = new String[10];
	double[] nota = new double[10];
	
	String nombreMayor, apellidoMayor;
	double notaMayor;
	
	int i = 0;
	
	System.out.println("Ingrese el nombre de cada uno de los estudiantes y su respectiva nota: ");
	System.out.print("Estudiante " + (i + 1) + ": ");
	alumno[i] = sc.nextLine();
	System.out.print("Apellido: ");
	apellido[i] = sc.nextLine();
	System.out.print("Nota: ");
	nota[i] = sc.nextDouble();
	
	notaMayor = nota[i];
	nombreMayor = alumno[i];
	apellidoMayor = apellido[i];
	
	for(i = 1; i < alumno.length; i++) {
		sc.nextLine();
		System.out.print("Estudiante " + (i + 1) + ": ");
		alumno[i] = sc.nextLine();
		System.out.print("Apellido: ");
		apellido[i] = sc.nextLine();
		System.out.print("Nota: ");
		nota[i] = sc.nextDouble();
		
		if(nota[i] > notaMayor) {
			notaMayor = nota[i];
			nombreMayor = alumno[i];
			apellidoMayor = apellido[i];
		}
	}
	System.out.println("El estudiante con mayor nota es: " + nombreMayor + " " + apellidoMayor);
	System.out.println("Nota: " + notaMayor);
}
}
