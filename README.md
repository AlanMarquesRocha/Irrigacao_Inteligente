# Irrigação Inteligente com Arduino e Tinkercad

## Descrição

Este projeto demonstra a criação de um sistema de irrigação automatizado, simulado no Tinkercad Circuits, usando Arduino UNO. O sistema monitora a umidade do solo e a temperatura ambiente, controla uma bomba via PWM com soft-start, exibe informações em um display LCD 16×2 e emite alerta sonoro quando a temperatura ultrapassa um limite definido.

---

## Funcionalidades

- Leitura de umidade do solo via sensor analógico (A2)  
- Medição de temperatura com sensor TMP36 (A3)  
- Controle da bomba (motor) por PWM com soft-start para reduzir picos de corrente  
- Alerta sonoro (piezo) acionado quando a temperatura ≥ 25 °C  
- Exibição de dados no display LCD 16×2  
- Splash screen “UNINTA” por 5 segundos no boot  

---

## Estrutura do Repositório

```bash
/                  # raiz do projeto
│
├── code/          # sketch Arduino (.ino)
│   └── Irrigacao_Inteligente.ino
│
├── tinkercad/     # exportações e captura de tela do circuito Tinkercad
│   └── circuito.png
│
└── READM.md       # este arquivo
```

---

## Pré-requisitos

- Arduino UNO (ou compatível)  
- Arduino IDE instalada (versão mínima 1.8.x)  
- Biblioteca [LiquidCrystal](https://www.arduino.cc/reference/pt/language/libraries/liquidcrystal/)  
- Acesso ao Tinkercad Circuits (opcional para simulação)  

---

## Instalação e Uso

1. **Clone** este repositório:  
   ```bash
   git clone https://github.com/SEU_USUARIO/irrigacao-inteligente.git
   ```

2. **Abra** o Arduino IDE e carregue o sketch `Irrigacao_Inteligente.ino` na pasta `code/`.

3. **Conecte** o Arduino ao computador via USB.

4. **Monte** o circuito conforme o diagrama em `tinkercad/circuito.png` ou seguindo as instruções:  
   - TMP36 → A3  
   - Sensor de umidade → A2  
   - LCD 16×2 → pinos 12, 11, 5, 4, 3, 2  
   - Piezo → D10  
   - Bomba (motor) → D6 (PWM)  
   - GND comum a todos os módulos  

5. **Selecione** a porta serial correta e a placa “Arduino Uno” no menu **Ferramentas**.

6. **Envie** o sketch para o Arduino.

7. **Observe** o splash screen “UNINTA” por 5 segundos e, em seguida, o sistema iniciará a leitura de sensores e controle de irrigação.

---

## Contribuições

Contribuições são bem-vindas! Abra _issues_ ou _pull requests_ para melhorias, correções e novas funcionalidades.

---

## Licença

Este projeto está licenciado sob a **Licença MIT**. Consulte o arquivo [LICENSE](LICENSE) para mais detalhes.
