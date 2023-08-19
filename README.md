# Função para calcular a taxa de lotação
def calcular_taxa_lotacao(area_pastagem, consumo_diario_por_animal):
    try:
        area_pastagem = float(area_pastagem)
        consumo_diario_por_animal = float(consumo_diario_por_animal)
        
        # Calcular a taxa de lotação
        taxa_lotacao = area_pastagem / consumo_diario_por_animal
        
        return taxa_lotacao
    except ValueError:
        return "Erro: Insira valores válidos para a área da pastagem e o consumo diário por animal."

# Interface de usuário
print("Calculadora de Taxa de Lotação em Pastagens")
print("-------------------------------------------")

area_pastagem = input("Informe a área da pastagem (em hectares): ")
consumo_diario_por_animal = input("Informe o consumo diário por animal (em kg): ")

resultado = calcular_taxa_lotacao(area_pastagem, consumo_diario_por_animal)

if isinstance(resultado, float):
    print(f"A taxa de lotação recomendada é de {resultado:.2f} animais por hectare.")
else:
    print(resultado)
