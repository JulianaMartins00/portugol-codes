programa
{
	inteiro n1,n2
	funcao inicio()
	{
		
		escreva("Digite um número\n")
		leia(n1)
		validacao1 () 
		escreva("Digite o segundo número\n")
		leia(n2)
		validacaon2 () 
		
		impressao ()
	}
		funcao vazio validacao1 () {
		enquanto (n1 <= 0) { 
			escreva("Precisa ser um número maior que 0. Vale 10, 100, 1000.... Digite novamente\n")
			leia(n1)
		}
		}
		funcao vazio validacaon2 () {
		enquanto (n2 <= 0) { 
			escreva("Precisa ser um número maior que 0. Vale 10, 100, 1000.... Digite novamente\n")
			leia(n2)
		}
		}
		funcao vazio impressao (){
		se (n1 > n2){
			escreva("O maior número é: " + n1)
		}senao escreva("O maior número é: " + n2)
		}
}
