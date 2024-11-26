# N-meros-primos
Determinar los números primos hasta un natural 'n'.
def es_primo(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

def encontrar_primos(hasta):
    return [n for n in range(2, hasta + 1) if es_primo(n)]

# Solicitar el número x al usuario
x = int(input("Introduce un número hasta el cual buscar números primos: "))
primos = encontrar_primos(x)

print(f"Números primos hasta {x}: {primos}")