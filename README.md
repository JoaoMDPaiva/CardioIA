# FIAP - Faculdade de Informática e Administração Paulista

<p align="center">
<a href= "https://www.fiap.com.br/"><img src="assets/logo-fiap.png" alt="FIAP - Faculdade de Informática e Admnistração Paulista" border="0" width=40% height=40%></a>
</p>

<br>

# CardioIA — A Nova Era da Cardiologia Inteligente

## Nome do grupo
_TODO: a definir_

## 👨‍🎓 Integrantes:
- _TODO: integrantes serão adicionados após a conclusão da atividade individual_

## 👩‍🏫 Professores:
### Tutor(a)
- _TODO_
### Coordenador(a)
- _TODO_

## 📜 Descrição

O **CardioIA** é um projeto acadêmico do curso de IA da FIAP que simula, ao
longo de 7 fases, o ecossistema de uma cardiologia moderna — integrando dados
clínicos, Machine Learning, Visão Computacional, IoT e agentes inteligentes
para apoiar triagem, diagnóstico, monitoramento, assistência remota e
previsões médicas.

Nesta **Fase 1 — Batimentos de Dados**, o papel assumido é o de cientista de
dados hospitalar: o objetivo é levantar, organizar e documentar três tipos de
dados que servirão de base para os módulos inteligentes das fases seguintes:

1. **Dados numéricos** (reais ou simulados) de pacientes cardíacos;
2. **Dados textuais** (médicos ou literários) sobre saúde cardiovascular;
3. **Dados visuais** (imagens de exames cardiológicos).

