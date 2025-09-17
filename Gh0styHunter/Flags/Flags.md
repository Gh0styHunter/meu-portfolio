# Flags Teóricas – GhostyHunter

## Vulnerabilidades Web
- **XSS Reflected:** `<script>alert('flag')</script>`  
- **XSS Stored:** `<script>document.cookie</script>`  
- **SQL Injection (Union-based):** `' UNION SELECT username,password FROM users --`  
- **IDOR:** `/user?id=2 → acesso a outro usuário`  
- **CSRF:** Form HTML que submete ações sem autorização do usuário  
- **LFI / RFI:** `/index.php?page=../../etc/passwd`  
- **Sensitive Data Exposure:** Endpoint expõe dados sensíveis sem autenticação

## API
- **Exposição de dados:** `GET /api/users → retorna dados sensíveis sem autenticação`  
- **Falha de autenticação:** Token JWT inválido aceito

## CTF Hack The Box – Meow
- **Flag:** `b40abdfe23665f766f9c61ecba8a4c19`  
- **Serviço explorado:** Telnet sem senha  
- **Diretório da flag:** `/root/flag.txt`  
- **Resumo:** Login root sem senha permitiu acesso completo à máquina
