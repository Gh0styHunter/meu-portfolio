# Wireshark

**Descrição:**  
Wireshark é um analisador de protocolos de rede que captura e permite inspecionar pacotes em tempo real ou a partir de arquivos de captura (pcap). Útil para análise de tráfego, investigação de incidentes e entendimento de protocolos.

---

## Funcionalidades principais
- Captura de pacotes em interfaces de rede  
- Decodificação de centenas de protocolos (HTTP, DNS, TLS, TCP, UDP, etc.)  
- Filtros de captura e exibição (BPF / display filters)  
- Estatísticas de conversas, protocolos e fluxo de dados  
- Reassembly de streams e reconstrução de sessões HTTP

---

## Filtros / Comandos úteis (teórico)
- Filtro de captura: `tcp port 80 and host 10.0.0.1`  
- Filtro de exibição: `http.request.method == "POST"`  
- Exportar objetos HTTP: `File → Export Objects → HTTP`  
- Salvar em pcap/pcapng para análise posterior

---

## Exemplos de uso teórico
- Capturar tráfego durante um teste para validar se credenciais foram transmitidas em texto claro.  
- Analisar handshake TLS para checar versões e ciphers negociados.

---

## Boas práticas / Observações
- Use filtros para reduzir volume de dados coletados.  
- Redija no relatório apenas evidências relevantes e apresente sempre contexto (quem, quando, como).  
- Trate PCAPs como evidência sensível — cuidado ao armazenar/compartilhar.

---

## Observações legais
- Captura de tráfego sem consentimento pode expor dados sensíveis — sempre ter autorização e seguir políticas de privacidade.
