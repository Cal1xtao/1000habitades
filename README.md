#1000habitantes
package exercicio2_205;
import java.util.Scanner;
public class exercicio2_205 {
	public static void main(String[] args){
		Scanner ler = new Scanner(System.in);
		//Setando e inicializando variáveis
		int gen;
		double alturaf=0,somaAf=0,alturam=0,somaAm=0,idade,i;
		double fem=0,masc=0,outro=0,somag=0,somagm=0,idadem=0,alturao=0,idadeo=0;
		double media_idadegeral=0, media_idadem,percentual=0;
		//For para repetir a impressão pedindo para digitar o genero da pessoa
		for (i=0;i<=999;i++) {
			System.out.printf("Digite seu genero (0 para feminino, 1 para masculino e 2 para outro):\n");
			//Lendo o genero escolhido
			gen=ler.nextInt();
			//Switch para determinar o que ocorre caso a pessoa digite 0 ou 1 ou 2
			switch (gen) {
			case 0:
				//Imprimindo o genero escolhido
				System.out.printf("Genero escolhido: Feminino\n");
				//Somando a quantidade de vezes que o genero foi escolhido
				fem=fem+1;
				//Pedindo a altura da pessoa
				System.out.printf("Informe sua altura:\n");
				//Lendo a altura
				alturaf=ler.nextFloat();
				//Somando a altura da pessoa 
				somaAf=alturaf+somaAf;
				//Pedindo a idade da pessoa
				System.out.printf("Informe sua idade:\n");
				//Lendo a idade da pessoa
				idade=ler.nextInt();
				//If para separar as pessoas com idade entre 18 anos e 35 anos
				if (idade>=18 && idade<=35)
					//Somando idade em uma variável
					media_idadegeral=idade+media_idadegeral;
				//Somando idade em outra variável, que é uma variável geral
				idade=idade+somag;
				break;
		    case 1:
		    	//Imprimindo o genero escolhido
		    	System.out.printf("Genero escolhido: Masculino\n");
		    	//Somando a quantidade de vezes que o genero foi escolhido
		    	masc=masc+1;
		    	//Pedindo a altura da pessoa
		    	System.out.printf("Informe sua altura:\n");
		    	//Lendo a altura
		    	alturam=ler.nextFloat();
		    	//Somando altura da pessoa		
				somaAm=alturam+somaAm;
				//Pedindo a idade da pessoa
				System.out.printf("Informe sua idade:\n");
				//Lendo a idade da pessoa
				idadem=ler.nextInt();
				//If para separar as pessoas com idade entre 18 anos e 35 anos
				if (idadem>=18 && idadem<=35)
					//Somando idade em uma variável
					media_idadegeral=idadem+media_idadegeral;
				//Somando idade em outra variável, que é uma variável geral
				idadem=idadem+somagm;
				break;
		    case 2:
		    	//Imprimindo o genero escolhido
		    	System.out.printf("Genero escolhido: outro\n");
		    	//Somando a quantidade de vezes que o genero foi escolhido
		    	outro=outro+1;
		    	//Pedindo a altura da pessoa
		    	System.out.printf("Informe sua altura:\n");
		    	//Lendo a altura
		    	alturao=ler.nextFloat();
		    	//Pedindo a idade da pessoa
		    	System.out.printf("Informe sua idade:\n");
		    	//Lendo a idade da pessoa
		    	idadeo=ler.nextInt();
		    	//If para separar as pessoas com idade entre 18 anos e 35 anos
		    	if (idadeo>=18 && idadeo<=35)
		    		//Somando idade em uma variável
					media_idadegeral=idadeo+media_idadegeral;
		    	break;
			}
	}
		//Imprimindo a quantidade de vezes que os generos foram escolhidos
		System.out.printf("Quantidade de mulheres %f , quantidade de homens e quantidade de pessoas que se identificam como outro %f\n", fem,masc,outro);
		//Imprimindo a media da idade geral
		System.out.printf("Media da idade geral e %f\n",media_idadegeral/5);
		//Imprimindo a media da altura das mulheres
		System.out.printf("Media da altura das mulheres e %f\n",somaAf/fem);
		//Imprimindo a media da idade dos homens
		System.out.printf("Media da idade dos homens e %f\n",idadem/masc);
		//Imprimindo o total de pessoas que se identificaram como outro
		System.out.printf("Pessoas que se identificam como outro %f\n",outro);
		//Exibindo o percentual de pessoas com idade entre 18 e 35 anos
		System.out.printf("Percentual de pessoas com idades entre 18 e 35 anos e %f\n",media_idadegeral/100);
	}
}
