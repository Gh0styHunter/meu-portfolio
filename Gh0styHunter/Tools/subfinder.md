# Subfinder

**Descrição:**  
Subfinder (ProjectDiscovery) é uma ferramenta de enumeração passiva de subdomínios, rápida e eficiente, que coleta informações de múltiplas fontes OSINT (APIs, certificados SSL, motores de busca) para identificar subdomínios conhecidos de um domínio alvo. É usada principalmente na fase de recon passivo de pentests.

---

## Conceitos principais
- **Enumeração passiva:** coleta informações sem interagir diretamente com o alvo.  
- **Pluggable sources:** integração com várias fontes via API keys para melhorar cobertura.  
- **Pipeline de recon:** normalmente usada antes de ferramentas ativas como Amass, MassDNS ou ffuf.  

---

## Funcionalidades principais
- Descoberta de subdomínios via múltiplas fontes OSINT (crt.sh, VirusTotal, DNSDumpster, etc.).  
- Suporte a arquivos de saída em TXT ou JSON.  
- Filtragem de resultados (wildcards, inclusão/exclusão de padrões).  
- Alta performance com baixo consumo de recursos.  

---

## Instalação (teórico)
- Instalar via Go:

go install github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest

Configurar API keys em ~/.config/subfinder/config.yaml (opcional, mas recomendado).

##Flags / opções úteis
-d <domain> — domínio alvo único

-dL <file> — arquivo com lista de domínios

-o <outfile> — arquivo de saída TXT

-oJ — saída em JSON

-silent — exibe apenas resultados encontrados

-all — usar todas as fontes disponíveis

-nW — desativar wildcards

-recursive — busca recursiva de subdomínios

-t <threads> — definir número de threads

##Exemplos de uso teórico
1) Enumeração passiva simples

subfinder -d exemplo.com -o subfinder_exemplo.txt

2) Múltiplos domínios a partir de arquivo

subfinder -dL domains.txt -o all_subs.txt

3) Saída JSON para pipelines

subfinder -d exemplo.com -oJ > subfinder_exemplo.json

---

## Boas práticas
Combine subfinder com ferramentas ativas como Amass ou ffuf para maior cobertura.

Configure API keys para fontes externas para melhorar resultados.

Normalize e dedupe a lista de subdomínios antes de usar em scanners ou ataques simulados.

Documente a origem de cada subdomínio para evidências em relatórios.

## Observações legais
A enumeração passiva geralmente é segura, mas algumas fontes externas podem gerar requests.

Sempre respeite termos de uso de APIs e limites de rate.

Execute apenas em alvos autorizados, mesmo em recon passivo, para evitar problemas legais.
