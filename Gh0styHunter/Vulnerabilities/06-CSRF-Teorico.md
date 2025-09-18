# Vulnerabilidade: Cross-Site Request Forgery (CSRF) – Teórica
**Data:** 17/09/2025  
**Plataforma:** Teórica  
**Lab:** Lab-Teórico-CSRF  

## 🔎 Descrição
Falha que permite a um atacante induzir um usuário autenticado a executar ações não desejadas em um aplicativo web.

## ⚔️ Exploração (teórica)
- Criar formulário ou link malicioso que envia requisições em nome do usuário  
- Teste de endpoints críticos como transferência de fundos ou alteração de dados  

## 📂 Impacto
- Execução de ações não autorizadas por usuários legítimos
- Possível alteração de dados ou transações não intencionais  

## 🛡 Mitigação
- Implementar tokens anti-CSRF
- Validação de referer/header
- Requerer reautenticação para ações críticas

## 🛠 Ferramentas utilizadas
- Navegador, Burp Suite (teórico)
