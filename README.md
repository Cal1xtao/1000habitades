# 1000habitades
package exercicio2_205;
import java.util.Scanner;
public class exercicio2_205 {
	public static void main(String[] args){
		Scanner ler = new Scanner(System.in);
		int gen;
		double alturaf=0,somaAf=0,alturam=0,somaAm=0,idade,i;
		double fem=0,masc=0,outro=0,somag=0,somagm=0,idadem=0,alturao=0,idadeo=0;
		double media_idadegeral=0, media_idadem,percentual=0;
		for (i=0;i<=999;i++) {
			System.out.printf("Digite seu genero (0 para feminino, 1 para masculino e 2 para outro):\n");
			gen=ler.nextInt();
			switch (gen) {
			case 0:
				System.out.printf("Genero escolhido: Feminino\n");
				fem=fem+1;
				System.out.printf("Informe sua altura:\n");
				alturaf=ler.nextFloat();
				somaAf=alturaf+somaAf;
				System.out.printf("Informe sua idade:\n");
				idade=ler.nextInt();
				if (idade>=18 && idade<=35)
					media_idadegeral=idade+media_idadegeral;
				idade=idade+somag;
				break;
		    case 1:
		    	System.out.printf("Genero escolhido: Masculino\n");
		    	masc=masc+1;
		    	System.out.printf("Informe sua altura:\n");
		    	alturam=ler.nextFloat();
				somaAm=alturam+somaAm;
				System.out.printf("Informe sua idade:\n");
				idadem=ler.nextInt();
				if (idadem>=18 && idadem<=35)
					media_idadegeral=idadem+media_idadegeral;
				idadem=idadem+somagm;
				break;
		    case 2:
		    	System.out.printf("Genero escolhido: outro\n");
		    	outro=outro+1;
		    	System.out.printf("Informe sua altura:\n");
		    	alturao=ler.nextFloat();
		    	System.out.printf("Informe sua idade:\n");
		    	idadeo=ler.nextInt();
		    	if (idadeo>=18 && idadeo<=35)
					media_idadegeral=idadeo+media_idadegeral;
		    	break;
			}
	}
		System.out.printf("Quantidade de mulheres %f , quantidade de homens e quantidade de pessoas que se identificam como outro %f\n", fem,masc,outro);
		System.out.printf("Media da idade geral e %f\n",media_idadegeral/5);
		System.out.printf("Media da altura das mulheres e %f\n",somaAf/fem);
		System.out.printf("Media da idade dos homens e %f\n",idadem/masc);
		System.out.printf("Pessoas que se identificam como outro %f\n",outro);
		System.out.printf("Percentual de pessoas com idades entre 18 e 35 anos e %f\n",media_idadegeral/100);
	}
}
![1000hab](https://user-images.githubusercontent.com/101893557/168133448-642e693a-3ed4-4bde-bdb0-41ea21e10493.jpeg)
