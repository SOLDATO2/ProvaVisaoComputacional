# ProvaVisaoComputacional

Aluno: Felipe Porto Caldeira do Nascimento (28628632)

# Descrição do Problema

Neste código, abordei problemas básicos como a aplicação de filtro, extração de caracteristicas e a classificação de imagens através de CNNs

# Tecnicas utilizadas

Para a aplicação de filtros e redimensionamento, foram aplicadas:

Redimensionamento inicial para 128x128, seguido de um gaussianBlur para borrar a imagem. Em um contexto real, o Gaussian blur pode ser utilizado para reduzir os ruidos de uma imagem como uma técnica de pré-processamento para outro filtro, como por exemplo: Thresholding adaptativo que é sensivel a ruidos. Já o resize pode ser utilizado para diminuir o tamanho da imagem para economizar poder computacional.

Equalização de histograma, onde as imagens originais foram convertidas para uma escala de cinza e então aplicadas em sequência a equalização. Esse filtro pode ser util para reduzir o contraste em areas muito claras e similar para áreas muito escuras, sendo assim, equalizando a imagem.

Para a extração de caracteristicas, as imagens foram convertidas para a escala de cinza e então foi utilizado o ORB para extrair pontos de interesse. O ORB foi escolhido preferencialmente devido a sua velocidade, já que o ORB é mais rápido que outros extratores de caracteristicas SIFT o que pode ser importante para aplicações de tempo real.

A extração de caracteristicas é util principalmente para comparar imagens e consequentemente, classificar elas.

Para a aplicação de IA, o dataset foi utilizado um dataset para classificação de cachorros e gatos onde o dataset foi dividido em 80% para treinamento e 20% para validação de acuracia. Foi utilizado CNNs devido ao seu forte vies em extrair caracteristicas de imagens devido aos "kernels" que escaneam a imagem e extraem caracteristicas de diferentes porções da imagem


# Resultados obtidos

Para a aplicação de filtros, foram obtidas 12 imagens (6 imagens de gatos e 6 de cachorros) em que foram aplicados filtros como GaussianBlur e Equalização de histograma e tambem um redimensionamento.

Para o treinamento de IA foi utilizado CNNs para treinar um modelo capaz de classificar imagens onde possuem Cachorros ou Gatos, o modelo obteu as seguintes acuracias depois de treinar por 3 épocas:

Acuracia: 65.72%
Precisão: 67%
Recall: 66%
F1 Score: 65%


# Tempo total gasto

O tempo total gasto para o desenvolvimento de todo código (criação do código dos filtros até o treinamento e teste da IA) foi de aproximadamente 2 horas e 30 minutos.



# Dificuldades encontradas

Durante o desenvolvimento, a principal dificuldade encontrada foi o treinamento do modelo. Para o modelo atingir niveis elevados de acuracia é necessário treinar o modelo por mais épocas. O modelo atual foi treinado por 3 épocas, gerando uma acuracia menor que desejavel. Para aumentar a acuracia, certamente seria necessário treinar o modelo por mais épocas, porém, infelizmente devido ao tempo limitado e poder de processamento disponivel, apenas o modelo foi treinado por apenas 3 épocas.

Para melhorias futuras, para melhorias futuras é interessante incrementar o numero de épocas para o treinamento do modelo e com base nos resultados, avaliar se existe a necessidade da implementação de outras tecnicas como o incremento de normalização de batchsize, data augmentation no dataset ou até mesmo a expansão da arquitetura do modelo.
