import math

print("=== SISTEMA DE FÍSICA -2º BIMESTRE ===")
print("Escolha o tema:")
print("1. 1ª Lei do Termodinâmica")
print("2. Ciclos Termodinâmicos")
print("3. Calores Específicos dos Gases Perfeitos")
print("4. Máquinas térmicas e 2ª Lei da termodinâmica")
print("5. Ciclos de Carnot")
print("6. Refrigeradores")
print("7. Ondas")
print("0. Sair")

while True:
    tema = input("\nDigite o número do tema: ")
    if tema  =='0':
        print("Encerrando programa...")
        break
    #1ª Lei da termodinâmica
    elif tema == '1':
        print("\n=== 1ª LEI DA TERMODINÂMICA ===")
        print("ΔU = Q - W")
        print("1. Calcular variação de energia interna")
        print("2. Calcular calor trocado")
        print("3. Calcular trabalho realizado")

        opçao = input("Escolha o cálculo: ")

        if opçao == '1':
            Q = float(input("Calor Trocado (J): "))
            W = float(input("Trabalho realizado (J): "))
            delta_U = Q - W 
            print(f"\nVariação de energia interna(ΔU) = {delta_U} J")
            if delta_U > 0:
                print("A energia interna do sistema aumentou.")
            elif delta_U < 0:
                print("A energia interna do sistema diminuiu.")
        else:
                print("A energia interna do sistema permaneceu constante.")

    elif opçao == '2':
            delta_U = float(input("Variação de energia interna (J): "))
            W = float(input("Trabalho realizados (J):"))
            Q = delta_U + W 
            print(f"\nCalor trocado (Q) = {Q} J")
            if Q > 0:
                print("O sisitema absorveu o calor.")
            elif Q < 0:
                print("O sistema liberou calor.")     
    elif opçao == '3':
        Q = float(input("Calor trocado (J): "))
        delta_U = float(input("Variação de energia interna (J): "))
        W = Q - delta_U
        print(f"\nTrabalho realizado (W) = {W} J")
        if W > 0:
            print("O sistema realizou trabalho sobre o ambiente.")
        elif W < 0:
            print("O ambiente realizou trabalho sobre o sistema.")

              #Ciclos Termodinamicos
    elif tema == '2':
         print("\n=== CICLOS TERMODINÂMICOS ===")
         print("1. Trabalho no ciclo (Área do ciclo)")
         print("2. Rendimento ciclo")

         opçao = input("Escolha o cálculo: ")
    if opçao  == '1':
         print("\nDigite os valores do ciclo no diagrama P x V")
         P_max = float(input("Pressão máxima (Pa): "))
         P_min = float(input("Pressão mínima (Pa): "))
         V_max = float(input("Volume máximo (m³): "))
         V_min = float(input("Volume mínimo (m³): "))
         W = (P_max - P_min * V_max - V_min)
         print(f"\nTrabalho no ciclo = {W} J")

    elif opçao == '2':
         Q_abs = float(input("Calor absorvido (J): "))
         Q_libera = float(input("Calor liberado (J): "))
         rendimento = (Q_abs - Q_libera) / Q_abs
         print(f"\nRendimento do ciclo = {rendimento:.2%}")
