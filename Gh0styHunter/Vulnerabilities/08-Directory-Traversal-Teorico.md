# Vulnerabilidade: Directory Traversal – Teórica
**Data:** 17/09/2025  
**Plataforma:** Teórica  
**Lab:** Lab-Teórico-Directory-Traversal  

## 🔎 Descrição
Falha que permite acessar arquivos sensíveis fora do diretório permitido via manipulação de path.

## ⚔️ Exploração (teórica)
- Teste de paths: `../../etc/passwd`  
- Objetivo: acessar arquivos críticos do sistema

## 📂 Impacto
- Leitura de arquivos sensíveis do servidor

## 🛡 Mitigação
- Validação de paths
- Uso de whitelist de arquivos permitidos

## 🛠 Ferramentas utilizadas
- Navegador, Burp Suite (teórico)
