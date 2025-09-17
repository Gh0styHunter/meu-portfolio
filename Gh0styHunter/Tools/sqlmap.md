# sqlmap

**Descrição:**  
sqlmap é uma ferramenta automatizada para detecção e exploração de falhas de SQL Injection em aplicações web. Permite enumerar bancos de dados, tabelas, colunas e até executar comandos dependendo do nível de acesso.

---

## Funcionalidades principais
- Detecção automática de SQLi (boolean, time-based, error-based, etc.)  
- Extração de dados (dbs, tables, columns)  
- Upload/execução de comandos (dependendo do backend)  
- Bypass de WAFs básicos com técnicas e tampering scripts  
- Suporte a múltiplos SGBDs (MySQL, PostgreSQL, MSSQL, Oracle, etc.)

---

## Opções / flags úteis (teórico)
- `-u` — URL alvo com parâmetro vulnerável.  
- `-p` — parâmetro a testar (`id`, `q` etc.).  
- `--dbs` — listar bancos de dados.  
- `--tables -D nome_db` — listar tabelas de um DB.  
- `--columns -D nome_db -T nome_tabela` — listar colunas.  
- `--dump -D nome_db -T nome_tabela` — extrair dados.  
- `--level` / `--risk` — aumentar profundidade e risco das técnicas.

---

## Exemplos de uso teórico
sqlmap -u "http://exemplo.com/produto?id=1" -p id --dbs

- Testa o parâmetro `id` e lista bancos de dados se vulnerável.

---

- Testa o parâmetro `id` e lista bancos de dados se vulnerável.

---

## Boas práticas / Observações
- Use em alvos autorizados; o processo de exploração pode afetar a disponibilidade.  
- Documente apenas os resultados necessários para o escopo (evite extrair dados sensíveis sem necessidade).  
- Combine resultados do sqlmap com validações manuais para confirmar falsos-positivos.

---

## Observações legais
- Extração de dados de sistemas sem autorização é crime — sempre trabalhar dentro do escopo autorizado.

- Extração de dados de sistemas sem autorização é crime — sempre trabalhar dentro do escopo autorizado.

