# desafio-renova
O desafio proposto tem como objetivo analisar e tratar os conjuntos de dados referentes às eleições municipais de 2020 em São Paulo, focando nas bases "Perfil do eleitorado" e "Resultados". Para avaliar habilidades técnicas de tratamento de dados, estruturação, criação de consultas e documentação. 

Esse código realiza o tratamento e análise dos dados eleitorais do estado de São Paulo para as eleições de 2020. Ele abrange a limpeza dos dados, a geração de consultas e a criação de tabelas específicas.

Cada parte do código é explicada com comentários detalhados. Os principais passos incluem:

Leitura e tratamento dos dados das eleições e do perfil eleitoral.
Realização de consultas para analisar o desempenho dos candidatos, incluindo candidato mais votado, votos por partido, entre outros.
Análise do perfil do eleitorado para candidatos a prefeito.
Cálculo das abstenções divididas por gênero.
O resultado de cada consulta é salvo em arquivos CSV para posterior análise. O código demonstra o uso de técnicas de limpeza, agregação e análise de dados. Projeto feito no Jupyter Notebook utilizando a linguagem Python. 

**Passo a Passo: Tratamento e Análise de Dados Eleitorais**

Aqui está um guia detalhado que descreve cada passo do processo de tratamento e análise de dados eleitorais para as eleições de 2020 no estado de São Paulo:

1. **Preparação Inicial:**
   - Certifique-se de ter os arquivos de dados `SP_turno_1.csv` (resultados da eleição) e `perfil_eleitorado_2020.csv` (perfil do eleitorado) no mesmo diretório do seu código.

2. **Importação de Bibliotecas:**
   - Importe as bibliotecas necessárias para a análise de dados, como `pandas` e `IPython.display`.
   - Obs: Código pode ser usado tanto em IDEs de sua escolha, quanto no Jupyter Notebook. O projeto foi desenvolvido no Jupyter. 

3. **Tratamento dos Dados das Eleições:**
   - Carregue o arquivo `SP_turno_1.csv` em um DataFrame chamado `df_sp`.
   - Remova colunas desnecessárias usando a lista `remover_colunas_sp`.
   - Salve o DataFrame tratado de volta no arquivo `SP_turno_1.csv`.

4. **Tratamento dos Dados do Perfil Eleitoral:**
   - Carregue o arquivo `perfil_eleitorado_2020.csv` em um DataFrame chamado `df_perfil`.
   - Remova linhas com valores nulos na coluna `QT_ELEITORES_PERFIL`.
   - Converta a coluna `QT_ELEITORES_PERFIL` para o tipo de dado inteiro.
   - Remova colunas desnecessárias usando a lista `remover_colunas`.
   - Filtre apenas os dados da UF São Paulo.
   - Remova a coluna `SG_UF`.
   - Salve o DataFrame tratado de volta no arquivo `perfil_eleitorado_2020.csv`.

5. **Consulta 1: Município com Maior Votação para Bruno Covas:**
   - Filtrar os resultados para o candidato "BRUNO COVAS".
   - Encontrar o município onde ele obteve mais votos.
   - Imprimir o resultado.

6. **Consulta 2: Candidato Mais Votado em Cada Município:**
   - Agrupar os resultados por município e encontrar o candidato mais votado em cada um.
   - Criar um DataFrame `df_resultado2` com as informações relevantes.
   - Salvar o DataFrame em `resultado_consulta2.csv`.

7. **Consulta 3: Perfil do Eleitorado que Mais Votou em Cada Candidato:**
   - Realizar um merge entre os resultados e o perfil eleitoral usando o nome do município.
   - Agrupar os dados por candidato e perfil eleitoral para encontrar o perfil com mais votos.
   - Criar um DataFrame `df_resultado3` com as informações relevantes.
   - Salvar o DataFrame em `resultado_consulta3.csv`.

8. **Consulta 4: Total de Abstenções por Zona Eleitoral e Candidato:**
   - Realizar um merge entre os resultados e o perfil eleitoral usando o nome do município.
   - Agrupar os dados por zona eleitoral e candidato para calcular o total de abstenções.
   - Ordenar os resultados pela zona e pelo total de abstenções.
   - Criar um DataFrame `df_resultado4` com as informações relevantes.
   - Salvar o DataFrame em `Abstencoes_por_zona.csv`.

9. **Consulta 5: Candidato Mais Votado em Toda a Eleição:**
   - Encontrar o candidato mais votado em toda a eleição.
   - Imprimir o nome do candidato e o número de votos.

10. **Consulta 6: Total de Votos por Partido:**
    - Agrupar os resultados por partido e calcular o total de votos.
    - Ordenar os resultados pelo total de votos em ordem decrescente.
    - Salvar os resultados em `total_votos_por_partido.csv`.

11. **Consulta 7: Total de Votos por Gênero para Eduardo Suplicy (Candidato a Prefeito):**
    - Filtrar os resultados para o candidato "EDUARDO SUPLICY" (certifique-se do nome correto).
    - Realizar um merge entre o perfil eleitoral e os resultados para obter dados de gênero.
    - Calcular o total de votos por gênero.
    - Salvar os resultados em `total_votos_por_genero_candidato.csv`.

12. **Consulta 8: Candidatos a Vereador Mais Votados por Zona Eleitoral:**

    - Filtrar os resultados para candidatos a vereador.
    -Agrupar os resultados por zona eleitoral e encontrar o candidato mais votado em cada uma.
    - Salvar os resultados em candidatos_mais_votados_vereadores_zona.csv.


13. **Consulta 9: Candidato a Prefeito Mais Votado por Zona Eleitoral:**

    - Filtrar os resultados para candidatos a prefeito.
    - Agrupar os resultados por zona eleitoral e encontrar o candidato mais votado em cada uma.
    - Salvar os resultados em prefeito_mais_votados_zona.csv.


14. **Consulta 10: Perfil do Eleitorado dos Candidatos a Prefeito:**

    - Filtrar os resultados para candidatos a prefeito.
    - Realizar um merge entre o perfil eleitoral e os resultados para obter dados de perfil.
    - Calcular o total de votos por perfil do eleitorado para cada candidato.
    - Salvar os resultados em arquivos CSV separados para cada candidato.


15. **Consulta 11: Abstenção Dividida por Gênero:**

Realizar um merge entre os resultados e o perfil eleitoral usando o nome do município.
Calcular o total de abstenção por gênero em toda a eleição.
Salvar os resultados em total_abstencao_genero.csv.
