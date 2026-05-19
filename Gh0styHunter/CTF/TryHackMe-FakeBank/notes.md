# TryHackMe FakeBank – Notas
Data: 10/09/2025
Plataforma: TryHackMe
Lab: FakeBank

## 🔎 Reconhecimento
- Ferramenta: Gobuster
- Objetivo: Descobrir diretórios ocultos e páginas administrativas
- Comando utilizado: `gobuster -u http://fakebank.thm -w wordlist.txt dir`
- Resultados encontrados:
  - /images (Status 301)
  - /bank-transfer (Status 200)

## ⚔️ Exploração
- Página vulnerável: /bank-transfer
- Ação: Transferência de fundos entre contas (ambiente seguro e simulado)
- Comando / Navegação: Inserir endereço `/bank-transfer` no navegador

## 📝 Observações
- Descoberta de diretórios ocultos via força bruta
- Acesso não autorizado a funcionalidade administrativa (apenas em laboratório seguro)
- Documentação completa do processo
