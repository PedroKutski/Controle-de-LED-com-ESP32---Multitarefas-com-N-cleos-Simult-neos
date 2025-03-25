💡 Controle Paralelo de LED e Botão no ESP32
Este projeto demonstra o uso de multitarefa no ESP32 com FreeRTOS, onde duas tarefas trabalham em paralelo: uma para piscar um LED e outra para monitorar um botão. Essa aplicação prática ilustra conceitos fundamentais de concorrência e controle de tarefas em microcontroladores, sendo uma excelente ferramenta educativa e base para sistemas embarcados interativos. 🚀

📌 Visão Geral
Multitarefa com FreeRTOS: Utilização de duas tarefas distintas rodando em núcleos separados do ESP32.

Controle de LED: Uma tarefa pisca o LED conectado ao pino 2, demonstrando operações de saída digital.

Monitoramento de Botão: Outra tarefa monitora o botão (pino 0) para pausar ou retomar o piscar do LED de forma dinâmica.

🔬 Desenvolvimento do Sistema
O código foi desenvolvido utilizando o ambiente Arduino para ESP32 e utiliza duas tarefas criadas com a API do FreeRTOS:

TaskBlink: Responsável por acender e apagar o LED com intervalos de 500 ms. Esta tarefa opera no núcleo 0 e verifica a variável pauseBlink para saber se deve pausar o piscar.

TaskMonitor: Responsável por monitorar o estado do botão, que alterna a variável pauseBlink ao ser pressionado. Essa tarefa roda no núcleo 1 e implementa debounce para evitar leituras errôneas.

A separação das funções em tarefas distintas permite uma resposta rápida e eficiente, mesmo quando o sistema realiza múltiplas operações simultaneamente. 🎯

🛠️ Componentes Utilizados
ESP32: Microcontrolador com suporte a multitarefa e conectividade Wi-Fi/Bluetooth.

LED: Conectado ao pino 2, utilizado para demonstração visual.

Botão: Conectado ao pino 0 (boot), utilizado para pausar/retomar o piscar do LED.

Ambiente de Desenvolvimento Arduino: Para programação e upload do código.

🚀 Execução
Configuração: Certifique-se de que o ESP32 esteja devidamente configurado no Arduino IDE e que os pinos correspondam ao hardware utilizado.

Upload do Código: Carregue o código para o ESP32.

Teste: Ao iniciar, o LED pisca a cada 500 ms. Pressione o botão para pausar ou retomar o piscar do LED.

🔍 Resultados Obtidos
Controle Dinâmico: O LED pisca de forma contínua até que o botão seja pressionado, demonstrando o controle em tempo real através de multitarefa.

Resposta Imediata: A utilização de FreeRTOS permite que o sistema responda imediatamente à interação do usuário, sem interrupções na execução de outras tarefas.

💡 Melhorias Futuras
🔹 Aprimoramento do Debounce: Refinar a lógica de debounce para garantir uma resposta ainda mais precisa na leitura do botão.
🔹 Integração de Mais Sensores: Expandir o sistema para incluir sensores adicionais (por exemplo, sensores de luminosidade ou temperatura) e criar novas tarefas de monitoramento.
🔹 Feedback Visual: Implementar um display ou LEDs adicionais para fornecer feedback sobre o estado das tarefas e interações do sistema.

📜 Licença
Este projeto é de código aberto e está licenciado sob a MIT License. Sinta-se à vontade para explorar, modificar e aprimorar! 🎉

