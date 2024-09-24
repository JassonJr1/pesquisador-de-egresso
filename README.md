# O que é Pesquisador de Egressos?

É uma ferramenta Python que serve como uma alternativa gratuita para localizar egressos de universidades no Linkedin. Ela permite que os usuários busquem e se conectem automaticamente com novos perfis no LinkedIn, com base em suas preferências. Esse proejto é uma adaptação do projeto [ConneXion](https://github.com/ethbak/connexion-for-linkedin/tree/main?tab=readme-ov-file).

# Tecnologias

![Static Badge](https://img.shields.io/badge/PYTHON-blue?style=for-the-badge)
![Static Badge](https://img.shields.io/badge/PANDAS-purple?style=for-the-badge)
![Static Badge](https://img.shields.io/badge/TKINTER-gold?style=for-the-badge)
![Static Badge](https://img.shields.io/badge/SELENIUM-green?style=for-the-badge)
![Static Badge](https://img.shields.io/badge/JSON-orange?style=for-the-badge)
![Static Badge](https://img.shields.io/badge/CUSTOM%20SEARCH%20API-red?style=for-the-badge)

# Vídeos
### [Demonstração de Busca](https://youtu.be/oXAYFiZ4hlQ)

# Funcionalidades
### Ferramenta de Busca de Perfis
Utiliza a API JSON do Google Custom Search para permitir que os usuários encontrem perfis do LinkedIn com base em preferências como Cargo, Localização e Universidade. A ferramenta exporta os dados dos perfis para um arquivo Excel, que pode ser usado com a Ferramenta de Automação de Conexões ou salvo para análise posterior. Com uma chave de API do Google, o usuário pode gerar até 1.000 resultados gratuitos por dia.

# Limitações

### Limites da API do Google
O Google limita suas requisições gratuitas da API Custom Search a 100 por dia, resultando em um máximo de 1.000 novos resultados de perfis. Requisições extras podem ser compradas por $5 por cada 1.000 [aqui](https://developers.google.com/custom-search/v1/overview).

### Termos de Serviço do LinkedIn
De acordo com os [Termos de Serviço](https://www.linkedin.com/help/linkedin/answer/a1340567/automated-activity-on-linkedin?lang=en#:~:text=In%20order%20to%20protect%20our,automate%20activity%20on%20LinkedIn's%20website) do LinkedIn, o uso de ferramentas automatizadas de terceiros é proibido. Portanto, os usuários da Ferramenta de Automação de Conexões devem operar por sua própria conta e risco. Se o LinkedIn detectar atividade automatizada prolongada, eles podem desativar temporariamente ou banir as contas dos usuários. O bot toma precauções para minimizar essa possibilidade, incluindo a randomização de intervalos entre atividades, mas ainda assim é importante usar a ferramenta com responsabilidade. Recomenda-se enviar apenas ~30 pedidos de conexão por vez, uma vez por dia. Se uma conta for temporariamente desativada, é recomendável parar de usar a ferramenta por um período prolongado para evitar um banimento permanente.

# Instalação

Pré-requisitos:
1. Instale o [Python / Anaconda](https://docs.anaconda.com/free/anaconda/install/index.html).
2. Baixe o [Google Chrome](https://www.google.com/chrome/).

Passos:
1. Baixe o código-fonte do [repositório]([https://github.com/ethbak/connexion-for-linkedin](https://github.com/JassonJr1/pesquisador-de-egresso/tree/master)).
2. Abra o terminal do seu computador e navegue até a pasta da aplicação.
3. Execute o seguinte comando para instalar as dependências da aplicação:
   ```bash
   pip install pillow numpy pandas selenium requests

4. Inicie a aplicação executando o seguinte comando:
   ```bash
   python main.py

# Uso
1. Localizações (Separadas por vírgula):
Permite ao usuário buscar perfis com base em uma lista de localizações. Os usuários devem inserir uma lista de localizações separadas por vírgula para obter melhores resultados. Não deve estar em branco.
2. Posição (Separados por vírgula):
Permite ao usuário buscar perfis que ocupem uma variedade de cargos. Os usuários devem inserir uma lista de cargos separados por vírgula para obter melhores resultados. Não deve estar em branco.
Campo de Universidade:
Um campo de entrada que permite ao usuário buscar perfis com base na universidade de graduação. O usuário deve inserir o nome da universidade, e a busca será feita com base nesta informação.
3. Local de Saída:
O local do arquivo Excel de saída. Deve terminar com .xlsx e representar um caminho de arquivo válido. Arquivos Excel existentes serão acrescentados, não sobrescritos. Novos arquivos Excel também podem ser criados, desde que o caminho seja válido.
4. Chave de API do Custom Search:
A chave de API JSON Custom Search do Google do usuário. Deve ser uma chave válida. Os usuários podem criar uma chave de API aqui.
5. Caixa de Repetir Consultas:
Quando marcada, termos de busca já utilizados anteriormente serão buscados novamente. É recomendável marcar esta caixa se um período significativo de tempo tiver passado desde a última busca. Quando desmarcada, termos de busca anteriores são ignorados.
