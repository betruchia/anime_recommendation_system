## anime_recommendation_system
finalproject_ironhack_daft

![imagem de one piece](https://cdn.vox-cdn.com/thumbor/xBIBkXiGLcP-kph3pCX61U7RMPY=/0x0:1400x788/1200x800/filters:focal(588x282:812x506)/cdn.vox-cdn.com/uploads/chorus_image/image/70412073/0377c76083423a1414e4001161e0cdffb0b36e1f_760x400.0.png)

### ideia e fonte de dados

- competição do kaggle:
  https://www.kaggle.com/competitions/anime-recommendation-system-by-tah

### proposta

- usando arquivos da competição, que contêm informações do site https://myanimelist.net/ (dados sobre os animes, como avaliações feitas pelos usuários), quis criar um sistema de recomendação para uso geral.

### big data

- os arquivos continham avaliações de 325772 usuários sobre 17562 animes - resultando em **57633278** notas! para lidar com tanta informação, precisei usar matriz esparsa, o que trouxe a dificuldade da não-visualização dos dados.

### distâncias limitadas

- como precisei calcular a distância dentro da matriz esparsa, não pude usar a distância de chebyshev, como gostaria. usei, então, a distância euclidiana.

### fatores demais

- queria usar o fator distância para aferir pesos às avaliações de todos os usuários, mas, para isso, precisaria da matriz densa :/ então, selecionei somente os 100 usuários mais próximos.

### dois pesos, duas medidas

- para espassar mais as diferenças entre notas e entre distâncias, elevei ambas ao quadrado.

### top10

- retorno da tabela com os 10 animes mais bem avaliados pelas pessoas com gostos similares, excluindo animes já avaliados pelo novo usuário.

...

### próximos passos

- mudar a função de soma das notas para algo que considere a frequência com que cada anime aparece na lista dos 100 mais próximos.
- colocar o sistema no streamlit, para maior interatividade do usuário, e com uma interface mais amigável.
- no streamlit, resolver a questão do número de animes, caso persista a ideia de usar inserção via selectbox.
- pensar nalguma forma de usar outras informações para aprimorar o sistema (como gênero do anime, ou se os usuários não terminaram de assistir/planejam assistir, etc).
- tentar ampliar ao máximo o número de próximos, a fim de viabilizar que haja recomendações, por mais avaliações que o novo usuário forneça.

![imagem de naruto](https://static.marriedgames.com.br/82bae879-naruto-classico-e-naruto-shippuden-fillers.jpg)