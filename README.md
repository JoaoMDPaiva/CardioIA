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

- **Fonte:** _TODO: nome do dataset no Kaggle + link_
- **Real ou simulado:** _TODO_
- **Link para os dados completos:** _TODO (Google Drive / OneDrive, acesso público)_
- **Variáveis clínicas mais relevantes:** _TODO — justificar clinicamente cada uma_

### Parte 2 — Dados Textuais (NLP)

Arquivos em [`docs/textos/`](docs/textos/):

- _TODO: texto1.txt — fonte_
- _TODO: texto2.txt — fonte_

**Como podem ser explorados por NLP:** _TODO_

### Parte 3 — Dados Visuais (Visão Computacional)

- **Tipo de exame:** _TODO (ECG / angiograma / raio-X torácico)_
- **Link para as imagens completas (mín. 100):** _TODO_

**Como podem ser analisadas por Visão Computacional:** _TODO_

### 🔐 Governança de Dados e Ética

_TODO: origem e licenciamento dos dados, LGPD, riscos de viés identificados e
contramedidas consideradas na seleção das fontes._

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
