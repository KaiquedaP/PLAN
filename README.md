# PLAN
JAVE
CODE


//INATkkk


//package exercicio;

import javafx.print.Printer;

public class Aluno {

    private String nome;
    private double nota2; 
    private double nota1;

    public Aluno(String nome, double nota2, double nota1) {
        this.nome = nome;
        this.nota2 = nota2;
        this.nota1 = nota1;
    }
    public  void consultarSituacao(){
        if (calcularMedia() >= 7) {
            System.out.println("Aprovado");
        } else if(calcularMedia() > 5 && calcularMedia() < 7){
            System.out.println("Recuperação");
        } else{
            System.out.println("Reprovado");
        }
    }

    public double calcularMedia(){
            return(nota1 + nota2) / 2;
    }
    
    
    
    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public double getNota2() {
        return nota2;
    }

    public void setNota2(double nota2) {
        this.nota2 = nota2;
    }

    public double getNota1() {
        return nota1;
    }

    public void setNota1(double nota1) {
        this.nota1 = nota1;
    }

    
    
}






package exercicio;


public class Main {
    public static void main(String[] args) {
         
        Aluno aluno = new Aluno ("Caio", 10, 10);
        
        System.out.println("nome: " + aluno.getNome());
        System.out.println("Media: " + aluno.calcularMedia());
        aluno.consultarSituacao();
    }
}
