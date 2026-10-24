# cvesandstuffs

Relatórios técnicos de vulnerabilidades (CVEs) de tecnologias muito usadas em desenvolvimento web, infraestrutura e IA, escritos em português e focados em **quem precisa agir**: suporte técnico, infraestrutura e Blue Team.

Cada relatório explica, para cada CVE, **o que a falha identifica**, **qual o impacto**, **como corrigir** e **o que fazer enquanto a correção não chega**, sempre citando as fontes oficiais do fabricante.

> Data de referência dos relatórios: **21 a 23 de outubro de 2026**.
> Vulnerabilidades mudam rápido — antes de agir em produção, confirme no aviso oficial linkado em cada documento.

---

## Relatórios

| Relatório | Período | Destaque | Arquivo |
|---|---|---|---|
| **PHP** | jul–out/2026 | *PHP2Shell* — CVE-2026-109618 e CVE-2026-109619, RCE sem autenticação (CVSS 4.0 = 9,2) | [`CVEs_PHP_jul-out_2026.pdf`](CVEs_PHP_jul-out_2026.pdf) |
| **Node.js** | jun–out/2026 | CVE-2026-111497 — escrita fora dos limites no decodificador Brotli (RCE); 33 CVEs detalhadas | [`CVEs_NodeJS_jun-out_2026.pdf`](CVEs_NodeJS_jun-out_2026.pdf) |
| **Microsoft** | Patch Tuesday out/2026 | ~1.410 CVEs no mês; zero-day explorado CVE-2026-96951 (Windows Shell / Mark of the Web) e RCEs críticas no Outlook | [`CVEs_Microsoft_out_2026.pdf`](CVEs_Microsoft_out_2026.pdf) |
| **Java (Oracle)** | CPU out/2026 | 52 CVEs do Java SE explicadas por componente + Security Alert CVE-2026-91403 (CAs eMudhra, CVSS 9,1) | [`CVEs_Java_out_2026.pdf`](CVEs_Java_out_2026.pdf) |
| **Python (CPython)** | ago–out/2026 | CVE-2026-19445 (ssl, CVSS 4.0 = 9,2), cinco falhas no `tarfile` e aviso crítico do `certifi` | [`CVEs_Python_ago-out_2026.pdf`](CVEs_Python_ago-out_2026.pdf) |
| **Next.js** | jul–out/2026 | Quatro RCEs críticas sem autenticação (`use cache`, Image Optimization com SVG/AVIF, servidores Windows) | [`CVEs_NextJS_jul-out_2026.pdf`](CVEs_NextJS_jul-out_2026.pdf) |
| **Ferramentas de IA** | 2026 (foco em out) | Claude Agent SDK, Ollama, LMCache, Claude Code Desktop (*SneakPeek*), Plugin4Shell e falhas de agentes em CI | [`CVEs_IA_2026.pdf`](CVEs_IA_2026.pdf) |

---

## O que cada relatório contém

Todos seguem a mesma estrutura, para facilitar a consulta:

1. **Sumário executivo** — o que é mais urgente e uma tabela com todas as CVEs (componente, tipo, gravidade, data).
2. **Conceitos e versões** — glossário dos termos técnicos e tabela de linhas suportadas / fim de vida.
3. **Ficha de cada CVE** — título oficial, vetor CVSS, CWE, versões afetadas e corrigidas, créditos.
4. **Explicação** — *O que identifica*, *Impacto* e *Correção e mitigação*.
5. **Recomendações práticas** — prioridade de atualização, checklist para o suporte técnico e sinais para monitorar (Blue Team).
6. **Fontes de pesquisa** — links numerados para os avisos oficiais e análises consultadas.

---

## Fontes e metodologia

- **Fontes primárias:** avisos dos próprios fabricantes e das autoridades emissoras de CVE (CNAs):
  - PHP: GitHub Security Advisories do `php/php-src`, ChangeLog do php.net e PHP Foundation
  - Node.js: avisos de segurança em nodejs.org e notas de versão
  - Microsoft: Security Update Guide (MSRC) e Windows message center
  - Oracle: Critical Patch Update Advisory, Security Alert e notas de versão do JDK
  - Python: lista `security-announce@python.org` e registros da PSF como CNA
  - Next.js: blog oficial (nextjs.org) e GitHub Security Advisories do `vercel/next.js`
  - IA: GitHub Security Advisories dos fabricantes, CERT Polska e NVD
- **Fontes complementares:** NVD, CISA, CSA Singapura e análises de empresas de segurança (Tenable, Qualys, ZDI etc.), sempre identificadas como de terceiros no texto.
- **Quando os dados divergem** (notas CVSS diferentes, versões corrigidas conflitantes), os relatórios mostram as duas versões e indicam qual segue o aviso oficial.
- **Paliativos que não vêm do fabricante** estão marcados como *não oficiais*.

---

## Aviso

Material de **estudo e apoio à defesa**. Os relatórios não contêm exploits nem provas de conceito, e não substituem os avisos oficiais dos fabricantes. As informações refletem o que estava publicado até a data de referência; correções, notas e status de exploração podem ter mudado depois.

---

## Autor

**João Victor Paixão Zolim**
[LinkedIn](https://www.linkedin.com/in/joao-victor-paixao-zolim) · [GitHub](https://github.com/joaovpzdev)

Pesquisa e redação feitas com apoio do Claude (Anthropic).