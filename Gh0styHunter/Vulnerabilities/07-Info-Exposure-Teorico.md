# Vulnerabilidade: Sensitive Data Exposure – Teórica
**Data:** 17/09/2025  
**Plataforma:** Teórica  
**Lab:** Lab-Teórico-Info-Exposure  

## 🔎 Descrição
Falha que expõe dados sensíveis de usuários ou sistemas (senhas, tokens, PII) por falta de criptografia ou má configuração.

## ⚔️ Exploração (teórica)
- Interceptação de tráfego HTTP sem TLS  
- Inspeção de headers ou arquivos mal protegidos  
- Testes de endpoints para verificar exposição de dados críticos  

## 📂 Impacto
- Vazamento de informações confidenciais
- Possível roubo de identidade ou acesso não autorizado

## 🛡 Mitigação
- Criptografia TLS/SSL para transmissão
- Criptografia de dados sensíveis em repouso
- Controle de acesso adequado

## 🛠 Ferramentas utilizadas
- Wireshark, Burp Suite (teórico)
