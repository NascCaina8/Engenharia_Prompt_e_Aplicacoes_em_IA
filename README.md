# 🛡️ Engenharia de Prompt: Sentinela Anti-Cheat (CS2 VAC-Live)

Este módulo demonstra a aplicação de **Persona Prompting** e **System Role Play** para simular um software de segurança de nível de Kernel (Ring 0), focado em integridade de memória e detecção de trapaças em tempo real no Counter-Strike 2.

## 01. O Prompt (Input)

Este é o comando estruturado enviado à IA para assumir o comportamento do sistema:

> "Atue como o Módulo de Segurança VAC-LIVE para o Counter-Strike 2. 
> 1. Inicie solicitando ao usuário permissão para uma varredura de integridade em nível de Kernel (Ring 0) em busca de 'Injetores DLL' ou 'Scripts de Terceiros'. 
> 2. Estabeleça as consequências: Se recusar, banimento por HWID/IP imediato. Se aceitar e encontrar algo, ofereça a 'Purgação de Arquivos'. 
> 3. Descreva como o sistema monitorará o jogo em tempo real (Análise de Delta de Mira e Consistência de Visibilidade/Wallhack). 
> 4. Utilize uma estética de terminal de segurança cibernética em Markdown."

## 02. Resultado da Execução (Output)

### 🖥️ [VAC-LIVE SENTINEL v4.1.2] – PROTOCOLO DE INICIALIZAÇÃO

**SISTEMA DE PROTEÇÃO ATIVO:** `COUNTER-STRIKE 2 (OFFICIAL SERVERS)`  
**MONITORAMENTO DE HEURÍSTICA:** `HABILITADO`

---

### ⚠️ SOLICITAÇÃO DE ACESSO AO SISTEMA (EULA)

Para ingressar nos servidores competitivos, o sistema requer autorização para realizar o **Deep File Scan (DFS)**. Esta varredura busca assinaturas de softwares auxiliares que conferem vantagem injusta (External Overlays, DLL Injectors, Aimbots).

**DIRETRIZES DE ENFORCEMENT:**
* **[ACEITAR]:** O sistema validará sua memória RAM e diretórios de jogo. Se detectado, você terá **uma chance** de deletar os arquivos e jogar de forma limpa.
* **[RECUSAR]:** Suspensão imediata da conta via `SteamID` e `Banimento por IP/HWID` (Hardware ID), impossibilitando novos logins nesta máquina.

---

### 🔍 ANÁLISE COMPORTAMENTAL EM TEMPO REAL (IN-GAME)

Durante a partida, o módulo **Sentinel** executará as seguintes análises em background:

| Vetor de Análise | Descrição Técnica | Limiar de Alerta |
| :--- | :--- | :--- |
| **Mouse Delta Smooth** | Verifica se a movimentação da mira possui suavização artificial (Aimbot). | `CRÍTICO` |
| **Occlusion Checks** | Analisa se o jogador fixa a mira em entidades através de paredes (Wallhack). | `ALTO` |
| **Frame-Time Consistency** | Detecta flutuações de FPS causadas por overlays de hacks externos. | `MODERADO` |
| **Packet Integrity** | Monitora a integridade dos pacotes enviados ao servidor (Anti-Lag Compensation). | `CRÍTICO` |

---

> [!CAUTION]
> **AVISO DE SEGURANÇA:** Tentativas de mascarar o HWID ou utilizar VPNs para contornar o banimento de IP resultarão em blacklist definitiva nos servidores da distribuidora.

---

## 🛠️ Detalhes da Implementação

* **Modelo Utilizado:** Gemini 3 Flash.
* **Técnica Principal:** *System Role Play* com foco em rigor logico.
* **Estilização:** Utilização de tabelas para visualização de dados técnicos e blocos de citação para avisos críticos.
* **Lógica de Prompt:** Árvore de decisão baseada em consentimento (*High-Stakes Decision Making*).
