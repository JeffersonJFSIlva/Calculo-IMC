# Calculo-IMC
Programa que calcula o IMC - Índice de Massa Corporal

public class Paciente {
	private double peso;
	private double altura;

	public Paciente( double peso, double altura ){
		this.peso = peso;
		this.altura = altura;
		
	}


	public double getPeso() {
		return peso;
	}


	public void setPeso(double peso) {
		this.peso = peso;
	}


	public double getAltura() {
		return altura;
	}


	public void setAltura(double altura) {
		this.altura = altura;
	}
	
	public double calcularIMC (double peso, double altura) {
		double IMC;
		IMC = peso / (altura *altura);
		return IMC;
		
	}
	
	public String diagnostico(double IMC) {
		
		if(IMC < 16) {
			return "Baixo peso Muito Grave!";
		}
		if(IMC >= 16 && IMC < 16.99) {
			return "Baixo peso grave";
		}	
		if(IMC >= 17 && IMC < 18.49) {
			return "Baixo peso";
		}
		if(IMC >= 18.50 && IMC < 24.99) {
			return "Peso normal";
		}
		if(IMC >= 25 && IMC < 29.99) {
			return "Sobrepeso";
		}
		if(IMC >= 30 && IMC < 34.99) {
			return "Obesidade grau I";
		}
		if(IMC >= 35 && IMC < 39.99) {
			return "Obesidade grau II";
		}
		if(IMC >= 40) {
			return "Obesidade grau III (Obesidade mórbida)";
		}
		return null;
	}
}


public class Principal {

	public static void main(String[] args) {
		
		System.out.println("Paciente 1\n");
		Paciente p1 = new Paciente (70, 1.65);
		System.out.println(p1.calcularIMC(p1.getPeso(), p1.getAltura()));
		System.out.println(p1.diagnostico(p1.calcularIMC(p1.getPeso(), p1.getAltura())));
	
		System.out.println("\nPaciente 2\n");
		Paciente p2 = new Paciente (80, 1.70);
		System.out.println(p2.calcularIMC(p2.getPeso(), p2.getAltura()));
		System.out.println(p2.diagnostico(p2.calcularIMC(p2.getPeso(), p2.getAltura())));
		
		System.out.println("\nPaciente 3\n");
		Paciente p3 = new Paciente (100, 1.75);
		System.out.println(p3.calcularIMC(p3.getPeso(), p3.getAltura()));
		System.out.println(p3.diagnostico(p3.calcularIMC(p3.getPeso(), p3.getAltura())));
	}
		
}
