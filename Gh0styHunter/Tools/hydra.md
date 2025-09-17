# Hydra

**Descrição:**  
Hydra (THC-Hydra) é uma ferramenta de força-bruta multi-protocolo para testar autenticações em serviços como SSH, FTP, HTTP-form, SMB, RDP, MySQL, entre outros. É utilizada em pentests autorizados para avaliar a robustez de credenciais.

---

## Conceitos principais
- **Brute-force / credential stuffing:** tenta combinações de usuário e senha.  
- **Módulos/protocolos:** suporte a diversos serviços (ssh, ftp, http-post-form, smb, rdp, etc.).  
- **Paralelismo:** permite múltiplas threads para acelerar testes.  
- **Fail condition:** define a resposta que indica falha (ex.: string de erro no login HTTP).

---

## Funcionalidades principais
- Suporte a dezenas de protocolos de autenticação.  
- Uso de wordlists (`-L`/`-P`) ou pares específicos (`-l`/`-p`).  
- Parar após sucesso (`-f`) ou continuar para múltiplos logins válidos.  
- Registro de resultados em arquivo (`-o`) e modo verbose (`-V`).  

---

## Flags / opções úteis
- `-l <user>` — usuário único  
- `-L <userfile>` — arquivo com lista de usuários  
- `-p <pass>` — senha única  
- `-P <passfile>` — arquivo com lista de senhas  
- `-s <port>` — porta do serviço  
- `-t <threads>` — número de threads  
- `-f` — parar após primeiro sucesso  
- `-M <targetsfile>` — arquivo com múltiplos alvos  
- `-o <outfile>` — salvar resultados  
- `-V` — verbose  
- `-e nsr` — testar variações de senha (null, single, reversed)  
- `http-post-form` — módulo para login web, precisa indicar string de falha.

---

## Exemplos de uso teórico

*1) SSH (usuário único)*

hydra -l root -P /wordlists/rockyou.txt ssh://192.168.1.10 -t 4 -o hydra_ssh_out.txt

*2) FTP (lista de usuários e senhas)*

hydra -L users.txt -P passwords.txt ftp://ftp.example.com -t 8 -o hydra_ftp_out.txt

*3) HTTP POST Form*

hydra -L users.txt -P passwords.txt example.com http-post-form "/login:username=^USER^&password=^PASS^:F=Login failed" -t 12 -o hydra_http_out.txt

*4) Targets múltiplos*

hydra -L users.txt -P passwords.txt -M targets.txt ssh -t 6 -o hydra_multi_out.txt

*6) Credential stuffing com combos*

hydra -C combos.txt ssh -t 4 -o hydra_combo_out.txt

---

## Boas práticas
Use paralelismo controlado para não sobrecarregar o alvo.

Prefira wordlists adaptadas ao contexto.

Teste em ambientes autorizados.

Documente todas as tentativas e timestamps.

Combine com monitoramento de lockouts e IDS/IPS.

## Observações legais
Não execute sem autorização.

Obtenha permissão por escrito e defina escopo claro.

Ataques não autorizados são ilegais e podem gerar consequências criminais.

Sempre documente resultados, limites e evidências para relatórios de pentest.
