# LoginJava

import java.util.Scanner;

public class Login {

    public static void main(String[] arg) {

        Scanner scanner = new Scanner(System.in);


        System.out.println("Digite seu nome: ");
        String nomeA = scanner.nextLine();

        System.out.println("Digite seu sobrenome: ");
        String nomeB = scanner.nextLine();


        String[] text;
        text = nomeA.split("");
        String letra = String.valueOf(text[0].charAt(0));
        String sobrenome = text[text.length - 1];

        String log = letra + "_" + sobrenome;
        System.out.println(log);


        System.out.println("Cadastre uma senha");
        String pwd = scanner.nextLine();
        if (pwd.matches("(^(?=.[0-9])(?=.[a-z])(?=.[-, !,@])(?=.[A-Z])(?=.*\\d).+)") && pwd.length() > 7) {

            System.out.println("Senha cadastrada com sucesso");

        } else {
            System.out.println("Necessário que sua senha possua 8 digitos, pelo menos uma letra maiuscula, um numero e um caractere especial");

        }

    }
}

