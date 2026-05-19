# HTB Meow – Notas
Data: 07/09/2025
Plataforma: Hack The Box
Máquina: Meow

## 🔎 Reconhecimento
- Ferramentas: ping, nmap, telnet
- Descobertas: Porta 23/tcp aberta (Telnet)

## ⚔️ Exploração
- Serviço vulnerável: Telnet
- Comando: `telnet <IP>` → login root sem senha (simulado)

## 📂 Pós-exploração
- Diretório da flag: /root/flag.txt
- Comando para visualizar: `cat /root/flag.txt`

## 📝 Observações
- Exploração de Telnet inseguro
- Documentação prática de pentest
