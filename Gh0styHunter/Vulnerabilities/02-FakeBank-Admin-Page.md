# Vulnerabilidade: Página Administrativa sem Restrição
**Data:** 10/09/2025  
**Plataforma:** TryHackMe  
**Lab:** FakeBank  

## 🔎 Descrição
Página de transferência bancária acessível sem autenticação. Diretório oculto encontrado via Gobuster: `/bank-transfer`.

## ⚔️ Exploração
- Inserir URL `/bank-transfer` no navegador
- Funcionalidade de transferência disponível mesmo sem credenciais

## 📂 Impacto
- Acesso a funções administrativas
- Possível manipulação de dados de contas (em ambiente seguro)

## 🛡 Mitigação
- Restringir acesso a páginas administrativas
- Implementar autenticação e autorização
- Monitoramento de atividades críticas

## 🛠 Ferramentas utilizadas
- Gobuster
