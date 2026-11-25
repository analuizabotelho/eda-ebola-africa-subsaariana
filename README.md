# Ebola na África Subsaariana, 2014–2026

Análise exploratória de dados e data storytelling sobre 1.200 registros semanais de Ebola em 7 países. **Mensagem principal: o atraso entre os sintomas e a internação é o fator mais associado à letalidade.**

Projeto em grupo da disciplina Exploratory Data Analysis (Prof. Kyung Moo Kim), Unimpacta.
Grupo: Ryan Hangai, Ana Luiza Botelho, Arthur Guerra, Michel Domingues e Julio Magno.

## Minha contribuição
Responsável pela parte de Data Storytelling: relatório executivo, plano de ação com metas e apresentação. Também participei dos ajustes da Etapa 1 e das visualizações da Etapa 2.

## Dados
- Base fornecida pelo professor da disciplina.
- 1.200 registros semanais, 7 países (Serra Leoa, Guiné, Libéria, RDC, Nigéria, Mali e Uganda), de 01/01/2014 a 30/09/2026.
- Tratamento: 84 nulos em dias até a internação e 60 em leitos por 10 mil habitantes, imputados pela mediana e marcados em colunas próprias. Valores extremos foram mantidos por serem plausíveis em surtos.
- Variáveis criadas: óbitos estimados, incidência por 100 mil habitantes (população de 2024, Banco Mundial) e médias móveis.

## Principais achados
- **Atraso na internação e letalidade:** a letalidade média vai de 43% (internação no mesmo dia) a 77% (10 dias de atraso), cerca de 3 a 4 pontos percentuais por dia. Correlação de 0,74 (Spearman 0,81). É uma associação, não prova de causa.
- **Carga semanal estável**, em torno de 100 casos e 60 óbitos estimados por semana, com dois picos pontuais: 720 casos na Libéria (28/06/2015) e 650 em Mali (08/04/2014).
- **Letalidade parecida entre países** (56,7% a 59,2%); a diferença vem do volume de casos. Serra Leoa lidera em volume e a Libéria em incidência por habitante.
- **Leitos por 10 mil habitantes, idade do paciente e casos semanais** não mostraram associação com a letalidade nestes dados.
- **Teste t de Student (Etapa 3):** comparando 2014–2019 com 2020–2026, a letalidade média caiu de 58,22% para 56,34% (t = 3,916; p = 0,0001; gl = 1198; α = 5%). A diferença é estatisticamente significativa, mas indica apenas uma leve queda, sem provar a causa.

## Recomendações
Reduzir os casos internados com 6 dias ou mais de atraso, revisar os atrasos extremos, criar um alerta semanal e priorizar Libéria e Serra Leoa. Detalhes no relatório.

## Limitações
- População de 2024 aplicada a todo o período.
- Óbitos estimados a partir da letalidade e dos casos, não observados diretamente.
- Registros espaçados, então as médias móveis têm poucos pontos.
- Correlação não prova causa.

## Arquivos
- `ebola_eda.ipynb`: notebook com a análise (Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy, StatsModels)
- `relatorio.pdf`: relatório executivo (versão da Etapa 2)
- `apresentacao.pdf`: apresentação (versão da Etapa 2)
