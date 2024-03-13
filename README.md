import math

def calcular_area_circulo(raio):
    """
    Calcula a área de um círculo com base no raio fornecido.

    Parâmetros:
    raio (float): O raio do círculo.

    Retorna:
    float: A área do círculo.
    """
    return math.pi * raio ** 2

def obter_raio_usuario():
    """
    Solicita ao usuário que insira o raio e valida a entrada.

    Retorna:
    float: O raio fornecido pelo usuário.
    """
    while True:
        try:
            raio = float(input("Digite o raio do círculo: "))
            if raio <= 0:
                raise ValueError("O raio deve ser um número positivo maior que zero.")
            return raio
        except ValueError as erro:
            print(f"Entrada inválida: {erro}")

def exibir_area_circulo(raio, area):
    """
    Exibe a área do círculo com base no raio fornecido.

    Parâmetros:
    raio (float): O raio do círculo.
    area (float): A área do círculo.
    """
    print(f"A área do círculo com raio {raio} é {area:.2f}")

def main():
    try:
        raio = obter_raio_usuario()
        area_do_circulo = calcular_area_circulo(raio)
        exibir_area_circulo(raio, area_do_circulo)
    except Exception as e:
        print(f"Ocorreu um erro ao calcular a área: {e}")

if __name__ == "__main__":
    main()
