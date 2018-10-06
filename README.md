package manejoarchivos;

import java.io.FileWriter;
import java.util.Scanner;
import utileria.Archivos;
import static utileria.Archivos.*;

public class ManejoArchivos {

    //Nota: Ya debe estar creada la carpeta sobre la que se va a trabajar
    //Y en caso necesario se deben asignar permisos de escritura a la carpeta
    private static final String NOMBRE_ARCHIVO = "C:\\Users\\jose\\Documents\\programacion II\\clase2.27julio\\ejercicio.txt";

    public static void main(String[] args) {
            
        System.out.println("MANEJO DE ARCHIVOS");
        System.out.println("1. Crear un archivo");
        System.out.println("2. Escribir en el archivo");
        System.out.println("3. Leer el archivo");
        System.out.println("4. Anexar el archivo");
       // System.out.println("5. ");
       
        Scanner op = new Scanner (System.in);
        System.out.println("Ingrese la opcion: ");
        op.nextInt();
        
      
        
        switch(op.nextInt()){
            case 1:
        //Crear un archivo
        crearArchivo(NOMBRE_ARCHIVO);
        Archivos crear = new Archivos();
        crear.crearArchivo("creacioDeArchivo.txt");
                System.out.println("Se ha creado correcramente el archivo");
        break;
        
            case 2:
        //Escribir a un archivo
        escribirArchivo(NOMBRE_ARCHIVO);
        Archivos escribir = new Archivos();
        escribir.escribirArchivo("creacioDeArchivo.txt");
        break;
        
            case 3:
        //Leer de un archivo
        leerArchivo(NOMBRE_ARCHIVO);
        Archivos leer = new Archivos();
        leer.leerArchivo("creacioDeArchivo.txt");
        break;
        
            case 4:
        //Anexar informacion a un archivo
        anexarArchivo(NOMBRE_ARCHIVO);
        Archivos anexar = new Archivos();
        anexar.anexarArchivo("creacioDeArchivo.txt");
        break;
        
        //    case 5:
        //Leer de un archivo
        //leerArchivo(NOMBRE_ARCHIVO);
        //Archivos lee = new Archivos();
        //lee.leerArchivo("creacioDeArchivo.txt");
        //        break;
        }
        
    }
}
