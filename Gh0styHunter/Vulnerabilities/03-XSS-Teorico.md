# Vulnerabilidade: Cross-Site Scripting (XSS)
**Data:** 17/09/2025  
**Plataforma:** DVWA
**Lab:** Lab-XSS  

## 🔎 Descrição
Falha de validação de inputs em campos web, permitindo execução de scripts no navegador do usuário.

## ⚔️ Exploração
- Payloads exemplo: `<script>alert(1)</script>`  
- Objetivo: execução de JavaScript não autorizado  
- Tipos estudados: Stored XSS, Reflected XSS

## 📂 Impacto
- Roubo de cookies e sessão
- Possível manipulação de DOM e phishing

## 🛡 Mitigação
- Sanitização de inputs
- Uso de Content Security Policy (CSP)

## 🛠 Ferramentas utilizadas
- Navegador
