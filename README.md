#include <iostream>

class CNumber {
private:
    int num1;
    int num2;
    int num3;

public:
    // Constructor
    CNumber(int n1, int n2, int n3) {
        num1 = n1;
        num2 = n2;
        num3 = n3;
    }

    // Función para calcular el máximo de los 3 números
    int calcularMaximo() {
        int max = num1;
        if (num2 > max) {
            max = num2;
        }
        if (num3 > max) {
            max = num3;
        }
        return max;
    }

    // Función para calcular el mínimo de los 3 números
    int calcularMinimo() {
        int min = num1;
        if (num2 < min) {
            min = num2;
        }
        if (num3 < min) {
            min = num3;
        }
        return min;
    }

    // Función para calcular el promedio de los 3 números
    double calcularPromedio() {
        return (num1 + num2 + num3) / 3.0;
    }

    // Función para calcular la cantidad de elementos pares
    int contarPares() {
        int count = 0;
        if (num1 % 2 == 0) {
            count++;
        }
        if (num2 % 2 == 0) {
            count++;
        }
        if (num3 % 2 == 0) {
            count++;
        }
        return count;
    }

    // Función para calcular la cantidad de elementos impares
    int contarImpares() {
        return 3 - contarPares();
    }
};

int main() {
    // Ejemplo de uso
    CNumber numeros(5, 12, 7);

    std::cout << "Máximo: " << numeros.calcularMaximo() << std::endl;
    std::cout << "Mínimo: " << numeros.calcularMinimo() << std::endl;
    std::cout << "Promedio: " << numeros.calcularPromedio() << std::endl;
    std::cout << "Elementos pares: " << numeros.contarPares() << std::endl;
    std::cout << "Elementos impares: " << numeros.contarImpares() << std::endl;

    return 0;
}
