# Project_SharkAttack

## Projeto Ironhack utilizando uma base com informações de ataques de tubarões. Objetivo, criar uma pergunta e através dessa pergunta utilizar a base de dados para encontrar a resposta, para isso, se fez necessário limpar a base de dados utilzandos metodos do python fezendo data cleaning e contruindo as analises.

Pergunta:
### surfistas são mais propensos a receber um ataque fatal de tubarão?


1- sns.heatmap(SA1.isnull(), cbar=False)
>>> Utilizando o heatmap para verificar a incidência de valores nulos.

2- SA1 = SA1.drop(columns=['Case Number','Unnamed: 22', 'Unnamed: 23','href', 'href formula', 'original order', 'pdf', 'Investigator or Source', 'Injury', 'Name','Case Number.1','Case Number.2'])
>>> Removendo colunas que não serão utilizadas na analise.

3- SA2 = SA1.dropna(thresh=10)
>>> Removando valores nulos.

4- SA2 = SA2.rename(columns={'Fatal (Y/N)':'Fatal'})
>>> Renomeando a principal coluna da analise.

5- SA2.columns = [x.strip().lower().replace(' ','_') for x in SA2.columns]
>>> Padronizando os titulos das colunas

6- SA3 = SA2.replace(to_replace={'fatal': {'N ':'N', 'UNKNOWN':'N', 'M':'N', 'y': 'Y', ' N':'N', '2017':'N', 'NaN': 'N', 'surfing':'N'}},value=None)
>>> Organizando a coluna fatal.

7- 
