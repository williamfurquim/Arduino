Projeto simples utilizando ESP32 e a biblioteca WiFi.h para criar um servidor web local capaz de controlar dois pinos GPIO pelo navegador.

👉 VISÃO GERAL
O ESP32 opera em modo Access Point (AP), criando sua própria rede Wi-Fi. Ao conectar-se a essa rede, o usuário acessa uma página web hospedada no próprio microcontrolador, onde é possível ligar e desligar dois LEDs conectados aos pinos 16 e 17.

👉 FUNCIONAMENTO
- O ESP32 cria uma rede Wi-Fi própria (WiFi.softAP)
- Um servidor HTTP roda na porta 80
- Ao acessar o IP do dispositivo, uma página HTML é exibida
- Botões enviam requisições GET:
/16/on e /16/off
/17/on e /17/off
- O ESP32 interpreta a requisição e altera o estado dos GPIOs

👉 CONCEITOS UTILIZADOS
⏺️ REDE
- Modo Access Point
- Servidor HTTP com WiFiServer
- Comunicação cliente-servidor em rede local

⏺️ HARDWARE
- Controle de GPIO
- Manipulação digital de pinos
- Integração software + hardware

⏺️ INTERFACE
- Geração dinâmica de HTML
- Manipulação de requisições GET
