# Ponderada-01-Modulo-4
## Parte 1
```
// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);  // turn the LED on (HIGH is the voltage level)
  delay(1000);                      // wait for a second
  digitalWrite(LED_BUILTIN, LOW);   // turn the LED off by making the voltage LOW
  delay(1000);                      // wait for a second
}
```
Video de funcionamento disponível no repositório

## Parte 2
```
// Defina os pinos do LED RGB
const int redPin = 9;   // Pino do LED vermelho
const int greenPin = 10; // Pino do LED verde
const int bluePin = 11;  // Pino do LED azul

// Função para definir a cor do LED RGB
void setColor(int redValue, int greenValue, int blueValue) {
  analogWrite(redPin, redValue);
  analogWrite(greenPin, greenValue);
  analogWrite(bluePin, blueValue);
}

void setup() {
  // Defina os pinos como saídas
  pinMode(redPin, OUTPUT);
  pinMode(greenPin, OUTPUT);
  pinMode(bluePin, OUTPUT);
}

void loop() {
  // Cor Vermelha
  setColor(255, 0, 0);
  delay(1000); // Piscar por 1 segundo

  // Cor Verde
  setColor(0, 255, 0);
  delay(1000); // Piscar por 1 segundo

  // Cor Azul
  setColor(0, 0, 255);
  delay(1000); // Piscar por 1 segundo

  // Cor Amarela (vermelho + verde)
  setColor(255, 255, 0);
  delay(1000); // Piscar por 1 segundo

  // Cor Ciano (verde + azul)
  setColor(0, 255, 255);
  delay(1000); // Piscar por 1 segundo

  // Cor Magenta (vermelho + azul)
  setColor(255, 0, 255);
  delay(1000); // Piscar por 1 segundo

  // Cor Branca (vermelho + verde + azul)
  setColor(255, 255, 255);
  delay(1000); // Piscar por 1 segundo

  // Apagar o LED
  setColor(0, 0, 0);
  delay(1000); // Apagado por 1 segundo
}
```
