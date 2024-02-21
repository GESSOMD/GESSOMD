Peço desculpas na fórmula 
 def distancia_centro_ponto(raio, x, y):
    """
    Calcula a distância entre o centro de um círculo (na origem) e um ponto (x, y).

    Args:
        raio (float): O raio do círculo.
        x (float): A coordenada x do ponto.
        y (float): A coordenada y do ponto.

    Returns:
        float: A distância entre o centro do círculo e o ponto.
    """
    try:
        # Verifica se o raio é um número positivo
        if raio <= 0:
            raise ValueError("O raio deve ser um número positivo.")
        
        # Calcula a distância usando a fórmula correta: sqrt(x^2 + y^2)
        distancia = (x**2 + y**2)**0.5
        
        return distancia
    except ValueError as e:
        print(f"Erro: {e}")
        return None

# Exemplo de uso
raio_usuario = float(input("Digite o raio do círculo: "))
x_usuario = float(input("Digite a coordenada x do ponto: "))
y_usuario = float(input("Digite a coordenada y do ponto: "))

distancia_resultante = distancia_centro_ponto(raio_usuario, x_usuario, y_usuario)

if distancia_resultante is not None:
    print(f"A distância entre o centro do círculo e o ponto ({x_usuario}, {y_usuario}) é: {distancia_resultante:.2f}")
