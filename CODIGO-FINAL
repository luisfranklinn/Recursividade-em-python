
from time import sleep

loop = True

# FUNCÕES PRONTAS
def vazio(lista):
    return lista == []


def cabeca(lista):
    return lista[0]


def cauda(lista):
    return lista[1:]


def insere(lista, x):
    lista.append(x)
    return lista


# FUNCÕES P FAZER
# CONCATENAÇÃO
def concatenacao(A, B):
    if vazio(A):
        return B
    if vazio(B):
        return A
    if vazio(A) and vazio(B):
        return []
    else:
        insere(A, cabeca(B))
        return f"A nova lista é: {concatenacao(A, cauda(B))}"


# COMPRIMENTO
def comprimento(A):
    if vazio(A):
        return 0
    return 1 + comprimento(cauda(A))


# ELEMENTO N
def elemento(A, n):
    if n == 0:
        return cabeca(A)
    else:
        n = n - 1
        return elemento(cauda(A), n)


# PERTENCE
def pertence(A, x):
    if vazio(A):
        return f"{x} não pertece a lista!"
    if cabeca(A) == x:
        return f"{x} pertece a lista!"
    return pertence(cauda(A), x)


# ULTIMO ELEMENTO
def ultimo(A):
    if vazio(A):
        return []
    if comprimento(A) == 1:
        return A
    else:
        anterior = []
        insere(anterior, cabeca(A))
        ultimo_elemento = "".join(map(str, ultimo(cauda(A))))
        return ultimo_elemento


# PRIMEIROS
def primeiros(A, n):
    if comprimento(A) == n:
        return A
    return primeiros(inverte(cauda(inverte(A))), n)


# INVERTE
def inverte(A):
    if vazio(A):
        return []
    invertida1 = inverte(cauda(A))
    invertida2 = insere(invertida1, cabeca(A))
    return invertida1


