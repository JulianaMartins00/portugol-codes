programa
{
	inclua biblioteca Util

	inteiro navex = 1, navey = 2
	
	funcao inicio()
	{
		logico jogarnovamente = verdadeiro
		
		enquanto (jogarnovamente){

		cadeia nomenojogo, continua
		inteiro pontos, jogadaRebelde = 0, jogadaDarth = 0, nave 
		inteiro ganhou = 0, perdeu = 0, usarforca = 0
		logico usouhabilidade = falso
		
		escreva("Olá, você acaba de ser recrutada para lutar ao lado dos Rebeldes, Rey\n")
		escreva("________________________________________________________________________\n")
		

//começo do jogo - escolha nave	
		escolhanave ()

// sorteio 			
		para(inteiro rodada = 0; rodada < 3; rodada++ ) {
			jogadaRebelde = Util.sorteia(1, 6)
			jogadaDarth = Util.sorteia(1, 6)
//usar habilidade ou não
		se (usouhabilidade == falso){
			escreva("Você quer usar a força da Princeia Leia para duplicar seu poder? Digite 1 para sim ou 2 para não \n")
			leia(usarforca)
		} se(usarforca == 1) {
				jogadaRebelde = jogadaRebelde*2
				resposta(jogadaRebelde, jogadaDarth)
				(usouhabilidade = verdadeiro)
		}senao{
				escreva("Você decidiu não usar a força da Princesa Leia para aumentar seu poder. Aperte S para continuar\n")
				leia(continua)
				resposta(jogadaRebelde, jogadaDarth)
		}
		se (usouhabilidade ==verdadeiro){
			escreva ("Você não pode mais usar o poder. Aperte S para enfrentar o Império sem a força da Princesa Leia ao seu lado\n")
			leia(continua)
		}
		}
		escreva("Você deseja jogar novamente?")
		cadeia respostajogarnovamente
		leia(respostajogarnovamente)
		se (respostajogarnovamente == "sim"){
			jogarnovamente = verdadeiro
		}
		senao {
			jogarnovamente = falso
		}
		}
	}

//funcao tipo de resposta
		funcao vazio resposta (inteiro jogRebel, inteiro jogDarth){
		se (jogRebel > jogDarth){
			escreva("Você ganhou essa rodada escreva. Essa é sua pontuação: " + jogRebel + " O Império fez: " + jogDarth+ ".\n")
			escreva("________________________________________________________________________\n")
		}senao {
			escreva("Você perdeu essa rodada. Essa é sua pontuação: " + jogRebel + " O Império fez: " + jogDarth+ ".\n")
			escreva("________________________________________________________________________\n")
			}
			}
		
//funcaoescolhanave		
		funcao vazio escolhanave (){
			inteiro decisao
			escreva("Você deve escolher qual será sua nave. Digite o número da nave escolhida.\nPara x-Wing, digite 1.\nPara Millennium Falcon, digite 2\n")
			leia(decisao)
			cadeia continua
		se ( decisao == 1){
			escreva ("Rey, você assumiu o comando da x-Wing e está pronta para a batalha. Aperte S para continuar\n")
			leia(continua)	
		}senao se(decisao ==2) {
			escreva ("Rey, você assumiu o comando da Millennium Falcon e está pronta para a batalha. Aperte S para continuar\n")
			leia(continua)	
			}
			}

}
