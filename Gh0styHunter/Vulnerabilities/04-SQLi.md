# Vulnerabilidade: SQL Injection
**Data:** 17/09/2025  
**Plataforma:** DVWA 
**Lab:** Lab-Teórico-SQLi  

## 🔎 Descrição
Falha em parâmetros que interagem com o banco de dados, permitindo injeção de comandos SQL.

## ⚔️ Exploração (teórica)
- Testes em parâmetros GET/POST: `' OR '1'='1`  
- Tipos estudados: Blind SQLi, Error-based SQLi

## 📂 Impacto
- Acesso não autorizado a dados
- Possível alteração ou exclusão de registros

## 🛡 Mitigação
- Prepared statements / ORM
- Validação e sanitização de inputs

## 🛠 Ferramentas utilizadas
- SQLMap, navegador, Burp Suite
