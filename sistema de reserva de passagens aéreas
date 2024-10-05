#include <iostream>
#include <cctype>

using namespace std;

void exibirPlanta(char reserva[10][6]) {
    cout << "\nPlanta do Avião:\n";
    cout << "\t\t[A] [B] [C]\t[D] [E] [F]\n";
    for (int i = 0; i < 10; i++) {
        cout << "\t" << (i + 1) << "\t";
        for (int j = 0; j < 6; j++) {
            cout << "[" << reserva[i][j] << "] ";
            if (j == 2) {
                cout << "\t";
            }
        }
        cout << endl;
    }
}

void reservarAssento(char reserva[10][6], char tipoPassagem) {
    int linha, coluna;
    char poltrona;

    cout << "\nDigite a linha (1-10): ";
    cin >> linha;

    cout << "Digite a poltrona (A-F): ";
    cin >> poltrona;
    poltrona = toupper(poltrona);

    coluna = poltrona - 'A';

    if (tipoPassagem == 'E' && (poltrona == 'A' || poltrona == 'F')) {
        cout << "Assentos A e F são exclusivos para passageiros Executivos." << endl;
        reservarAssento(reserva, tipoPassagem); 
    } else if (reserva[linha - 1][coluna] == 'x') {
        cout << "A poltrona " << linha << poltrona << " já está reservada. Por favor, escolha outra." << endl;
        reservarAssento(reserva, tipoPassagem); 
    } else {
        reserva[linha - 1][coluna] = 'x';
        if (tipoPassagem == 'E' && (poltrona != 'A' && poltrona != 'F')) {
            cout << "Recomendamos os assentos A ou F para passageiros Executivos." << endl;
        }
        cout << "Assento reservado com sucesso!" << endl;
    }
}

int main() {
    const int NUM_LINHAS = 10;
    const int NUM_COLUNAS = 6;
    char reserva[NUM_LINHAS][NUM_COLUNAS] = {
        {' ', ' ', ' ', ' ', ' ', ' '},
        {' ', ' ', ' ', ' ', ' ', ' '},
        {' ', ' ', ' ', ' ', ' ', ' '},
        {' ', ' ', ' ', ' ', ' ', ' '},
        {' ', ' ', ' ', ' ', ' ', ' '},
        {' ', ' ', ' ', ' ', ' ', ' '},
        {' ', ' ', ' ', ' ', ' ', ' '},
        {' ', ' ', ' ', ' ', ' ', ' '},
        {' ', ' ', ' ', ' ', ' ', ' '},
        {' ', ' ', ' ', ' ', ' ', ' '}
    };

    char tipoPassagem;
    bool continuar = true;

    while (continuar) {
        exibirPlanta(reserva);

        cout << "Escolha o tipo de passagem (E - Econômico, X - Executivo): ";
        cin >> tipoPassagem;
        tipoPassagem = toupper(tipoPassagem);

        while (tipoPassagem != 'E' && tipoPassagem != 'X') {
            cout << "Tipo de passagem inválido. Por favor, digite E ou X." << endl;
            cin >> tipoPassagem;
            tipoPassagem = toupper(tipoPassagem);
        }

        reservarAssento(reserva, tipoPassagem);

        cout << "\nDeseja realizar outra reserva? (S/N): ";
        char resposta;
        cin >> resposta;
        resposta = tolower(resposta);

        if (resposta != 's') {
            continuar = false;
            cout << "Encerrando o sistema de reservas..." << endl;
        }
    }

    return 0;
}
