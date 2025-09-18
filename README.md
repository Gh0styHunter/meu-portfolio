# 💻 Portfolio de Pentest – Gh0styHunter

Olá! Este portfolio demonstra meu aprendizado prático e teórico em testes de intrusão (Pentest), realizado em ambientes seguros como Hack The Box e TryHackMe. Contém minhas experiências em CTFs, ferramentas utilizadas, vulnerabilidades encontradas e relatórios simulando um pentest profissional.

---

## 🏆 Experiências em CTFs / Labs

### 1. HTB – Meow
**Plataforma:** Hack The Box  
**Máquina:** Meow (Ponto de Partida)  
**IP:** 10.129.34.76  
**Data:** 07/09/2025  

#### 🔎 Reconhecimento
- Ferramentas usadas: ping, Nmap, Telnet  
- Host respondeu ao ping  
- Porta 23/tcp aberta (Telnet)  

#### ⚔️ Exploração
- Serviço vulnerável: Telnet  
- Login root sem senha (simulado)  

#### 📂 Pós-exploração
- Diretório da flag: `/root/flag.txt`  
- Comando usado: `cat /root/flag.txt`  

#### 🏅 Flag
b40abdfe23665f766f9c61ecba8a4c19  

#### ✅ Conclusão
- Vulnerabilidade: Telnet sem senha para root  
- Impacto: Acesso root total  
- Mitigação sugerida: Desabilitar Telnet, usar SSH, autenticação forte  

---

### 2. TryHackMe – FakeBank
**Plataforma:** TryHackMe  
**Máquina:** FakeBank  
**Data:** 10/09/2025  

#### 🔎 Reconhecimento
- Ferramenta usada: Gobuster  
- Diretórios encontrados: `/images` (301), `/bank-transfer` (200)  

#### ⚔️ Exploração
- Página vulnerável: `/bank-transfer`  
- Ação realizada: Transferência simulada de US$ 2.000 da conta 2276 para a conta 8881  

#### 📂 Pós-exploração
- Navegador acessando `/bank-transfer`  
- Saldo atualizado evidenciando exploração ética  

#### 🏅 Flag
BANK-HACKED  

#### ✅ Conclusão
- Vulnerabilidade: Página administrativa acessível sem restrições  
- Impacto: Possível transferência não autorizada de fundos  
- Mitigação sugerida: Restringir acesso, autenticação forte, validação de permissões  

---

## 🛠 Ferramentas Conhecidas

| Categoria | Ferramenta | Nível | Observações |
|-----------|------------|-------|------------|
| Recon / Subdomínios | Amass | Intermediário | Recon ativo e passivo |
| Recon / Subdomínios | Subfinder | Intermediário | Enumeração passiva |
| Recon / Rede | Nmap | Intermediário | Mapeamento de rede e portas |
| Recon / Rede | Wireshark | Básico | Captura e análise de pacotes |
| Web / APIs | FFUF | Intermediário | Fuzzing de diretórios e parâmetros |
| Web / APIs | Burp Suite | Básico/Intermediário | Análise e exploração de aplicações web |
| Brute-force / Senhas | Hydra | Básico/Intermediário | Ataques multi-protocolo |
| Web / APIs | Gobuster | Básico | Enumeração de diretórios e subdomínios |

---

## ⚠️ Vulnerabilidades Estudadas
- Telnet sem senha (HTB Meow) – Acesso root  
- Página administrativa sem restrição (FakeBank) – Transferência não autorizada  

---

## 📄 Observações Profissionais
- Experiência prática em **CTFs e laboratórios virtuais seguros**  
- Conhecimento aplicado em **ferramentas de recon, fuzzing, brute-force e web/mobile pentest**  
- Relatórios documentados com **flags, comandos e conclusões**, simulando workflow de pentest profissional  
- Motivado para crescer em **mobile pentest, web scanning avançado e documentação de pentest**

---

## 📜 Certificados

- ![Selo Cisco]([link-para-imagem-do-selo](https://www.credly.com/badges/5fb44fac-9253-4310-aec3-07ee40f2a98b/public_url)) Cisco CyberOps Associate – Cisco – 2025  
- Fundamentos de Python – Cisco – 2024  
- Conceitos Básicos de Redes – Cisco – 2024  
- Introdução ao Pentest – Desec/Solyd – 2025  
- CCNA – Cisco – 2024

---

## 📌 Contato
- Name: Jackson
- Nickname: Gh0styHunter  
- Email: jacksonfelixbertolb@email.com  /  gh0styhunter.bugbounter@gmail.com
- LinkedIn: linkedin.com/in/gh0styhunter  
- GitHub: github.com/gh0styhunter
