# AtlasDNGS-BRp1-Scientific
Atlas das grades DNGS do Brasil, parte 1 - Grades Científicas\
Processo de documentação DNGS com suporte do QGIS

O QGIS é utilizado para renderizar os níveis das grades científicas, permitindo padronizar a confecção de imagens exemplos como a ferramenta de "layout".

Utilizando o QGIS, foram renderizadas camadas de grades hierárquicas, partindo do nível 0 até o nível 7,5. O objetivo foi representar visualmente a relação hierárquica entre os níveis, garantindo que cada nível fosse exibido juntamente com seu nível anterior, evidenciando a subdivisão das células.

Para isso, foram aplicados estilos diferenciados:\
O nível atual recebeu preenchimento com gradiente de cores e rótulos contendo sua codificação.\
O nível anterior foi representado apenas com contorno e rótulos, destacando a hierarquia entre as células.

Além disso, na imagem de representação isolada do nível atual, uma célula específica foi destacada com cor diferenciada para enfatizar sua identificação.\
Esse método permite uma visualização clara e organizada da hierarquia das grades, auxiliando na interpretação espacial da subdivisão das células.

Para representar as células de grade anterior sem preenchimento, configura-se a simbologia para representar os polígonos com contornos simpls ou sem preenchimento

Para representar as células da grade atual com preenchimento de gradiente e destaque na célula de interesse, basta criar simbologia baseada em regra, definindo cqual célula destacar com base no seu código, conforme exemplo:

![Exemplo de simbologia](/exemplos/simbologia.jpg)

Os rótulos pdem ser configurados conforme o tamanho de texto, para isto basta escolher em tamanho conforme exemplo a seguir:

![Exemplo de rótulo](/exemplos/rotulos.jpg)

Uma boa solução para destacar o texto foi aplicar o buffer em contraste com a cor do texto, conforme a imagem abaixo:

![Exemplo de buffer no rótulo](/exemplos/buffer_rotulo.jpg)
