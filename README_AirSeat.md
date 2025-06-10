# ✈️ AirSeat – Sistema de Reserva de Assentos em Aviões

Este é um projeto simples em C++ que simula a reserva de assentos em uma aeronave, divididos em duas classes: **Econômica** e **Executiva**.

---

## 🧩 Funcionalidades

- Exibição visual da planta de assentos
- Reserva de assento por número e letra
- Validação de disponibilidade
- Restrição de poltronas conforme o tipo de passagem
- Loop contínuo até o usuário decidir sair

---

## 🎮 Como usar

1. Compile o código:
```bash
g++ src/main.cpp -o airseat
```

2. Execute o programa:
```bash
./airseat
```

3. Siga as instruções no terminal:
   - Escolha tipo de passagem: `E` (Econômica) ou `X` (Executiva)
   - Escolha linha e poltrona (ex: `5 B`)
   - Continue ou finalize a qualquer momento

---

## 🧠 Estrutura do Código

- **`reserva[10][6]`**: matriz 2D que representa os assentos (10 fileiras, 6 poltronas A-F)
- **`exibirPlanta()`**: exibe o avião com marcação dos assentos livres ou reservados
- **`reservarAssento()`**: realiza a lógica de reserva conforme tipo da passagem
- **`main()`**: laço principal de interação com o usuário

---

## 🛫 Regras de Assento

- Assentos `A` e `F` são **exclusivos da classe Executiva**
- Classe Econômica pode escolher `B`, `C`, `D` ou `E`
- Se o assento já estiver ocupado, o usuário é alertado

---

## 📁 Arquivo principal

- `src/main.cpp`

---

## 📜 Licença

Este projeto é livre para uso educacional. Para uso comercial, recomenda-se adicionar uma [LICENÇA](https://choosealicense.com).

---

Desenvolvido para fins didáticos.
