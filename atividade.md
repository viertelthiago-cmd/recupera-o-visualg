algoritmo "reservas_restaurante"

```bash
var
   vetorNome: vetor[1..10] de caractere
   vetorPessoas: vetor[1..10] de inteiro
   vetorData: vetor[1..10] de caractere
   vetorStatus: vetor[1..10] de caractere

   opcao: inteiro

   numero, quantidade, posicao: inteiro

   nomeBusca: caractere

   encontrou: logico

inicio

   numero <- 0

   repita

      escreval("===================================")
      escreval(" SISTEMA DE RESERVAS")
      escreval("===================================")
      escreval("1 - Registrar reserva")
      escreval("2 - Cancelar reserva")
      escreval("3 - Buscar reserva")
      escreval("4 - Listar reservas")
      escreval("5 - Total de reservas ativas")
      escreval("6 - Sair")
      escreval("Escolha uma opcao: ")
      leia(opcao)

      escolha opcao

         caso 1

            se numero < 10 entao

               numero <- numero + 1

               escreva("Nome do cliente: ")
               leia(vetorNome[numero])

               escreva("Quantidade de pessoas: ")
               leia(vetorPessoas[quantidade])

               escreva("Data da reserva: ")
               leia(vetorData[numero])

               vetorStatus[numero] <- "Ativa"

               escreval("Reserva cadastrada com sucesso!")

            senao

               escreval("Limite maximo de reservas atingido!")

            fimse

         caso 2

            escreva("Digite o nome para cancelar: ")
            leia(nomeBusca)

            encontrou <- falso

            para quantidade de 1 ate numero faca

               se vetorNome[numero] = nomeBusca entao

                  vetorStatus[numero] <- "Cancelada"
                  encontrou <- verdadeiro

               fimse

            fimpara

            se encontrou entao
               escreval("Reserva cancelada com sucesso!")
            senao
               escreval("Reserva nao encontrada!")
            fimse

         caso 3

            escreva("Digite o nome para buscar: ")
            leia(nomeBusca)

            encontrou <- falso

            para quantidade de 1 ate numero faca

               se vetorNome[i] = nomeBusca entao

                  escreval("Nome: ", vetorNome[numero])
                  escreval("Pessoas: ", vetorPessoas[numero])
                  escreval("Data: ", vetorData[numero])
                  escreval("Status: ", vetorStatus[numero])

                  encontrou <- verdadeiro
               fimse

            fimpara

            se encontrou = falso entao
               escreval("Reserva nao encontrada!")
            fimse

         caso 4

            se numero = 0 entao

               escreval("Nenhuma reserva cadastrada!")

            senao

               escreval("===== LISTA DE RESERVAS =====")

               para quantidade de 1 ate numero faca

                  escreval("----------------------------")
                  escreval("Nome: ", vetorNome[numero])
                  escreval("Pessoas: ", vetorPessoas[numero])
                  escreval("Data: ", vetorData[numero])
                  escreval("Status: ", vetorStatus[numero])

               fimpara

            fimse

         caso 5

            posicao <- 0

            para quantidade de 1 ate numero faca

               se vetorStatus[quantidade] = "Ativa" entao
                  posicao <- posicao + 1
               fimse

            fimpara

            escreval("Total de reservas ativas: ", posicao)

         caso 6

            escreval("Sistema encerrado!")

         outrocaso

            escreval("Opcao invalida!")

      fimescolha

   ate opcao = 6

fimalgoritmo
```