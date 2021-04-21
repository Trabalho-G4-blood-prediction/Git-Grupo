# Contexto

O problema pode ser inserido no contexto dos desafios gerais relacionados a doação de sangue, mais especificamente, na necessidade de se equilibrar oferta de sangue em relação a demanda ao longo do tempo. A questão se torna especialmente complexa considerando que as doações de sangue seguem variações sanzonais causadas por, dentre outros fatores, ocorrência de feriados, mudanças de estações do ano, eventos como campanhas de vacinação (BIANCO, 2013, p. 231), além de feriados bancários e campanhas de doação (OLIVEIRA et. al., 2013). Esses fatores devem ser considerados para fins de prever doações futuras, auxiliando no uso racional de recursos escassos na coleta, distribuição e armazenamento de sangue de maneira adequada ao longo do ano.

Outra questão relevante é a dos diferentes tipos de doadores de sangue. Doadores de sangue podem ser classificados como *recorrentes* e de *primeira vez* o que pode afetar o número de novas doações e o tempo entre doações, com doadores recorrentes retornando de maneira mais frequente e realizando mais doações (DE ALMEIDA NETO, 2012, p. 4-6). Deve-se levar essa diferença em consideração na hora em vista de resolver o desafio em tela.

Finalmente, devemos considerar o contexto geral de doação de sangue em Taiwan. Apesar de algumas dificuldades recentes relacionadas a falta de sangue do tipo A (DEAETH, 2019), o país parece apresentar boas taxas de doação de sangue quando comparado globalmente (EVERINGTON, 2018; TAIWAN BLOOD SERVICES FOUNDATION, 2013). Ainda assim o envelhecimento da população pode demandar maior o volume de sangue coletado para futuro próximo.

# **Machine Learning Canvas**
 
## Análises Propostas
 
Partindo dos dados disponibilizados e das informações obtidas na imersão, nós pretendemos utilizar de algorítimos de classificação para prever a probabilidade de se doar ou não sangue em março de 2007.

## Fontes de Dados
 
Nossa base de dados vem do repositório de Machine Learning da UCI. Os dados foram coletados por veículo de doação de sangue em Taiwan, organizados pela “Taiwan blood services foundation” (Fundação de hemo-serviços taiwanesa), em diferentes universidades.
 
## Recursos Técnicos
 
Python: Sklearn, Matplot, NumPy, Pandas.
Google Drive: Para juntar as informações e dados de pesquisas.
Trello: Para a organização das atividades do grupo.
Algoritmos: Ada Boosting, Arvore de decisão, Floresta Aleatória, k-means, Rede Neural, Regressão Logística e SVM.
Ferramenta para visualização dos dados: Python
 
## AI values
 
A partir de nossa base de dados, bem como das ferramentas utilizadas, temos por objetivo criar um modelo capaz de prever corretamente a reincidência na doação de sangue. Para isso será necessário: 

1.  Analisar, limpar, separar e normalizar os dados.
2.  Testar distintos algorítimos, com hiperparâmetros diversos, utilizando dados de treinamento e validação. A partir disso vamos escolher os hiperparâmetros que apresentarem melhores melhores resultados segundo certas métricas (mas priorizando a "pontuação F1" por melhor representar o desbalanceamento dos dados).
3.  Testar todos os algorítimos com base nos dados de teste e escolher aquele que apresentar melhor performance.
4.   Entrega dos resultados.
 
 
## Principais Riscos
 
Os principais riscos estão na má alocação de recursos causada por erros de identificação das probabilidades reais. Se as probabilidades calculadas forem superiores às reais, o veículo de coleta pode acabar comprando e trazendo mais material do que necessário; se elas forem abaixo da realidade, o veículo pode trazer menos recursos do que o necessário para as coletas. Em suma: há o risco de que erros em previsões se transformem em problemas (de desperdício ou escassez de material) na coleta de sangue.   

Outro risco consiste no atraso da entrega dos resultados. Isso pode ocorrer por diversos fatores: necessidade de coleta de novos dados, erros de coletas nos dados fornecidos pelo stakeholder, problemas técnicos, dentre outros.

Há também riscos técnicos de os dados serem insuficientes ou inadequados para modelagem. Isto é, podemos não conseguir treinar modelos adequados para a realização de previsões.
 
## Principais Stakeholders
 
*Nesse caso em específico*, o stakeholder interessado é o "Blood Transfusion Service Center", responsável pela coleta de sangue, que deseja saber se alguém vai ou não doar na sua próxima ida ao campus (prevista para março de 2007).
 
## Canal de Entrega
 
Relatório técnico (Visualização + código)
 
## Métricas de Sucesso
 
 
A partir de nosso modelo, esperamos conseguir prever corretamente pelo menos 70% das doações de sangue em março de 2007. Para tanto, vamos nos utilizar dos recursos disponíveis nas bibliotecas de Python visando ajustar os erros no nosso modelo para aprimorar nossas predições. 
 
Por fim, pretendemos avaliar os modelos de classificação segundo algumas métricas. Estas são: a acurácia (total de classificações corretas); a precisão (total de classificações positivas verdadeiras); a precisão (total de classificações positivas verdadeiras sobre o total de classificações positivas); a sensibilidade/revocação (quantos do total de positivos verdadeiros foram capturados pelo modelo); pontuação F1 macro (a média aritimética das notas F1 por classe) e; área sobre a curva ou AUC (avalia a relação entre especificidade, ou total de negativos verdadeiros sobre negativos pevistos, e revocação) dos modelos testados. 
