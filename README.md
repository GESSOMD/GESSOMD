
def calcular_area_circulo(raio):
    """
    Calcula a área de um círculo com base no raio.

    Args:
        raio (float): O raio do círculo.

    Returns:
        float: A área do círculo.
    """
    try:
        # Verifica se o raio é um número positivo
        if raio <= 0:
            raise ValueError("O raio deve ser um número positivo.")
        
        # Importa a constante pi do módulo math
        from math import pi
        
        # Calcula a área usando a fórmula: pi * raio^2
        area = pi * raio ** 2
        
        return area
    except ValueError as e:
        print(f"Erro: {e}")
        return None

# Exemplo de uso
raio_usuario = float(input("Digite o raio do círculo: "))
area_resultante = calcular_area_circulo(raio_usuario)

if area_resultante is not None:
    print(f"A área do círculo de raio {raio_usuario:.2f} é {area_resultante:.2f}")
