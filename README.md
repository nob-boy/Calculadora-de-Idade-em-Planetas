# Calculadora de Idade em Planetas

def calcular_idade_em_planeta(idade_em_anos, fator):
    idade_no_planeta = idade_em_anos / fator
    return idade_no_planeta

def main():
    print("Bem-vindo à Calculadora de Idade em Planetas!")
    idade = float(input("Digite sua idade em anos terrestres: "))
    
    planetas = {
        "Mercúrio": 0.2408467,
        "Vênus": 0.61519726,
        "Marte": 1.8808158,
        "Júpiter": 11.862615,
        "Saturno": 29.447498,
        "Urano": 84.016846,
        "Netuno": 164.79132
    }
    
    print("\nEscolha um planeta para calcular sua idade:")
    for i, planeta in enumerate(planetas.keys(), start=1):
        print(f"{i}. {planeta}")
    
    escolha = int(input("\nDigite o número do planeta escolhido: "))
    
    planetas_list = list(planetas.values())
    planeta_escolhido = list(planetas.keys())[escolha - 1]
    fator_escolhido = planetas_list[escolha - 1]
    
    idade_no_planeta = calcular_idade_em_planeta(idade, fator_escolhido)
    print(f"\nSua idade em {planeta_escolhido} seria de {idade_no_planeta:.2f} anos.")

if __name__ == "__main__":
    main()

