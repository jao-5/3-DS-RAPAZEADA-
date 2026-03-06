# 3-DS-RAPAZEADA-
def calculadora():
    print("Calculadora simples: digite 'sair' para encerrar.")
    while True:
        operacao = input("Digite a operação (ex: 2 + 3): ")
        if operacao.lower() == "sair":
            print("Encerrando a calculadora. Até logo!")
            break
        try:
            numeros = operacao.split()
            if len(numeros) != 3:
                print("Formato inválido! Use: número operador número")
                continue
            a, operador, b = numeros
            a, b = float(a), float(b)
            if operador == "+":
                resultado = a + b
            elif operador == "-":
                resultado = a - b
            elif operador == "*":
                resultado = a * b
            elif operador == "/":
                if b == 0:
                    print("Erro: divisão por zero!")
                    continue
                resultado = a / b
            else:
                print("Operador inválido! Use +, -, * ou /")
                continue
            print("Resultado:", resultado)
        except ValueError:
            print("Digite números válidos!")

calculadora()
