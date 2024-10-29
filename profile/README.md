
# 🎉 Bem-vindo ao Projeto de Captive Portal para ESP32 e NodeMCU ESP8266! 🌐

![Design sem nome (1)](https://github.com/user-attachments/assets/6660a460-5d1c-4d2a-b6db-23345ae37fad)


### Acesso rapido
- [Projeto ESP32 -LORATTGO sem HTTPS](https://github.com/PIC-projeto-Humanidades/captive-portal-micro/tree/esp32-with-http)
- [Projeto ESP8266 - Nodemcu com HTTPS](https://github.com/PIC-projeto-Humanidades/captive-portal-micro/tree/esp8266-with-https)

Este repositório traz uma solução acessível para implementar um sistema de captive portal em placas de baixo custo, como ESP8266 e ESP32. O projeto é voltado para quem deseja controlar o acesso em redes Wi-Fi de forma eficiente e econômica, ideal para comunidades remotas ou locais com infraestrutura limitada. 🌍 Aproveite para explorar e utilizar essa tecnologia para promover a inclusão digital e facilitar o acesso seguro à internet em qualquer lugar! 🚀

---

## Captive Portal para ESP32 e NodeMCU ESP8266 🔒

Este projeto visa implementar um sistema de captive portal de baixo custo, compatível com placas genéricas NodeMCU ESP8266 e ESP32. A solução replica funcionalidades básicas de gerenciamento de acesso comumente encontradas em roteadores corporativos, como autenticação e redirecionamento, permitindo o controle de acesso em redes Wi-Fi de forma simples e acessível. O projeto é ideal para ambientes com restrição de infraestrutura e locais de difícil acesso, como comunidades rurais e ribeirinhas. 🏞️

## 💡 Descrição do Projeto

Com o crescente uso de redes Wi-Fi e a necessidade de controle de acesso em locais públicos e corporativos, o captive portal se tornou uma ferramenta essencial para a segurança 🔐 e gestão de conectividade 📶. Esse sistema exige que os usuários passem por uma etapa de autenticação antes de obter acesso completo à rede, garantindo maior segurança e controle de uso.

Neste projeto, o captive portal foi implementado em microcontroladores ESP8266 e ESP32, dispositivos de baixo custo que suportam funcionalidades básicas de Wi-Fi e permitem a inclusão digital em regiões remotas. 🌎

## 🧭 Comportamento Esperado

1. **Mensagem de Boas-vindas**: Ao acessar o captive portal, o usuário é recebido com uma mensagem amigável, como:
   - "👋 Bem-vindo(a) à nossa rede! Conecte-se para acessar o conteúdo."
   - "Olá! 😃 Aproveite nosso acesso controlado à internet. Faça seu login para continuar. 🌐"
2. **Autenticação Direta**: O usuário insere suas credenciais e, ao autenticar, obtém acesso total à rede. 🔓
3. **Autenticação Indireta**: O usuário é redirecionado para uma página de registro, onde confirma sua presença. Em seguida, um botão é exibido para liberar o acesso com uma mensagem de boas-vindas, como:
   - "✅ Você está quase conectado! Clique abaixo para finalizar o processo."

## 🛠️ Tecnologias Utilizadas

- **C++**: Utilizado para implementação da lógica principal, gerenciando serviços de DNS e controle de conectividade Wi-Fi. 💻
- **HTML, CSS e JavaScript**: Para construção da interface gráfica, que permite interação com o usuário durante o processo de autenticação. 🎨
  
## 🗂️ Arquitetura do Sistema

O sistema foi dividido em camadas para melhor organização e modularidade 🧩:

- **Main**: Arquivos responsáveis pela inicialização do sistema e configuração dos serviços de DNS e Wi-Fi. 🚀
- **Controller**: Define as rotas e regras de redirecionamento, controlando o fluxo de autenticação. 🌐
- **Service**: Contém os serviços de suporte, como autenticação e redirecionamento. 🔄
- **Credentials**: Armazena informações de conectividade, como SSID e senha, além de dados de autenticação. 📑

## 🔍 Desafios e Considerações

### HTTP vs. HTTPS no Captive Portal

- **HTTP**: Facilita o redirecionamento de usuários sem necessidade de criptografia, otimizando a experiência do usuário 🕶️, sem sobrecarga de processamento ⚡.
- **HTTPS**: A implementação de HTTPS é limitada em dispositivos de baixo custo 🛠️ devido à falta de suporte nativo para certificados SSL/TLS confiáveis. Embora mais seguro 🔒, o HTTPS pode comprometer a performance e exige uma configuração complexa.

### ⚠️ HSTS e Limitações de Redirecionamento

Dispositivos modernos utilizam o protocolo HTTPS com HSTS (HTTP Strict Transport Security) 🔗, o que impede o redirecionamento HTTP em muitos casos. Isso é uma limitação em dispositivos NodeMCU e ESP32 que operam sem certificados SSL.

## 📈 Análise de Conectividade e Performance

Durante testes 🧪, observou-se um tempo médio de conexão inicial para ambos os dispositivos, com uma redução progressiva nos tempos de carregamento em conexões subsequentes. O NodeMCU demonstrou tempos mais rápidos na conexão inicial em comparação ao ESP32. Abaixo está um resumo dos resultados:

- **NodeMCU (HTTP)**: Conexão inicial rápida 🚀, com melhoria de performance em conexões subsequentes.
- **ESP32 (HTTP)**: Tempos de conexão semelhantes ao NodeMCU, mas com maior latência na primeira conexão. ⏱️
- **HTTPS**: Ambos os dispositivos apresentaram perda de performance significativa 📉 ao operar em HTTPS.

## 📋 Requisitos

- NodeMCU ESP8266 ou ESP32 📲
- Ambiente de desenvolvimento Arduino IDE ou PlatformIO 🛠️
- Conexão Wi-Fi para configuração do captive portal 📶

## 📖 Como Usar

1. Clone o repositório 📂
2. Configure as credenciais de rede no arquivo `Credentials` 🔐
3. Carregue o código na placa ESP8266 ou ESP32 📲
4. Conecte-se à rede Wi-Fi e acesse o captive portal através do navegador 🌐
5. A interface de autenticação mostrará uma mensagem de boas-vindas para guiar o usuário no processo de conexão 🎉

## 🤔 Considerações Finais

Este projeto oferece uma solução viável para o controle de acesso em redes Wi-Fi de baixo custo 💸, promovendo a inclusão digital em áreas remotas 🌍. Embora apresente limitações em ambientes com HTTPS, o captive portal em HTTP funciona de forma eficiente para controle e monitoramento de usuários. 

---

Desfrute do projeto e sinta-se à vontade para contribuir ou sugerir melhorias! 💡
