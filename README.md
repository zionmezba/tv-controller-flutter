# Slide Control with Flutter and NodeJS via WebSocket

This project allows you to control one Slideshow (or any other software) at a distance, simulating movements of mouse and keyboard through a Flutter app connected via WebSocket to a NodeJS server. The Flutter app uses the sensors of accelerometer and gyroscope from the device to detect movements, providing a fluid experience to navigate between slides or perform actions remotely.

## Functionalities

- Remote control of slideshows.
- Simulation of mouse movements and keyboard actions.
- Real-time connection between the NodeJS and app Flutter via WebSocket.
- Using sensors of accelerometer and gyroscope to detect movements.
- Ideal for those who need to control presentations while away from the device.

## Requirements

### Server (NodeJS)

- Node.js (v14.x ou superior)
- WebSocket
- Libraries for mouse and keyboard simulation

### Application (Flutter)

- Flutter SDK (v2.0 or superior)
- Plugin `sensors_plus` for access to device sensors
- WebSocket for communication with the server

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/cl0v/tv-controller
cd tv-controller
```

### 2. NodeJS Server Configuration

Install NodeJS dependencies:

```bash
cd nodejs
npm install
```

### 3. Launch WebSocket Server

```bash
npm run start
```

### 4. Flutter App Configuration

Certifique-se de que o Flutter está instalado e as dependências estão configuradas:

```bash
cd flutter
flutter pub get
```

### 5. Run the Flutter App

Connect a device or use the emulator to run the app:

```bash
flutter run
```

## How It Works

### NodeJS Server

The NodeJS server receives commands from the Flutter application via WebSocket and simulates mouse and keyboard actions on the host system. Depending on the data sent by the accelerometer and gyroscope, the server performs the following actions:

- **Mouse Movement**: Based on the inclination and movement of the device.
- **Advance/Retrovers of Slide:**: Using device-specific gestures or tilts to send keyboard commands (e.g., keys  `seta para esquerda` e `seta para direita`).

### App Flutter

The application collects the motion data through the sensors (accelerometer/gyroscope) and sends this data to the NodeJS server via WebSocket. The server interprets this data and turns it into mouse/keyboard commands.

## Usage Examples

### Movement to the Left/Right

- Tilt the device to the left to simulate pressing the left arrow.
- Tilt the device to the right to simulate pressing the arrow to the right.

### Mouse Movement

- Smooth movements on the shaft X or Y gyroscope can be used to move the mouse cursor.

## Capturas de tela
![Exemplo de uso](/screenshots/output.gif)

## Technologies Used

- **NodeJS**: To manage the WebSocket server and control mouse and keyboard actions.
- **WebSocket**: This is for real-time communication between the server and the Flutter app.
- **Flutter**: To capture data from the accelerometer and gyroscope and send it to the server.
- **sensors_plus**: A Flutter plugin is used to access sensors like an accelerometer and gyroscope.
- **robotjs**: NodeJS library to simulate mouse and keyboard actions.

## Contribuindo

1. Make a fork of the project
2. Create a branch for your feature (`git checkout -b feature/nova-feature`)
3. Commit your changes (`git commit -m 'Adiciona nova feature'`)
4. Push to the branch (`git push origin feature/nova-feature`)
5. Open a Pull Request

## Buy me a Coffee

Give a ⭐️ if this project helped you!

<a href="https://www.patreon.com/cl0v">
  <img src="https://c5.patreon.com/external/logo/become_a_patron_button@2x.png" width="160">
</a>

## Licença

Este projeto está licenciado sob a [Licença Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0).

## Contato

Caso tenha dúvidas ou sugestões, sinta-se à vontade para abrir uma **issue** ou entrar em contato pelo [LinkedIn](https://www.linkedin.com/in/marcelo-fernandes-viana-a49311329/).

### Estrutura do Projeto:

- **nodejs/**: Contém o código do servidor NodeJS.
- **flutter/**: Contém o código do aplicativo Flutter.
