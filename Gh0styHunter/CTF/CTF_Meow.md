# 📑 Capture The Flag – HTB Meow

**Plataforma:** Hack The Box  
**Máquina:** Meow (Ponto de Partida)  
**IP:** 10.129.34.76  
**Data:** 07/09/2025  

## 🔎 Reconhecimento
- Ferramentas utilizadas: ping, nmap, telnet
- Notas teóricas: Host respondeu, porta 23/tcp aberta (Telnet)

## ⚔️ Exploração
- Serviço vulnerável: Telnet
- Login root sem senha (simulado)

## 📂 Pós-exploração
- Diretório da flag: `/root/flag.txt`
- Comando: `cat /root/flag.txt`

## 🏆 Flag
b40abdfe23665f766f9c61ecba8a4c19


## ✅ Conclusão
- Vulnerabilidade: Telnet sem senha para root
- Impacto: Acesso root total
- Mitigação: Desabilitar Telnet, usar SSH, autenticação forte
