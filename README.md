
# Projeto de Linhas de Transmissão com Simulated Annealing

<p align="justify">
Projeto de otimização da distribuição de torres de linhas de transmissão considerando restrições mecânicas, perfil do terreno, altura mínima do cabo, custo de implantação e classificação automática das torres.
</p>

---

# 1. Visão Geral

<p align="justify">
Este projeto implementa um algoritmo de otimização baseado em <b>Simulated Annealing (SA)</b> para definir automaticamente a melhor localização das torres de uma Linha de Transmissão (LT).
</p>
<p align="justify">
O modelo busca minimizar o custo total da implantação respeitando simultaneamente diversas restrições técnicas utilizadas em projetos reais de transmissão de energia elétrica.
</p>
Durante a otimização são considerados:

- comprimento total da LT;
- distância mínima e máxima entre torres;
- perfil do terreno;
- altura de fixação dos cabos;
- distância mínima cabo-solo;
- classificação automática entre torres de suspensão e ancoragem;
- penalizações para soluções inviáveis;
- custo de implantação.
<p align="justify">
Ao final, o algoritmo produz uma configuração otimizada contendo a posição das torres, altura de fixação dos cabos, tipo de cada estrutura e custo estimado da solução.
</p>



# 2. Objetivos

<p align="justify">
O objetivo principal é minimizar o custo total da linha de transmissão mantendo todas as restrições físicas e mecânicas da infraestrutura.
</p>
<p align="justify">
A solução procura reduzir o número de torres sem comprometer a segurança da instalação, garantindo que todos os vãos permaneçam dentro dos limites especificados e que o cabo mantenha distância adequada do terreno em todo o percurso.
</p>



# 3. Características do Projeto

<p align="justify">

O projeto contempla:

- geração automática do perfil do terreno;
- cálculo dos vãos entre torres;
- cálculo aproximado da catenária utilizando modelo parabólico;
- verificação automática da distância mínima cabo-solo;
- avaliação do ângulo entre torres consecutivas;
- classificação automática entre torres de suspensão e ancoragem;
- função objetivo baseada em custos e penalidades;
- otimização utilizando Simulated Annealing;
- visualização gráfica da solução encontrada;
- gráfico de convergência do algoritmo.

</p>

-

# 4. Modelagem do Problema

<p align="justify">
Cada solução candidata representa um conjunto de torres distribuídas ao longo da linha de transmissão.
</p>

Cada torre possui:

- posição ao longo da LT;
- altura de fixação do cabo;
- classificação estrutural.

A função objetivo combina:

- custo das torres;
- custo dos cabos;
- penalizações por violações das restrições;
- penalizações para excesso de torres;
- penalizações para alturas excessivas.
<p align="justify">
O processo iterativo do Simulated Annealing explora diferentes configurações até encontrar uma solução de menor custo.
</p>



# 5. Restrições Consideradas

<p align="justify">

O algoritmo verifica automaticamente:

- vão mínimo permitido;
- vão máximo permitido;
- distância mínima entre cabo e terreno;
- limite máximo do ângulo do cabo;
- altura mínima de fixação;
- altura máxima de fixação;
- classificação correta das torres quando ocorre mudança significativa de direção.
</p>
<p align="justify">
Caso qualquer restrição seja violada, grandes penalidades são aplicadas à função objetivo.
</p>



# 6. Perfil Otimizado da Linha de Transmissão

<p align="center">


<p align="center">
  <img src="https://github.com/rodfloripa/Projeto83/blob/main/fig1.png">
</p>

</p>

<br><br>



# 7. Fluxo do Algoritmo

<p align="justify">

O processo de otimização segue as seguintes etapas:

1. geração do perfil do terreno;
2. criação de uma solução inicial;
3. avaliação do custo;
4. geração de soluções vizinhas;
5. aceitação ou rejeição da nova solução conforme o critério do Simulated Annealing;
6. redução gradual da temperatura;
7. armazenamento da melhor solução encontrada.

</p>



# 8. Tecnologias Utilizadas

<p align="justify">

O projeto foi desenvolvido utilizando:

- Python
- NumPy
- Matplotlib
- Math
- Random

</p>



# 9. Resultados

<p align="justify">

Após o processo de otimização o algoritmo fornece automaticamente:

- número de torres;
- posição de cada torre;
- altura de fixação;
- classificação estrutural;
- comprimento dos vãos;
- custo total estimado;
- gráfico da configuração final;
- curva de convergência do Simulated Annealing.
</p>
<p align="justify">
Esses resultados permitem avaliar diferentes configurações de projeto e identificar soluções economicamente mais eficientes sem violar as restrições de engenharia.
</p>



# 10. Aplicações

<p align="justify">
O método pode ser aplicado em estudos preliminares de implantação de linhas de transmissão, análise de alternativas de traçado, planejamento de infraestrutura elétrica, comparação de projetos, apoio à engenharia de transmissão e desenvolvimento de ferramentas computacionais para otimização de ativos energéticos.
</p>



# 11. Conclusão

<p align="justify">
A utilização do Simulated Annealing mostrou-se adequada para resolver um problema de otimização altamente restritivo e não linear, permitindo explorar inúmeras configurações possíveis de posicionamento das torres sem necessidade de métodos determinísticos complexos.
  </p>
<p align="justify">
Ao integrar informações do terreno, limitações mecânicas, classificação estrutural das torres e custos de implantação, o modelo produz soluções consistentes que equilibram desempenho técnico e viabilidade econômica. Essa abordagem pode ser expandida para cenários reais incorporando modelos digitais de terreno, diferentes tipos de cabos, condições climáticas, restrições ambientais e múltiplos critérios de projeto, tornando-se uma ferramenta de apoio para estudos avançados de planejamento de linhas de transmissão.
</p>

