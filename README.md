# calculadorapy
teste de uma calculadora em python

def soma(a, b):
    return a + b

def subtracao(a, b):
    return a - b

def multiplicacao(a, b):
    return a * b

def divisao(a, b):
    if b != 0:
        return a / b
    else:
        return "Não é possível dividir por zero."

# Função principal
def calculadora():
    while True:
        print("\nEscolha a operação:")
        print("1. Soma")
        print("2. Subtração")
        print("3. Multiplicação")
        print("4. Divisão")
        print("5. Sair")

        escolha = input("Digite o número da operação desejada: ")

        if escolha == '5':
            print("Saindo da calculadora. Até mais!")
            break

        if escolha in ('1', '2', '3', '4'):
            num1 = float(input("Digite o primeiro número: "))
            num2 = float(input("Digite o segundo número: "))

            if escolha == '1':
                print(f"\nResultado: {soma(num1, num2)}")
            elif escolha == '2':
                print(f"\nResultado: {subtracao(num1, num2)}")
            elif escolha == '3':
                print(f"\nResultado: {multiplicacao(num1, num2)}")
            elif escolha == '4':
                print(f"\nResultado: {divisao(num1, num2)}")
            else:
                print("Opção inválida. Tente novamente.")
        else:
            print("Opção inválida. Tente novamente.")

# Chamar a função principal
calculadora()