A escolha e organização das fontes já considera, desde esta fase, os
conceitos de **Governança de Dados e viés** — relevância clínica,
representatividade da amostra e transparência sobre a origem dos dados —
detalhados na seção [Governança de Dados e Ética](#-governança-de-dados-e-ética).

## 📁 Estrutura de pastas

Dentre os arquivos e pastas presentes na raiz do projeto, definem-se:

- <b>.github</b>: arquivos de configuração específicos do GitHub que ajudam a
  gerenciar e automatizar processos no repositório.
- <b>assets</b>: elementos não-estruturados do repositório, como imagens.
- <b>config</b>: arquivos de configuração usados para definir parâmetros e
  ajustes do projeto.
- <b>docs/textos</b>: os arquivos `.txt` da Parte 2 (Dados Textuais / NLP)
  desta fase — subpasta adicionada ao template-base conforme permitido pelo
  enunciado da atividade.
- <b>document</b>: documentos do projeto exigidos pelas atividades. Na
  subpasta "other", documentos complementares e menos importantes.
- <b>scripts</b>: scripts auxiliares para tarefas específicas do projeto
  (ex.: deploy, migrações de banco de dados, backups).
- <b>src</b>: todo o código-fonte criado para o desenvolvimento do projeto ao
  longo das 7 fases.
- <b>README.md</b>: este arquivo, guia e explicação geral sobre o projeto.

## 🩺 Fase 1 — Batimentos de Dados

### Parte 1 — Dados Numéricos (IoT)

- **Fonte:** [Heart Failure Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction) (Kaggle, curado por fedesoriano) — combinação de 5 bases clínicas reais: Cleveland Clinic Foundation, Hungarian Institute of Cardiology (Budapeste), University Hospital de Zurique, University Hospital de Basel e V.A. Medical Center (Long Beach), originalmente doadas ao [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/).
- **Real ou simulado:** Real. Todas as variáveis foram aferidas em exame clínico (não autodeclaradas pelo paciente), com os médicos responsáveis por cada instituição de origem identificados nominalmente.
- **Licença:** Open Database License (ODbL) — autoriza explicitamente copiar e redistribuir a base com atribuição, o que permite hospedar a cópia abaixo.
- **Link para os dados completos:** [heart.csv — Google Drive, acesso público](https://drive.google.com/file/d/1Q8bq2rCqqPY7Ipmao7megFtDihwAGGy6/view?usp=sharing)
- **Tamanho:** 918 registros × 12 colunas (11 variáveis preditoras + variável-alvo), resultado da deduplicação de 1.190 observações originais (272 duplicadas removidas na curadoria).

**Variáveis clínicas mais relevantes:**

| Variável | Justificativa clínica |
|---|---|
| `Age` | Principal fator de risco não modificável para doença cardiovascular; risco cresce de forma acentuada após os 45-55 anos. |
| `Sex` | O risco cardiovascular e a idade de início diferem significativamente entre homens e mulheres. |
| `ChestPainType` | Tipo de dor no peito (angina típica/atípica, não anginosa, assintomático) é sintoma-chave na triagem inicial de doença coronariana. |
| `RestingBP` | Hipertensão é um dos principais fatores de risco modificáveis para doença cardíaca. |
| `Cholesterol` | Colesterol sérico elevado está diretamente associado à aterosclerose e obstrução coronariana. |
| `FastingBS` | Hiperglicemia/diabetes é comorbidade de alto risco para eventos cardiovasculares. |
| `RestingECG` | Identifica anormalidades elétricas do coração (ex.: hipertrofia ventricular) associadas a doença estrutural. |
| `MaxHR` | Capacidade funcional cardiovascular reduzida está associada a pior prognóstico. |
| `ExerciseAngina` | Angina induzida por esforço é sintoma de isquemia miocárdica e forte preditor de doença coronariana. |
| `Oldpeak` | Depressão do segmento ST é achado eletrocardiográfico clássico de isquemia sob esforço. |
| `ST_Slope` | Complementa o `Oldpeak` na caracterização do padrão isquêmico no ECG de esforço. |
| `HeartDisease` | Variável-alvo (0/1) — presença ou ausência de doença cardíaca, usada para treinar/validar modelos preditivos nas próximas fases do curso. |

### Parte 2 — Dados Textuais (NLP)

Arquivos em [`docs/textos/`](docs/textos/), ambos artigos científicos reais publicados nos *Arquivos Brasileiros de Cardiologia*, indexados no PubMed Central (PMC) sob licença **Creative Commons Attribution (CC BY)**, que autoriza reprodução com atribuição da fonte:

- [`manejo-dcv-mulheres.txt`](docs/textos/manejo-dcv-mulheres.txt) — Oliveira GMM, Wenger NK. *Manejo das Doenças Cardiovasculares em Mulheres: É Trabalho de Todos*. Arq Bras Cardiol. 2023;120(5):e20230250. [PMC10263394](https://pmc.ncbi.nlm.nih.gov/articles/PMC10263394/). Aborda fatores de risco, sintomas e determinantes específicos de sexo nas doenças cardiovasculares.
- [`doenca-isquemica-renda.txt`](docs/textos/doenca-isquemica-renda.txt) — Bertoletti OA. *Doença Cardíaca Isquêmica e Nível de Renda – Uma Reflexão Acerca de Determinantes Sociais e Estruturais*. Arq Bras Cardiol. 2024;120(11):e20240014. [PMC11098580](https://pmc.ncbi.nlm.nih.gov/articles/PMC11098580/). Relaciona nível socioeconômico, ambiente urbano e prevalência de doença isquêmica do coração.

**Como podem ser explorados por NLP:**

- **Extração de sintomas e fatores de risco:** técnicas de Named Entity Recognition (NER) podem identificar automaticamente termos clínicos recorrentes (ex.: "hipertensão", "pré-eclâmpsia", "diabetes", "tabagismo") para alimentar uma base estruturada de fatores de risco cardiovascular a partir de texto livre.
- **Classificação de tópicos:** os dois textos cobrem ângulos diferentes (sexo/gênero vs. determinantes socioeconômicos) — um classificador supervisionado treinado sobre esses e outros artigos poderia rotular automaticamente novos textos médicos por tema, útil para triagem de literatura em larga escala.
- **Análise de sentimentos/tom:** embora sejam textos técnicos (tom predominantemente neutro-descritivo), a mesma técnica aplicada a textos de pacientes (ex.: relatos em prontuário, redes sociais) permitiria detectar urgência ou gravidade percebida de sintomas.
- **Sumarização automática:** dado o volume crescente de literatura médica, resumir artigos como estes automaticamente ajudaria profissionais de saúde a acompanhar evidências mais recentes sem ler o texto completo.

**Por que isso é relevante para IA em saúde:** a maior parte do conhecimento médico ainda está em texto não estruturado (artigos, prontuários, prescrições). Extrair informação estruturada desse texto é o que permite que os módulos de ML das próximas fases do CardioIA cruzem sintomas relatados em linguagem natural com os dados numéricos e de imagem já coletados, em vez de depender só de formulários estruturados.

### Parte 3 — Dados Visuais (Visão Computacional)

- **Tipo de exame:** _TODO (ECG / angiograma / raio-X torácico)_
- **Link para as imagens completas (mín. 100):** _TODO_

**Como podem ser analisadas por Visão Computacional:** _TODO_

### 🔐 Governança de Dados e Ética

- **Origem e licenciamento:** dataset real, combinação de 5 bases clínicas de instituições hospitalares nomeadas (não anônimas), doadas ao UCI Machine Learning Repository e curadas no Kaggle sob licença ODbL — o que garante o direito de hospedar publicamente uma cópia neste projeto. Confiabilidade da coleta e direito de redistribuição foram avaliados como critérios **independentes** na escolha da fonte: um dataset bem coletado não é necessariamente redistribuível, e vice-versa.
- **Por que este dataset e não uma base maior:** havia uma alternativa com 70.000 registros, mas com licença "Unknown" no Kaggle e variáveis parcialmente autodeclaradas pelo paciente (fumo, álcool, atividade física). Priorizamos o Heart Failure Prediction Dataset por suas variáveis serem majoritariamente aferidas clinicamente e por ter licença explícita que permite a redistribuição exigida por esta atividade.
- **Riscos de viés identificados:**
  - Os dados vêm de hospitais dos EUA e Europa, coletados entre as décadas de 1980-90 — não representam a população brasileira nem os perfis epidemiológicos atuais; qualquer modelo treinado sobre esta base exigiria validação/recalibração antes de qualquer uso clínico real.
  - Possível desbalanceamento entre sexos e faixas etárias nas amostras originais, a verificar antes de qualquer modelagem nas fases seguintes.
  - Critérios diagnósticos e tecnologias de exame de 1980-90 diferem dos padrões atuais.
- **LGPD:** os dados já são anonimizados/agregados na fonte (sem identificação direta de pacientes), o que reduz o risco de reidentificação. Ainda assim, são tratados como dado sensível de saúde, sem tentativa de cruzamento com outras bases.

## 🔧 Como executar o código

A Fase 1 é uma etapa de levantamento e documentação de dados, sem código
executável associado. Os conjuntos de dados estão disponíveis pelos links
públicos listados nas seções [Parte 1](#parte-1--dados-numéricos-iot) e
[Parte 3](#parte-3--dados-visuais-visão-computacional) acima; os textos da
Parte 2 estão versionados em [`docs/textos/`](docs/textos/).

## 🗃 Histórico de lançamentos

* 0.1.0 - _TODO: data_
    * Estrutura inicial do repositório (baseada no template FIAP) e entrega da Fase 1 — Batimentos de Dados.

## 📋 Licença

<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/agodoi/template">MODELO GIT FIAP</a> por <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://fiap.com.br">Fiap</a> está licenciado sobre <a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Attribution 4.0 International</a>.</p>
