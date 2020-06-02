package clasesIvan;

import java.util.Scanner;

public class matrizIdentidad {
	
	public static int[][] generarMatriz(int filas,int columnas) {
		
		Scanner entrada = new Scanner(System.in);
		int [][] matriz = new int [filas][columnas];
		System.out.println("introduce los valores");
		for(int i = 0; i < matriz.length; i++) {
			for(int j = 0; j < matriz.length; j++) {
				
				matriz[i][j] = entrada.nextInt();
			}
		}
		return matriz;
	}
	public static void imprimeMatriz(int [][] matriz) {
		System.out.println("---MATRIZ ORIGINAL---");
		for(int i = 0; i < matriz.length; i++) {
			System.out.println();
			for(int j = 0; j < matriz.length; j++) {
				System.out.print(matriz[i][j] + " ");	
			}
		}	
	}
	public static boolean diagPrincipalEs1(int[][] matriz) {
		
		int numeros;
		for(int i = 0; i < matriz.length; i++) {
			for(int j = 0;j < matriz.length; j++) {
				if(i == j) {
					numeros = matriz[i][j];
					if(numeros != 1)
						return false;
				}	
			}
		}
		return true;
	}
	
	public static void main(String[] args) {
		// TODO Auto-generated method stub

		Scanner entrada = new Scanner(System.in);
		int filas;
		int columnas;
		int veces = 3;
		
		for(int i = 0; i < veces; i++) {
			System.out.println("introduce el nº de filas");
			filas = entrada.nextInt();
			System.out.println("introduce el nº de columnas");
			columnas = entrada.nextInt();
			if(filas != columnas) {
				System.out.println("dede de tener el mismo nº de filas q de columnas");
				System.exit(0);
			}
			if(filas < 2 || filas > 50 || columnas < 2 && columnas > 50) {
				System.out.println("dimension de la matriz no valida\n 2 x 2 o 50 x 50");
				System.exit(0);
			}
			int[][] matrizAux = new int [filas][columnas];
			matrizAux = matrizIdentidad.generarMatriz(filas, columnas);
			System.out.println("has elegido una matriz de " + filas + " filas por " + columnas + " columnas");
			imprimeMatriz(matrizAux);
			System.out.println("\n---¿¿ES MATRIZ IDENTIDAD ??---\n" + matrizIdentidad.diagPrincipalEs1(matrizAux));		
		}
	}
}
