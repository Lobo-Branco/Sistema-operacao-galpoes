# 🏢 Sistema Integrado de Gestão Operacional & BPO (Case de Estudo)

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=Streamlit&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white)
![UI/UX](https://img.shields.io/badge/UI/UX-Dark_Theme-000000?style=for-the-badge)

> 🔒 **Nota de Confidencialidade:** Este é um repositório de portfólio focado em arquitetura de software, UI/UX e regras de negócio. O código-fonte é proprietário e não está disponível publicamente (NDA). As imagens contêm dados ofuscados para preservar informações sensíveis corporativas.

## 📌 O Desafio
Operações de processamento de documentos (BPO) lidam com volumes massivos de dados, gargalos logísticos e a necessidade de microgerenciamento de equipes. O desafio era unificar o acompanhamento de metas, auditoria de galpão, controle de ponto, fechamento de produção e emissão de hardware (impressoras térmicas) em uma **única plataforma web centralizada, ágil e à prova de falhas humanas**.

## 💡 A Solução
Desenvolvi uma aplicação full-stack utilizando Python com foco em alta performance, análise de dados e experiência do usuário (UX). O sistema elimina planilhas fragmentadas e entrega "Inteligência Operacional em Tempo Real".

---

## 🚀 Funcionalidades Principais (Módulos)

### 1. Painel de Controle (Real-Time Dashboard)
Monitoramento ao vivo da "saúde" da operação. O gestor não precisa esperar o fim do dia para tomar decisões críticas.
* **Métricas Dinâmicas:** Acompanhamento do Total Indexado, Eficiência Atual (%) e Volume faltante para atingir a meta do dia.
* **Visão por Esteira:** Acompanhamento detalhado do volume por etapa (Preparação, Controle, Guarda, Digitalização).
* **Gestão de Pessoas Integrada:** Painel lateral cruzando ausências, férias e atestados, permitindo remanejamento imediato da equipe.

![Painel de Controle](1-dashboard.png)

---

### 2. Gamificação e Ranking de Desempenho
Transformando pressão operacional em engajamento amigável e baseado em dados.
* **Pódio Dinâmico:** Destaque automático (Top 3 e Top 1 por esteira) para os colaboradores mais produtivos.
* **Gestão de Baixo Desempenho:** Alertas visuais automatizados (Métrica Crítica / Alerta) para identificar gargalos operacionais e permitir feedback rápido do supervisor.

![Ranking e Desempenho](2-ranking.png)

---

### 3. Fechamento Diário e Balanceamento
Consolidação inteligente de dados para faturamento e controle de SLAs.
* **Gráficos e Resumos:** Visualização gráfica da produção total por setor.
* **Detalhamento Balanceado:** Cruzamento automático de horas trabalhadas versus volume produzido, gerando o percentual de eficiência individual exato.
* **Exportação Prática:** Integração com um clique para copiar/exportar todos os dados já mastigados para relatórios de diretoria.

![Fechamento Diário](5-fechamento.png)

---

### 4. Auditoria e Pendências de Lançamento (Leakage)
Controle rigoroso de horas não faturadas ou esquecidas.
* **Radar de Pendências:** O sistema mapeia os horários da operação e cruza com a produção declarada. 
* **Ação Direta:** Lista automaticamente quem "esqueceu" de lançar horas (ex: *Existem 89 horários não lançados por 21 pessoas*), exigindo justificativa diretamente na plataforma, fechando as brechas de produtividade.

![Auditoria de Pendências](3-pendencias.png)

---

### 5. Integração de Hardware (Motor de Impressão Zebra)
A ponte robusta entre o software e o chão de fábrica (Galpão).
* **Motor Vetorial:** Geração de PDFs em tempo real com código de barras, perfeitamente dimensionados para **impressoras térmicas Zebra**.
* **Fila Sequencial Inteligente:** Memória global que puxa o último lote impresso e gera a numeração contínua, evitando duplicidade em caixas físicas.
* **Trava de Segurança Térmica:** Algoritmo que impõe pausas automatizadas para evitar o superaquecimento e a queima da cabeça de impressão.

![Impressão de Lotes](4-impressao.png)

---

## 🛠️ Arquitetura e Tecnologias Utilizadas
A arquitetura foi projetada para lidar com requisições assíncronas e grande volume de dados:
* **Frontend/UI:** Streamlit com injeção de CSS customizado (Dark Theme responsivo, tooltips, cards flutuantes).
* **Backend:** Python 3.x.
* **Processamento de Dados (ETL):** Pandas para manipulação massiva de dataframes, limpeza de strings e cálculos de eficiência.
* **Visão Computacional & IA:** EasyOCR para leitura de imagens e integração via API com o **Google Gemini (LLM)** para análise semântica e classificação documental avançada.
* **Integrações Externas:** API do Google (Sheets/Drive) para sincronização de base de dados em nuvem sem delay.

## 📈 Impacto no Negócio
* **Redução de SLA de Gestão:** Decisões de alocação de equipe que demoravam horas agora são tomadas em segundos.
* **Zero Perda Físico-Digital:** O motor de impressão mitigou 100% da duplicidade de lotes colados nas caixas.
* **Recuperação de Receita:** O módulo de pendências reduziu o "vazamento" de horas não lançadas, garantindo que toda a produção seja faturada.

---
*Arquitetado e Desenvolvido por **Bruno Queiros**.*
