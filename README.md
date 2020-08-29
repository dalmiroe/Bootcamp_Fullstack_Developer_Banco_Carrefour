# Bootcamp_Fullstack_Developer_Banco_Carrefour

Assuntos estudados no Bootcamp

##- Lógica de programação
  Algoritimo - Sequencia de ações;
  Pseudocódigo - algoritmos descritos de forma estruturada;
  Fluxograma - Forma gráfica de representar a ações - app da internet para criar fluxograma - flowgorithm;
  Protugol - Linguagem de programação para estudo;
  Comandos - Tomadas de decisões, laços de repetição, variáveis, constantes, matrizes e vetores;
  
##- Introdução ao Git e controle de versões.

  Controle de versão - Gerencia o ciclo do código
  Ferramentas - Git/cvs/subversion/tfs
  GIT - Principais comandos via terminal
     git init - incializar o controle para um diretorio
     git clone - obter a estrutura remoto para o local
     git add - adicionar arquivos - add. ou pontou add nome do arquivo
     git commit -m - adicionar comentario ao commit 
     git push - publicar as aterações no repositorio remoto
     git (baixar)pull - atualiza o repositorio local
     git merge - juntar váris alterações do mesmo arquivos
     git status - informações sobre o repositorio
     git log - informações sobre todas as ações no repositório
     git branch - criação de ramos - principal e a master
     https://git-scm.com/docs - mais informações
     Utilizando os comandos
  Reposotório remoto - Github, gitlab,bitbucket
  
