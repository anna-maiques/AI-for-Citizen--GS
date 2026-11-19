# AI-for-Citizen--GS
O Citizen Assist AI é um assistente digital desenvolvido como parte da Global Solutions da disciplina Prompt and Artificial Intelligence.

O objetivo do projeto é facilitar o acesso a informações sobre documentos pessoais por meio de um chatbot que utiliza inteligência artificial e linguagem simples.

O assistente foi pensado principalmente para pessoas idosas, pessoas com deficiência e cidadãos com pouca familiaridade com serviços digitais.

**Importante:** este projeto é um protótipo educacional. As informações utilizadas foram fornecidas em fichas fictícias da Central do Cidadão de Aurora e não representam regras oficiais.

## Integrantes

- Fernando Hoefle — RM 569920
- Anna Cecília — RM 570955
- Lucas Parkin — RM 573251

## Como executar

1. Abra o arquivo `Ai chat _citizen` no Google Colab.
2. No menu de segredos do Colab, cadastre uma chave válida da OpenAI com o nome `OPENAI_API_KEY`.
3. Autorize o notebook a utilizar esse segredo.
4. Execute a célula de instalação e importação das bibliotecas.
5. Quando aparecer a solicitação de upload, selecione o arquivo `1CC-documentos_de_referencia.zip`, disponível neste repositório.
    
É necessário ter conexão com a internet e uma chave válida da API OpenAI. O uso da API pode gerar custos.

O arquivo ZIP precisa ser enviado ao Colab a cada nova sessão de execução. Não é necessário descompactá-lo manualmente.

## Problema identificado

Muitas pessoas encontram dificuldades para compreender informações sobre documentos pessoais e serviços públicos.

A linguagem burocrática, os procedimentos complexos e as dificuldades de navegação podem tornar a busca por informações mais complicada.

## Solução desenvolvida

Foi desenvolvido um chatbot capaz de receber perguntas em linguagem natural e apresentar informações de maneira organizada, utilizando sete fichas de referência.

O sistema possui:

- Menu com categorias de documentos.
- Campo para perguntas livres.
- Respostas com orientações e referências.
- Validação de entradas inadequadas.
- Proteção básica contra o uso indevido de dados pessoais.
- Verificações contra algumas tentativas de prompt injection.
- Avisos sobre as limitações do protótipo.

## Tecnologias utilizadas

- Python
- Google Colab
- LangChain
- GPT-4o-mini
- API OpenAI
- Pandas
- Graphviz
- Arquivos Markdown

## Documentos utilizados

O assistente consulta sete fichas fictícias:

- FC-01 — RG
- FC-02 — CPF
- FC-03 — Título de eleitor
- FC-04 — Carteira de trabalho
- FC-05 — Certidões
- FC-06 — CNH
- FC-07 — Regras gerais de atendimento e acessibilidade

As fichas são organizadas em arquivos Markdown e utilizadas como fonte de informação do agente.

## Avaliação com Golden Dataset

Foram utilizadas as 26 perguntas obrigatórias do enunciado para avaliar o chatbot com o método LLM-as-a-Judge.

| Resultado | Antes | Depois |
|---|---:|---:|
| Respostas corretas | 24 | 24 |
| Respostas incorretas | 2 | 2 |
| Erros técnicos | 0 | 0 |
| Taxa de acerto | 92,31% | 92,31% |

A versão melhorada apresentou uma correção em um teste de resistência a prompt injection, mas não aumentou o percentual geral de acertos.

Os resultados automáticos devem ser complementados por conferência manual.

## Testes de usabilidade

Foram realizados testes com cinco participantes externos ao grupo.

Cada participante realizou três tarefas, totalizando 15 execuções.

### Resultados

- **Taxa de acerto:** 100% (15 de 15 tarefas).
- **Tempo médio geral:** 40,2 segundos por tarefa.
- **Facilidade média de utilização:** 4,56/5.
- **Quantidade de participantes:** 5.

Os resultados indicaram uma avaliação positiva, com oportunidades de melhoria principalmente na navegação do menu.

## Limitações

O Citizen Assist AI possui algumas limitações:

- As informações são fictícias e não substituem fontes oficiais.
- O chatbot não realiza agendamentos ou emissão de documentos.
- Não acessa bancos de dados oficiais.
- Depende da API OpenAI para gerar respostas.
- As proteções contra dados pessoais e prompt injection não são infalíveis.
- A interface depende dos recursos de visualização do Google Colab.
- O avaliador automático também pode apresentar erros.

O projeto deve ser utilizado apenas para fins educacionais.

## Links 

Google Colab: https://colab.research.google.com/drive/1mt2W-n2MrvHQ_EG8YYr1Zccan9-mR2rQ?usp=sharing