# MENU/LAÇO PRINCIPAL
while loop:
    escolha = input(
        "Olá, seja bem-vindo(a) ao programa\n Brincando com Listas!\n Com o que você gostaria de brincar hoje?\n 1)Concatenação? (União de duas listas)\n 2)Comprimento da lista?\n 3)Achar o elemento?\n 4)Verificar se pertence a lista?\n 5)Mostrar o último elemento?\n 6)Mostrar os N primeiros elementos?\n 7)Inverter a lista?\n 8)Sair?"
    )
    if (
        escolha != "1"
        and escolha != "2"
        and escolha != "3"
        and escolha != "4"
        and escolha != "5"
        and escolha != "6"
        and escolha != "7"
        and escolha != "8"
    ):
        while True:
            escolha = input(
                "Insira um valor entre 1 e 8!\n Com o que você gostaria de brincar hoje?\n 1)Concatenação? (União de duas listas)\n 2)Comprimento da lista?\n 3)Achar o elemento?\n 4)Verificar se pertence a lista?\n 5)Mostrar o último elemento?\n 6)Mostrar os N primeiros elementos?\n 7)Inverter a lista?\n 8)Sair?"
            )
            if (
                escolha != "1"
                and escolha != "2"
                and escolha != "3"
                and escolha != "4"
                and escolha != "5"
                and escolha != "6"
                and escolha != "7"
                and escolha != "8"
            ):
                pass
            else:
                break

    # CONCATENAÇÃO
    if escolha == "1":
        #!LISTA 1
        lista_1 = []
        colocar_1 = input("O que você gostaria de inserir na primeira lista?:")
        lista_1.append(colocar_1)
        while True:
            escolha_2 = input("Deseja continuar?\n 1)Sim?\n 2)Não?")
            if escolha_2 == "1":
                colocar_1 = input("O que você gostaria de inserir na primeira lista?:")
                lista_1.append(colocar_1)
            elif escolha_2 == "2":
                break
            else:
                print("Insira um valor entre 1 e 2!")
        #!LISTA 2
        lista_2 = []
        colocar_2 = input("O que você gostaria de inserir na segunda lista?:")
        lista_2.append(colocar_2)
        while True:
            escolha_3 = input("Deseja continuar?\n 1)Sim?\n 2)Não?")
            if escolha_3 == "1":
                colocar_2 = input("O que você gostaria de inserir na segunda lista?:")
                lista_2.append(colocar_2)
            elif escolha_3 == "2":
                break
            else:
                print("Insira um valor entre 1 e 2!")
        print(concatenacao(lista_1, lista_2))
        dados = open("Dados.txt", "a")
        dados.write(
            f"CONCATENAÇÃO\nLista 1:{lista_1}\nLista 2:{lista_2}\n{concatenacao(lista_1, lista_2)}"
        )
        dados.write("\n")
        dados.close()

    # COMPRIMENTO
    elif escolha == "2":
        lista_1 = []
        colocar_1 = input("O que você gostaria de inserir na sua lista?:")
        lista_1.append(colocar_1)
        while True:
            escolha_2 = input("Deseja continuar?\n 1)Sim?\n 2)Não?")
            if escolha_2 == "1":
                colocar_1 = input("O que você gostaria de inserir na sua lista?:")
                lista_1.append(colocar_1)
            elif escolha_2 == "2":
                break
            else:
                print("Insira um valor entre 1 e 2!")
        print(f"O comprimento da sua lista é: {comprimento(lista_1)}")
        dados = open("Dados.txt", "a")
        dados.write(
            f"COMPRIMENTO\nLista:{lista_1}\nComprimento da lista: {comprimento(lista_1)}"
        )
        dados.write("\n")
        dados.close()

    # ELEMENTO N
    elif escolha == "3":
        lista_1 = []
        colocar_1 = input("O que você gostaria de inserir na sua lista?:")
        lista_1.append(colocar_1)
        while True:
            escolha_2 = input("Deseja continuar?\n 1)Sim?\n 2)Não?")
            if escolha_2 == "1":
                colocar_1 = input("O que você gostaria de inserir na sua lista?:")
                lista_1.append(colocar_1)
            elif escolha_2 == "2":
                break
            else:
                print("Insira um valor entre 1 e 2!")

        while True:
            escolha_3 = int(
                input(
                    f"Qual elemento da lista você deseja saber?\nVocê pode escolher entre 1 e {len(lista_1)}!:"
                )
            )
            if escolha_3 > len(lista_1) or escolha_3 < 1:
                print(f"Insira um valor entre 1 e {len(lista_1)}!")
            else:
                print(f"O elemento {escolha_3} é: {elemento(lista_1, escolha_3 - 1)}")
                break
        dados = open("Dados.txt", "a")
        dados.write(
            f"ELEMENTO N\nLista:{lista_1}\nO elemento {escolha_3} é: {elemento(lista_1, escolha_3-1)}"
        )
        dados.write("\n")
        dados.close()

    # PERTENCE
    elif escolha == "4":
        lista_1 = []
        colocar_1 = input("O que você gostaria de inserir na sua lista?:")
        lista_1.append(colocar_1)
        while True:
            escolha_2 = input("Deseja continuar?\n 1)Sim?\n 2)Não?")
            if escolha_2 == "1":
                colocar_1 = input("O que você gostaria de inserir na sua lista?:")
                lista_1.append(colocar_1)
            elif escolha_2 == "2":
                break
            else:
                print("Insira um valor entre 1 e 2!")

        escolha_3 = input("Qual elemento da lista você deseja verificar se pertence?")

        print(pertence(lista_1, escolha_3))
        dados = open("Dados.txt", "a")
        dados.write(f"PERTENCE\nLista:{lista_1}\n{pertence(lista_1, escolha_3)}")
        dados.write("\n")
        dados.close()

    # ULTIMO
    elif escolha == "5":
        lista_1 = []
        colocar_1 = input("O que você gostaria de inserir na sua lista?:")
        lista_1.append(colocar_1)
        while True:
            escolha_2 = input("Deseja continuar?\n 1)Sim?\n 2)Não?")
            if escolha_2 == "1":
                colocar_1 = input("O que você gostaria de inserir na primeira lista?:")
                lista_1.append(colocar_1)
            elif escolha_2 == "2":
                break
            else:
                print("Insira um valor entre 1 e 2!")
        print(f"O ultimo elemento é: {ultimo(lista_1)}")
        dados = open("Dados.txt", "a")
        dados.write(f"ÚLTIMO\nLista :{lista_1}\nO ultimo elemento é: {ultimo(lista_1)}")
        dados.write("\n")
        dados.close()

    # PRIMEIROS
    elif escolha == "6":
        lista_1 = []
        colocar_1 = input("O que você gostaria de inserir na sua lista?:")
        lista_1.append(colocar_1)
        while True:
            escolha_2 = input("Deseja continuar?\n 1)Sim?\n 2)Não?")
            if escolha_2 == "1":
                colocar_1 = input("O que você gostaria de inserir na sua lista?:")
                lista_1.append(colocar_1)
            elif escolha_2 == "2":
                break
            else:
                print("Insira um valor entre 1 e 2!")
        while True:
            escolha_3 = int(
                input(
                    f"Até qual elemento da lista você deseja mostrar?\nVocê pode escolher entre 1 e {len(lista_1)}!:"
                )
            )
            if escolha_3 > len(lista_1) or escolha_3 < 1:
                print(f"Insira um valor entre 1 e {len(lista_1)}!")
            else:
                print(primeiros(lista_1, escolha_3))
                break
        dados = open("Dados.txt", "a")
        dados.write(
            f"PRIMEIROS N\nLista:{lista_1}\nOs {escolha_3} primeiros elementos são: {primeiros(lista_1, escolha_3)}"
        )
        dados.write("\n")
        dados.close()

    # INVERTE
    elif escolha == "7":
        lista_1 = []
        colocar_1 = input("O que você gostaria de inserir na lista para inverter?:")
        lista_1.append(colocar_1)
        while True:
            escolha_2 = input("Deseja continuar?\n 1)Sim?\n 2)Não?")
            if escolha_2 == "1":
                colocar_1 = input(
                    "O que você gostaria de inserir na lista para inverter?:"
                )
                lista_1.append(colocar_1)
            elif escolha_2 == "2":
                break
            else:
                print("Insira um valor entre 1 e 2!")

        print(inverte(lista_1))
        dados = open("Dados.txt", "a")
        dados.write(f"INVERTE\nLista :{lista_1}\n{(inverte(lista_1))}")
        dados.write("\n")
        dados.close()

    # SAÍDA
    elif escolha == "8":
        print("Muito obrigado!")
        break

    # DESEJA CONTINUAR?
    sleep(2)
    while True:
        escolha_4 = input("Deseja brincar novamente?\n 1)Sim?\n 2)Não?\n")
        if escolha_4 != "1" and escolha_4 != "2":
            print("Insira um valor entre 1 e 2!")
        elif escolha_4 == "1":
            break
        if escolha_4 == "2":
            print("Muito obrigado!")
            loop = False
            break