##- Introdução ao GitHub

   git remote add origin - conectar meu repositorio local a um servidor remoto
   Branch - Ramificações - Quebrar o projeto em versões 
      git branch - mostra as branchs
      git branch novaB - cria um nova branch com o nome novaB
      git checkout novaB - cria e ja posiciona na nova branch
      git push origin novaB - atualiza no github a minha nova branch
      git reset HEAD nme-arq. - retirar arq apos add
      git merege - deixar o master atualizada com determinada branch
      git commit --amend - editar msg do ultimo commit
  
  ##- Fundamentos de Arquitetura de Sistema
  
  WebServices - aplicação que serve para fazer integração entre sistema.
    Comunição feita atraves do protocolo http, pode usar a estrutura **SOAP** ou **REST**
    Soap usa xml, wsdl e xsd. 
    Rest usa json
    
  Modelos Monolito x Microserviços
    Monolito é a arquitetura baseada em uma únca aplcação fazendo tudo e gerenciando tudo, acesso a banco, regra de negocios,etc.
    Microserviços, temos várias arquiteturas, mas basicamente é quebrar a aplicação (as regras de negocios) em pequenos serviços e fazer os serviços conversarem e tentar deixar    mais independente possível.
    
  Gerenciamento de erros e volume de acesso
  https://github.com/jeffhsta/fundamentos_arquitetura
 
  ##- A arquitetura de aplicações móveis e internet das coisas
 
  Internet da coisas - Sensores embutidos em objetos (coisas) para conectar a internet e coletar dados
    Desafios - Privacidade e Segurança / Quantidade exponencial de dispositivos na rede / Gerar valor com os dados coletados
    Arquitetura - Baixo consumo de energia, rede de dados limitado, resiliencia, segurança, customização e baixo custo. / Arduino para protótipo, Embarcados equipamentos             profissional, Minicomputadores.
    Protocolo de comunicação - MQTT, mensagem assincrona, Modelo Publish/Subscribe
      Tópico
        protocolo://broker/user identifiier / sensor/position
        mqtt://broker.io/a6g319/gps/position
     Subscribe - escutar o broker
     
  Cloud - Por conta do número grande de dados é necessário a nuvem. 
  
  Estudo de caso
    Arquitetura escolhida - GPS conecta via protocolo MQTT a um BROKER que conecta a um WORKER que armazena em DATA STORE
    Prova de conceito (POC) - APP Android - Eclipse Mosquitto - Node.js - Mysql
    Mínimo produto viável (MVP)- GPS Embarcado - HiveMQ - Akka Scala JVM - Bando de dados noSql - MongoDB
    solução final - vai ter todas as ferramentas de mercado mais profissionais
    
  ##- Arquitetura de dados essencial
 
  Modelo Sustentável - Estruturação, Durabilidade, Velocidade, Controle de acesso e Isolamento.
  Modelo Flat - linha de registros e colunas. Ex. Tabela
  Modelo Hierárquico - Grupos de informações
  Modelo relacional - Tabelas relacionadas
    Tabelas com linhas e colunas e chaves primarias (identificação única) e secundárais (relaciona as tabelas).
    Modelagem conceitual - MER - Modelo entidade e relacionamento
      DER - Diagrama de entidade e relacionamento, demostra graficamento o relacionamento entre as entidades.
        Destaca as entidades fortes (entidades que não dependem de outras), entidades fracas (entidades que dependem de outras), entidades associativas que são geradas com base nos relacionamento n para n. E difinição das cardinalidades.
        Normalização - 1 a 5 formas normais
          Primeira forma normal - Tirando duplicidade de informação através de nova coluna 
          Segunda forma normal - Tirando duplicidade atraves de nova tabela com relacionamento
          Terceira forma normal - Retirada de colunas dependentes
   
  SGDBR-SQL - Sistema gerenciador de banco de dados relacional
  
  Linguagens que controlam o banco de dados
        DDL - Data Definition Language - Controla as tabela, atributos e relacionamentos. Controla os objetos criados
          Ex. Create table....
        DML - Data manipulation Language - Fazer as transformações no ambiente - criação, alteração, exclusão
          Ex. Insert into tabela.....
        DQL - Data Query Languege - Fazer minipulações e consultas no dados
          Ex. select * from .....
          
   Transactions 
    ACID - atomicidade, todas as operações executadas com sucesso.
      Consistência - Unicidade de chaves, restrições de integridade única
      Isolamento - Transações podem acessar simultaneamente os dados
      Durabilidade - Depois do commit, mesmo com erros,queda de nergia, etc. As alterações sejam aplicadas
      
   ## - Conceitos de responsividade e experiência do usuário
   
    UI/UX Interface e experiência do usuário - Briefing, Imersão e Unpack
    
    Wireframes, Grids e Hierarquia - Estrutura, conteúdo, Hierarquia informativa e funcionalidades
    
    Cores - Psicologia das cores
        Cores primárias - Azul, Laranja e Cinza
        Paleta secundária - Cores com significados próprios, as padrões...
        Gradiente ou Degradê - Tons de cinza
        Tipografias - A roupa do seu projeto
        Tipos de fonte
          Serifadas - fontes com pequenos traços - Transfmite o conceito de seriedade e tradição
          Sem serifa (sans - serif) - Fontes sem os traços - mais modernas
          Cursivas - manuscritas ou caligráficas - mais clásicos
          Decorativas - charmar a atenção 
          Tamanho e peso - 16px é um padrão - Peso é a grossura do caracter
    
    Componentes 
      
      Iconografia - icones - Combinar icones com palavras
      Imagens - Captura a atenção 
      Guia de estilo para o projeto - Contem todas as informações do projeto e desta forma ajudar a padronizar o layout - Padrão visual
      
   Processos do mundo real
      Responsividade - O layout se adequar a todos os tipos e tamanho de dispositivos.
      Ferramentas - Google Resize, Windows resize
      Acessibilidade - Possibilitar qq pessoa usar o sistema. 
      Uxdesign.blog.br
   
   Prototipagem - melhora a experiência do usuário, identificar problemas.
      Fidelidada - baixa, méduia ou alta
      
   Bibliografia 
      Medium: ui-lab-school / us-strategy; http://www.ideo.com; https://material.io; youtube: ux lab / ux now; 
      
   ## - Introdução ao domain driven design e padrões de arquitetura
   
    Arquitetura de SW - engloba estrutura, comportamento, necessidades do cliente, depende do ambiente, depende do time, tem um estilo arquetetural.
    O SW tem uma arquitetura.
    Design de SW - Especificação de requisitos, design de alto nivel e design detalhado
    Estilo de Arquitetura - camadas, microserviços, pipes and filter, plugins, client/server, etc
    Padrões de arquitetura - mvc, cqrs, event sourcing, 3 cmadas, etc
    DDD - Domain Driven Design - Como vc aborda o negócio para a criação do sw
      É sobre o negócio, agrupar conhecimento de negócio, reconhecer e seprar subdominios, desenhar modelo de domínio rico. Pode ser udado com qq estilo e pdrão. é uma aobradagem de design, modelagem. Não é tecnologia é padrão de trabalho.
      
 ## - Arquitetura de sistemas avançados
 
    Comunição de serviços via mensagem em comunição assincrona.
    Gerenciamento de erros através de monitoramento 
    Rastreamento de fluxo atravês de logs
 
 
    
   
    
   

   
    
          
      
   
   
    
    
   
  
     
    
 
