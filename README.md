# Desafio para processo seletivo de estágio SHARENERGY 2020
   Esse repositório se destina aos interessados em participar do processo seletivo para estagiários da SHARENERGY 2020. As vagas são voltadas para desenvolvimento de aplicação para Web.

## Sobre a SHARENERGY
Acreditamos que as energias renováveis terão um lugar dominante em nossa economia pelo resto de nossas vidas. Trabalhamos no sentido de ampliar o impacto positivo que as energias renováveis podem ter no meio ambiente e nas nossas vidas. O sucesso da SHARENERGY é resultado de nossa equipe apaixonada, juntamente com nosso compromisso de oferecer a melhor solução.

## Sobre a vaga
Já pensou em potencializar o setor que mais cresce na galáxia e trabalhar com uma solução que utiliza tecnologia web de ponta, altamente distribuída com foco em performance e disponibilidade? 👀

Os desenvolvedores da Sharenergy são responsáveis por criar e manter aplicações para clientes internos e externos, prover soluções escaláveis, resilientes e altamente disponíveis que sustentem picos de acesso além de atuar como referência técnica e tutores de outros desenvolvedores. Procuramos por pessoas dinâmicas e que queiram estar aprendendo sempre. Nossa equipe é jovem, motivada e estamos sempre em busca de soluções criativas para alcançar os resultados que nossos clientes esperam. Se você tem esse perfil, é autoconfiante e tem facilidade para lidar com desafios diários, essa vaga é para você!

## O desafio
   Criar uma aplicação para Web que atenda às demandas listadas abaixo. O aplicativo deve apresentar uma interface amigável, bonita e limpa, na qual o usuário possa navegar por meio botões para obter suas informações de interesse.
### Contexto
   No ramo da produção de energia fotovotaica, há a modalidade de produção compartilhada. Nessa modalidade, diferentes pessoas investem na construção de uma mesma usina fotovoltaica e dividem o retorno finaceiro referente à energia gerada. A aplicação desenvolvida no desafio visa gerenciar as informações de produção de usina fotovoltaica e de seus clientes (investidores).
### Demanda 1: visualização de dados de uma usina fotovoltaica
   A aplicação deve ler os dados contidos no objeto [dadosUsina.json](dadosUsina.json), que contém informações de um dia de produção de uma usina fotovotaica. Em seguida, a aplicação deve plotar os dados em um gráfico de uma variável de interesse (tensão, corrente, potência ou temperatura) em função do tempo. O aplicação deve plotar apenas uma variável por vez e possuir uma opção que permita o usuário escolher qual variável será mostrada. Para tanto, pode-se utilizar, por exemplo, uma lista suspensa ou um radio.
### Demanda 2: gerenciamento de clientes
   A aplicação deve ser capaz de gerenciar os dados dos clientes da usina fotovoltaica. Para esse desafio, são fornecidos dados fictícios de clientes no objeto [dadosClientes.json](dadosClientes.json), que devem ser usados para inicializar o banco de dados de clientes. A aplicação deve possuir recursos básicos de CRUD (Create, Read, Update, and Delete) de modo que seja possível adicionar e deleter clientes, editar os dados de um cliente específico e exibir as informações de todos os clientes.
### Demanda 3: receita de clientes
   A aplicação deve estimar a receita obtida por cada cliente oriunda da energia produzida pela usina fotovoltaica no dia. Primeiramete, a aplicação deve calcular energia produzida no dia usando as informações de potência em função do tempo disponíveis no objeto [dadosUsina.json](dadosUsina.json). Lembre-se que, fisicamente, a potência P (kW) é a derivada no tempo t (h) da energia E (kWh), P = dE/dt. Portanto, a energia gerada pode ser calculada a partir da potência por: 
      
   ![Equação para ΔE](equation.jpg)
   <!--
      Imagem gerada pelo site: http://www.sciweavers.org/free-online-latex-equation-editor
      Foi usado o comando LaTeX: " \Delta E = \int_{t_0}^{t_f}P(t)dt  \approx \Delta t  \sum_{i = 1}^{N-1} P(t_i) "
      Font: Arev (padrão), Font size: 12 (padrão)
   -->
   Em que ΔE é a energia gerada (kWh), t<sub>0</sub> é o instante de tempo inicial (h), t<sub>f</sub> é o instante de tempo final (h), Δt é o intervalo de tempo em que os dados foram amostrados (h), i indica a posição do dado no registro (i = 1, ..., N) e N é o número total de dados amostrados.  
   De posse dos valores da energia gerada (ΔE) e do preço da energia (considere R$0,95 / kWh), a receita total pode ser facilmente obtida. Por fim, a receita de cada cliente pode ser calculada com base no percentual de cada da usina. No caso dos dados de clientes fornecidos, essa informação está na chave "percentualUsina" do objeto [dadosClientes.json](dadosClientes.json).
### Aprimoramentos (opcional)
   A aplicação do desafio pode ser aprimorada com recursos pensados por você. A seguir, estão listadas algumas sugestões:
* Documentação
* Responsividade
* Contas de usuário
   * Proteção contras modiificações de pessoas não autorizadas
* Estatística descritiva dos dados dos gráficos (por exemplo, média, desvio-padrão, mínimo, máximo, etc.)
* Adicionar mais campos aos formulários de criação e edição de clientes.
* Implementação de fórmula mais precisa de integração numérica para o cálculo de ΔE
* Realizar validação dos dados 
### Quais ferramentas posso usar?
   Não será especificado... código que já faça o mesmo...
   Não obstante. usar as mesmas ferramentas que trabalhamos será um diferencial. 
### Mas, afinal, quais ferramentas a Sharenergy utiliza?
   Atualmente, nossas aplicações são desenvolvidas usando a plataforma [Meteor JS](https://www.meteor.com/). Mais especificadamente, nossas aplicações se caracterizam por:
* Gerenciador de pacotes: [npm](https://www.npmjs.com/get-npm)
* Para back-end: [Node.js](https://nodejs.org/en/)
* Banco de dados: [MongoDB](https://www.mongodb.com/) do lado do servidor e [Minimongo](https://guide.meteor.com/collections.html) do lado do cliente (cache)
* Validação de dados: [Schema-utils](https://www.npmjs.com/package/schema-utils) 
* Framework para front-end: [React JS](https://pt-br.reactjs.org/)
* UI: [CSS 3](https://www.w3.org/Style/CSS/), [Material-UI](https://material-ui.com/pt/) e [Reflexbox](https://rebassjs.org/reflexbox/)
* Gráficos: [Victory](https://formidable.com/open-source/victory/)
* Roteamento: [react-router-dom](https://www.npmjs.com/package/react-router-dom)
## O que entregar?
   Esperamos de você duas entregas: o código da aplicação no Git-Hub e um vídeo explicativo no YouTube 
### Instruções sobre aplicação
   Clone esse repositório. Fetch... branch... request pull...
   Incluir arquivo de texto listando todas as dependências usadas e instrução de instalação/uso da aplicação criado.
### Instruções sobre vídeo explicativo no YouTube
   O vídeo duração aproximada de 5 min... não indexado...  link em arquivo...
   Não é necessário mostrar sua face na vídeo, embora seja bom.
### Prazo limite de entrega
   O envio do que foi solicitado deve ser feito até o dia XX/YY/2020.
