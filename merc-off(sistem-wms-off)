estoque = {}
carrinho = {}
print("O que deseja?")
while True:
    
    print("\n1. Gostaria de dicionar item ao estoque")
    print("2.Gostaria de verificar item no estoque")
    print("3. Gostaria de remover item do estoque")
    print("4. Gostaria de ver todos os itens no estoque")
    print("5. Sair do programa")

    opcao = int(input("\nPor favor, escolha uma opção: "))

    if opcao == 1:
        item = input("Digite o nome do item: ")
        quantidade = int(input("Digite a quantidade do item: "))
        estoque[item] = quantidade
        print(f"{quantidade} {item}(s) adicionado(s) ao estoque.")

    elif opcao == 2:
        item = input("Digite o nome do item: ")
        if item in estoque:
            print(f"{estoque[item]} {item}(s) no estoque.")
        else:
            print("Item não encontrado no estoque.")

    elif opcao == 3:
        item = input("Digite o nome do item: ")
        if item in estoque:
            del estoque[item]
            print(f"{item} removido do estoque.")
        else:
            print("Item não encontrado no estoque.")

    elif opcao == 4:
        print("Itens no estoque:")
        for item, quantidade in estoque.items():
            print(f"{quantidade} {item}(s)")

    elif opcao == 5:
        break

    else:
        print("Opção inválida. Tente novamente.")
while True:
    print("\n1. Adicionar item ao carrinho")
    print("2. Remover item do carrinho")
    print("3. Ver itens no carrinho")
    print("4. Finalizar compra")
    print("5. Sair do programa")

    opcao = int(input("\nEscolha uma opção: "))

    if opcao == 1:
        item = input("Digite o nome do item: ")
        if item in estoque:
            quantidade = int(input("Digite a quantidade do item: "))
            if quantidade <= estoque[item]:
                carrinho[item] = carrinho.get(item, 0) + quantidade
                estoque[item] -= quantidade
                print(f"{quantidade} {item}(s) adicionado(s) ao carrinho.")
            else:
                print("Quantidade insuficiente no estoque.")
        else:
            print("Item não encontrado no estoque.")

    elif opcao == 2:
        item = input("Digite o nome do item: ")
        if item in carrinho:
            quantidade = carrinho[item]
            del carrinho[item]
            estoque[item] += quantidade
            print(f"{quantidade} {item}(s) removido(s) do carrinho.")
        else:
            print("Item não encontrado no carrinho.")

    elif opcao == 3:
        print("Itens no carrinho:")
        for item, quantidade in carrinho.items():
            print(f"{quantidade} {item}(s)")

    elif opcao == 4:
        total = sum(quantidade * preco for item, quantidade, preco in [(item, carrinho[item], precos[item]) for item in carrinho])
        print(f"Total da compra: R$ {total:.2f}")
        for item, quantidade in carrinho.items():
            estoque[item] -= quantidade
        carrinho = {}
        print("Compra finalizada com sucesso!")

    elif opcao == 5:
        break

    else:
        print("Opção inválida. Tente novamente.")

