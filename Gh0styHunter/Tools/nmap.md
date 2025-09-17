# nmap

**Descrição:**  
Nmap (Network Mapper) é uma ferramenta de auditoria e descoberta de rede usada para mapear hosts, portas, serviços e sistemas operacionais em uma rede. Muito usada em reconhecimento (recon) durante testes de segurança.

---

## Funcionalidades principais
- Descoberta de hosts ativos (host discovery)  
- Varredura de portas (port scanning)  
- Detecção de versão de serviços (-sV)  
- Identificação de sistema operacional (OS detection)  
- Varreduras avançadas (SYN scan, UDP scan, TCP connect)  
- Scripts NSE (Nmap Scripting Engine) para automação de checagens específicas

---

## Opções / flags úteis (teórico)
- `-sS` — TCP SYN scan (stealth).  
- `-sT` — TCP connect scan.  
- `-sU` — UDP scan.  
- `-sV` — detecta versão dos serviços.  
- `-O` — tenta identificar SO (OS detection).  
- `-A` — ativa detecção de versão, scripts NSE e identificação de SO.  
- `-p` — especifica portas ou ranges (`-p 1-65535` ou `-p 80,443`).  
- `-Pn` — não faz host discovery (trata host como up).  
- `-oN`, `-oX`, `-oG` — formatos de output (normal, XML, grepable).  
- `--script` — rodar scripts NSE (ex.: `--script vuln`).

---

## Exemplos de uso teórico
1) **Varredura de serviços e versões**
nmap -sS -sV -p 1-1000 10.10.10.10 -oN nmap_services.txt

lua
Copiar código
2) **Detecção de SO e serviços (mais agressivo)**
nmap -A 10.10.10.0/24 -oN nmap_full.txt

markdown
Copiar código
3) **Rodar script específico (vuln)**
nmap -p 445 --script vuln 192.168.1.100

yaml
Copiar código

---


---

## Boas práticas / Observações
- Use scans menos ruidosos em ambientes produtivos para não disparar IDS/IPS.  
- Documente portas e serviços detectados para inclusão em relatórios.  
- Combine `-sV` com scripts NSE para identificação de vulnerabilidades conhecidas.  
- Sempre obtenha autorização para varreduras em redes que não são suas.

---

## Observações legais
- Varredura de rede sem consentimento é considerada atividade intrusiva — sempre ter autorização por escrito (escopo).

