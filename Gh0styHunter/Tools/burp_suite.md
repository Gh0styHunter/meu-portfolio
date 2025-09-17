# Burp Suite

**Descrição:**  
Burp Suite é uma plataforma integrada para teste de segurança de aplicações web. Possui proxy para interceptação, utilitários para manipulação de requisições, scanner (na versão profissional) e ferramentas auxiliares úteis durante um pentest web.

---

## Funcionalidades principais
- Proxy HTTP(S) para interceptar e modificar tráfego entre browser e servidor  
- Repeater para reenvio e ajuste manual de requisições  
- Intruder para automação de ataques controlados (fuzzing, brute force)  
- Scanner automatizado (versão Pro) para identificar vulnerabilidades web  
- Sequencer para análise de entropia de tokens/sessões  
- Extensibilidade via BApp Store e extensões personalizadas

---

## Componentes importantes
- **Proxy:** intercepta e modifica tráfego.  
- **Target:** organização dos endpoints descobertos.  
- **Scanner:** identifica automaticamente problemas (XSS, SQLi, etc.).  
- **Intruder:** automatiza variações de payloads.  
- **Repeater:** testar manualmente requisições.  
- **Comparer, Sequencer, Decoder**: utilitários auxiliares.

---

## Fluxo de uso teórico
1. Configurar browser para usar Burp como proxy.  
2. Navegar pela aplicação para mapear endpoints (Target).  
3. Interceptar requisições e analisar parâmetros (Proxy).  
4. Usar Repeater para testar manipulações manuais.  
5. Usar Intruder para fuzzing de parâmetros ou brute-force controlado.  
6. (Pro) Executar Scanner para relatar vulnerabilidades automaticamente.

---

## Exemplos de uso teórico
- Interceptar requisição de login e alterar parâmetros para testar autenticação.  
- Inserir payloads em campos com Repeater para validar XSS refletido.  
- Usar Intruder com wordlists para testar usernames ou parâmetros.

---

## Boas práticas / Observações
- Ao usar Burp, registre todas as requisições relevantes com contexto para relatórios.  
- Combine escaneamentos automáticos com testes manuais (falso-positivos são comuns).  
- Use extensões (ex.: Autorize, Logger) para tarefas repetitivas.  
- Configurar certificados SSL do Burp no browser para interceptar HTTPS.

---

## Observações legais
- Interceptação e manipulação de tráfego sem permissão é ilegal. Use apenas em ambientes autorizados.

