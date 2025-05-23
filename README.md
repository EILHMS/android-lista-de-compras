Nome: Lucas Henrique de Melo Silva
Turma: 3 sir
Rm: 550175
-------------------------------------------
# Lista de Compras – App Android com Kotlin

Este projeto é um aplicativo simples de lista de compras desenvolvido com Kotlin para Android. Ele utiliza arquitetura baseada em componentes do Jetpack, como ViewModel, LiveData e Room Database, e permite que o usuário adicione e remova itens de uma lista de compras.

## Estrutura do Projeto

### Pasta: data/
Responsável pela camada de acesso ao banco de dados com Room.
- ItemDao.kt: Interface com os métodos para manipulação de dados no banco, como inserir, deletar e listar itens.
- ItemDatabase.kt: Classe abstrata que configura o banco de dados Room e fornece acesso ao DAO.

### Pasta: model/
Contém o modelo de dados da aplicação.
- ItemModel.kt: Classe que representa a estrutura dos itens da lista. Possui campos como id e nome, e é mapeada como uma entidade do Room.

### Pasta: viewmodel/
Gerencia a lógica de negócios e interação entre a interface e os dados.
- ItemsViewModel.kt: Armazena e manipula a lista de itens, expõe os dados via LiveData e oferece métodos para adicionar e remover itens.
- ItemsAdapter.kt: Adapta os dados para serem exibidos em uma RecyclerView. Controla a exibição e ações sobre os itens.
- ItemsViewModelFactory.kt: Responsável por instanciar o ViewModel passando o DAO como parâmetro.

### Pasta: ui/theme/
Define os estilos e o visual do aplicativo.
- Color.kt: Contém definições de cores utilizadas no app.
- Theme.kt: Configura o tema principal da aplicação, como cores e estilo.
- Type.kt: Define a tipografia do aplicativo, como tamanhos e estilos de fonte.

### Pasta: res/
Contém recursos visuais e arquivos de layout da interface.
- layout/: Arquivos XML que definem a estrutura visual das telas do app.
- values/: Arquivos com recursos reutilizáveis como:
  - colors.xml: Definição de cores do app.
  - strings.xml: Textos e mensagens usadas na interface.
  - themes.xml: Estilos e temas aplicados globalmente.

## Funcionalidades do Aplicativo

- O usuário pode digitar o nome de um item e adicioná-lo à lista de compras.
- A lista é exibida com um componente RecyclerView que mostra todos os itens adicionados.
- Cada item exibido possui um botão que permite removê-lo da lista.
- Os dados são armazenados localmente usando o Room Database.
- A lista se atualiza automaticamente quando há adição ou remoção de itens, graças ao uso de LiveData.
- A arquitetura do aplicativo separa claramente a interface, a lógica de negócio e o armazenamento de dados.

## Tecnologias Utilizadas

- Kotlin
- Android SDK
- Android Jetpack (ViewModel, LiveData)
- Room Database
- RecyclerView
