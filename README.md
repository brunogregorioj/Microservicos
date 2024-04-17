# Construindo uma aplicação do zero com microsserviços

Nesta seção, estaremos realizando uma atividade prática para aprender a construir microsserviços. Vamos implementar uma aplicação utilizando a arquitetura baseada em microsserviços, utilizando JavaScript como linguagem principal. A ideia é implementar os diversos recursos necessários um a um, ao invés de utilizar pacotes já prontos para isso. Nas próximas seções, lidaremos também com o seu uso.


## Visão Geral

Nesta seção, vamos discutir quais microsserviços implementar e como abordaremos sua implementação.

### Quais microsserviços implementar?

Uma decisão importante a ser tomada é sobre quais e quantos microsserviços implementar. Para esta aplicação, iremos implementar um microsserviço para cada tipo de objeto que ela manipula. Assim, teremos um microsserviço para os lembretes e outro para as observações. Cada um realizará as seguintes tarefas:

- **Microsserviço de lembretes**:
  1. Criar um lembrete
  2. Listar os lembretes
  
- **Microsserviço de observações**:
  1. Criar uma observação
  2. Listar as observações de um lembrete

É importante observar que, mesmo para funcionalidades aparentemente simples, existem questões relativamente complexas a serem resolvidas. As funcionalidades do microsserviço de observações, por exemplo, dependem de dados dos lembretes, o que nos leva a decidir qual forma de comunicação será empregada entre os microsserviços.

### Implementando o microsserviço de lembretes

Os microsserviços serão implementados utilizando o [2]. Caso não tenha instalado, visite o Capítulo 5 para mais informações.

## Configurando o Ambiente de Desenvolvimento

Comece criando um diretório para abrigar os arquivos dos projetos.

## O Microsserviço de Lembretes

Cada microsserviço será implementado como um projeto independente. Siga os passos abaixo para configurar o microsserviço de lembretes:

1. Crie uma pasta chamada `lembretes` em seu workspace.
2. Utilize o comando `npm init -y` para criar um projeto. A opção `-y` indica que deseja-se utilizar valores padrão para cada item que caracteriza o projeto, como nome, versão etc.

## Pacotes

Os pacotes que utilizaremos, a princípio, são:

- **[Express](link_do_pacote)**: Um framework web para o Node.js que adiciona níveis de abstração para, entre outras coisas, a manipulação de requisições HTTP.
- **cors**: CORS significa Cross-Origin Resource Sharing. Trata-se de um mecanismo utilizado para especificar como cliente e servidor podem compartilhar recursos, em particular para o caso em que tiverem domínios diferentes. O pacote `cors` disponibiliza uma API que simplifica esse tipo de especificação.
- **axios**: Um pacote que simplifica a realização de requisições HTTP assíncronas usando Ajax.
- **nodemon**: Seu nome vem de Node Monitor. É natural a necessidade de reinicializar o servidor em tempo de desenvolvimento. Em geral, isso é necessário para que novas atualizações realizadas possam ser testadas. O `nodemon` é um pacote que monitora a execução de um servidor e que o reinicializa automaticamente quando detecta que arquivos de extensões especificadas são alterados.
