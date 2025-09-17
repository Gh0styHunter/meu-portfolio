# gobuster

**Descrição:**  
Gobuster é uma ferramenta de enumeração por brute-force utilizada para encontrar diretórios, arquivos e subdomínios ocultos em aplicações web. É rápida e baseada em wordlists.

---

## Funcionalidades principais
- Enumeração de diretórios e arquivos (dir mode)  
- Enumeração de subdomínios (vhost/subdomain mode)  
- Força bruta de nomes de diretório/arquivo com wordlists  
- Suporte a filtros por status code e size

---

## Opções / flags úteis (teórico)
- `dir` — modo diretório (`gobuster dir -u ...`).  
- `dns` — modo DNS/subdomain.  
- `-u` — URL alvo.  
- `-w` — wordlist.  
- `-t` — threads.  
- `-s` — status codes a considerar como positivos (ex.: `-s 200,301`).  
- `-x` — extensões a testar (ex.: `-x php,html`).

---

## Exemplos de uso teórico
1) **Enumeração de diretórios**
gobuster dir -u https://exemplo.com/ -w /wordlists/common.txt -t 50 -s 200,301

markdown
Copiar código
2) **Enumeração de subdomínios**
gobuster dns -d exemplo.com -w /wordlists/subdomains.txt

---

## Boas práticas / Observações
- Escolha wordlists adequadas ao escopo e ao idioma do alvo.  
- Filtre por status codes e tamanho para reduzir falsos positivos.  
- Evite paralelismo extremo em ambientes sensíveis.

---

## Observações legais
- Enumeração sem autorização pode gerar tráfego indesejado e é proibida — sempre escopo autorizado.
