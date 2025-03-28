# Atlas das grades DNGS do Brasil, parte 1 - Grades Científicas
O Atlas é um documento importante para se entender e utilizar as grades DNGS, está [disponível neste Gdoc](https://docs.google.com/document/d/1g6hSGvYh8of1qNRCccEMcS1aG3DA8Ji2ebZZ4XR34iU/). Neste repositório git temos todos os subsídos para se reproduzir as ilustrações da documentação, construída com suporte do QGIS. Também fazemos uso do site de apoio, para acessar as células da grade; por exemplo https://AFA.codes/BR+d1

O QGIS é utilizado para renderizar os níveis das grades científicas, permitindo padronizar a confecção de imagens exemplos como a ferramenta de "layout".

Utilizando o QGIS, foram renderizadas camadas de grades hierárquicas, partindo do nível 0 até o nível 7,5. O objetivo foi representar visualmente a relação hierárquica entre os níveis, garantindo que cada nível fosse exibido juntamente com seu nível anterior, evidenciando a subdivisão das células.

## Instruções

Para isso, foram aplicados estilos diferenciados:\
O nível atual recebeu preenchimento com gradiente de cores e rótulos contendo sua codificação.\
O nível anterior foi representado apenas com contorno e rótulos, destacando a hierarquia entre as células.

Além disso, na imagem de representação isolada do nível atual, uma célula específica foi destacada com cor diferenciada para enfatizar sua identificação.\
Esse método permite uma visualização clara e organizada da hierarquia das grades, auxiliando na interpretação espacial da subdivisão das células.

Para representar as células de grade anterior sem preenchimento, configura-se a simbologia para representar os polígonos com contornos simples ou sem preenchimento

Para representar as células da grade atual com preenchimento de gradiente e destaque na célula de interesse, basta criar simbologia baseada em regra, definindo cqual célula destacar com base no seu código, conforme exemplo:

![Exemplo de simbologia](/exemplos/simbologia.jpg)

Os rótulos pdem ser configurados conforme o tamanho de texto, para isto basta escolher em tamanho conforme exemplo a seguir:

![Exemplo de rótulo](/exemplos/rotulos.jpg)

Uma boa solução para destacar o texto foi aplicar o buffer em contraste com a cor do texto, conforme a imagem abaixo:

![Exemplo de buffer no rótulo](/exemplos/buffer_rotulo.jpg)

Além disso, conforme o avanço dos níveis da grade, foi necessário o aumento de escala e portanto foi implementado uma modificação na representação, apresentando um estilo de linha tracejada para destacar a subdivisão de células entre nível anterior e atual.
Desta forma a confecção de exemplos foi realizada neste padrão, conforme o seguinte exemplo:
![Exemplo de padrão tracejado das grades](/img )

Todas as configurações utilizadas para produção dos exemplos do Atlas estão armazenadas em um arquivo em formato geopackage, contendo também as geometrias das grades geradas, juntamente com suas configurações de renderização.
Link do Geopackage:![URL do geopackage](/link)

## Orientações para uso do Geopackage

O geopackage é um formato de arquivo aberto para representação de dados geoespaciais adotado pela Open Geospatial Consortium que funciona como um contêiner SQL, e permite o armazenamento em um único arquivo o projeto do QGIS, seus estidos e camadas e também configurações de layout de impressão.

Para utilizá-lo no QGIS e abrir o projeto salvo, deve-se selecionar a opção projeto e seguir o seguinte exemplo:
![Orientação para abrir o projeto geopackage](/exemplos/projeto_gpkg.jpg)

Ao selecionar as opções acima, uma aba solicitará a busca pelo arquivo geopackage, o qual deve ser escolhido, e desta forma aparecerá os projetos salvos dentro do arquivo:
![Orientação para abrir o projeto geopackage](/exemplos/projeto_gpkg1.jpg) 
