# Vulnerabilidade: Insecure Direct Object Reference (IDOR) – Teórica
**Data:** 17/09/2025  
**Plataforma:** Teórica  
**Lab:** Lab-Teórico-IDOR  

## 🔎 Descrição
Falha de autorização que permite acessar ou modificar objetos (contas, arquivos, recursos) sem permissão adequada, alterando parâmetros na URL ou requests.

## ⚔️ Exploração (teórica)
- Modificação de IDs em URL ou API: `/account/12345` → `/account/12346`  
- Testes em GET/POST para verificar acesso não autorizado  

## 📂 Impacto
- Acesso ou alteração de dados de outros usuários
- Possível violação de privacidade ou integridade de informações  

## 🛡 Mitigação
- Verificação de autorização em cada request
- Controle de acesso baseado em funções (RBAC)
- Auditoria de logs

## 🛠 Ferramentas utilizadas
- Navegador, Burp Suite (teórico)
