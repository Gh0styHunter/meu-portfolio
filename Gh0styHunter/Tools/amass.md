# amass

**Descrição:**  
Amass (OWASP Amass / ProjectDiscovery fork popular) é uma ferramenta de enumeração de ativos focada em descoberta de subdomínios, mapeamento de infraestrutura e correlação de dados a partir de múltiplas fontes (passivas e ativas). Muito usada em recon de superfície de ataque e levantamento de ativos.

---

## Principais conceitos
- **Enumeração passiva:** coleta de subdomínios a partir de fontes públicas (OSINT) sem tocar nos alvos (ex.: certificados, arquivos públicos, APIs).  
- **Enumeração ativa:** consultas DNS, brute-force e varreduras que interagem com o alvo.  
- **Graphing / correlation:** Amass gera grafo de relacionamentos entre domínios, ASN, IPs e provedores.  
- **Integração:** suporta integrações com serviços externos (VirusTotal, Shodan, Censys, etc.) via API keys.

---

## Funcionalidades principais
- Descoberta de subdomínios (passiva e ativa)  
- Enumeração por brute-force (wordlists)  
- Resolução DNS em massa e verificação de takeover potencial  
- Mapeamento de rede (ASN, IP ranges) e correlação por infraestrutura  
- Exportação para JSON/CSV/graph formats (GEXF)  
- Suporte a configurações customizadas (config file) e modo distribuído

---

## Instalação (teórico)
- Instalar via `go install` ou pacotes pré-compilados / repositório oficial:
```bash
go install -v github.com/owasp-amass/amass/v3/...@latest
exit

## Opções / flags úteis (teórico)

enum — modo de enumeração principal (amass enum -d exemplo.com)

-d — domínio alvo (-d exemplo.com)

-oA — saída em múltiplos formatos (-oA resultado)

-o — arquivo de saída simples (-o out.txt)

-src — incluir fonte nos resultados (mostrar origem da descoberta)

-ip — também resolver e mostrar IPs associados

-rf — usar wordlist para brute-force (resolver nomes gerados)

-brute — habilitar brute forcing (quando configurado)

-passive — rodar apenas coleta passiva (sem consultas ativas)

-config — arquivo de configuração customizado (keys, settings)

-viz / gexf — exportar grafo para análise (Gephi)

--

## Exemplos de uso prático (teórico)

*Enumeração passiva + ativa básica*

amass enum -d exemplo.com -oA amass_exemplo


*Enumeração passiva apenas (sem tocar o alvo)*

amass enum -d exemplo.com -passive -o amass_passive.txt


*Bruteforce com wordlist e resolução de IPs*

amass enum -d exemplo.com -brute -rf /wordlists/subdomains.txt -ip -o amass_brute.txt


*Gerar grafo para Gephi*

amass viz -d exemplo.com -o gexf -o amass_graph.gexf

## Boas práticas / Observações

Configure API keys (VirusTotal, Censys, Shodan, etc.) para aumentar cobertura e qualidade dos resultados.

Use -passive quando não quiser gerar tráfego ativo (bom para coleta inicial).

Combine Amass com subfinder e outras ferramentas para maior recall (passive-first, depois active).

Filtre e dedupe resultados (muitos subdomínios são aliases/CNAMEs).

Documente a origem de cada domínio (fonte) para evidência em relatórios.

## Observações legais

Enumeração de subdomínios geralmente é passiva (OSINT), mas brute-force e resolução em massa podem gerar tráfego — execute apenas com autorização quando fizer parte de um teste.

Respeite políticas de robots e limites de APIs externas (uso de API keys).
