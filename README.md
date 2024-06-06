# <h1 align=center>Lista de Afazeres (To do List)</h1>
 
<p><img align="" src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white">
<img align="" src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white">
<img align="" src="https://img.shields.io/badge/VSCode-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white">
<img align="" src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white">
<img align="" src="https://img.shields.io/badge/GIT-E44C30?style=for-the-badge&logo=git&logoColor=white ">
<img src="https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E">
<img src="https://img.shields.io/badge/markdown-%23000000.svg?style=for-the-badge&logo=markdown&logoColor=white">
<img src="https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white">
<img src="https://img.shields.io/badge/OneDrive-0078D4.svg?style=for-the-badge&logo=microsoftonedrive&logoColor=white">
<img src="https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white">
</p>
 
>Este projeto é uma aplicação simples de lista de tarefas ("To Do List") construída utilizando HTML, CSS e JavaScript.
 
*Disciplina:* Desensivolvimento Web
 
 
 
*Professor*: [Leonardo Santiago Sidon da Rocha](https://github.com/LeonardoRochaMarista/)

 
### A seguir, está uma explicação detalhada de cada parte do código:
<h3 align=center> HTML:</h3>
 
>O HTML define a estrutura da página, incluindo elementos como formulários, botões e listas de tarefas que compõem a aplicação.
 
### Estrutura HTML:
`todo-conteiner:` Contêiner principal da aplicação.
 
`` header:`` Cabeçalho contendo o título da aplicação.
 
`todo-form:` Formulário para adicionar novas tarefas.
 
`edit-form:` Formulário para editar tarefas existentes.
 
`toolbar:` Barra de ferramentas para pesquisa e filtro de tarefas.
 
`todo-list:` Lista de tarefas com exemplos de tarefas (feitas e não feitas).
#
<h3 align=center> CSS:</h3>
 
> O CSS é utilizado para estilizar a aplicação, definindo a aparência dos elementos HTML.
 
 
### Estrutura CSS:
`Estilos globais:` Reseta margens e define a fonte.
 
`body:` Define a imagem de fundo.
 
`button:` Estiliza os botões com transições e mudanças de cor ao passar o mouse.
 
`input, select:` Estiliza os campos de texto e select.
 
`.hide:` Classe para esconder elementos.
 
`.todo-conteiner:` Centraliza e estiliza o contêiner principal.
 
`.todo:` Estiliza as tarefas na lista, diferenciando as concluídas com .done.
#
<h3 align=center> JavaScript:</h3>
 
> O JavaScript é responsável pela interatividade da aplicação, permitindo adicionar, editar e remover tarefas.
### Estrutura JavaScript:
 
<h5 align=center><i>Seleção de Elementos</i></h5>
<p>Primeiro, selecionamos os elementos HTML que precisaremos manipular:</p>
 
`todoForm`: Seleciona o formulário onde adicionamos novas tarefas.
 
`todoInput`: Seleciona o campo de texto onde inserimos o nome da tarefa.
 
`todoList`: Seleciona o contêiner onde as tarefas serão exibidas.
 
`editForm`: Seleciona o formulário de edição de tarefas.
 
`editInput`: Seleciona o campo de texto onde editamos o nome da tarefa.
 
`cancelEditBtn`: Seleciona o botão de cancelar a edição.
 
`oldInputValue`: Variável para armazenar o valor antigo da tarefa antes da edição.
 
#
 
<h5 align=center><i>Funções</i></h5>
 
**Função `saveTodo`:** Essa função cria e adiciona uma nova tarefa à lista de tarefas.
1. Criação do contêiner da tarefa (div):
* todo: Cria uma div para a tarefa e adiciona a classe `todo`.
 
2. Criação do título da tarefa (h3):
* todoTitle: Cria um elemento `h3` para o título da tarefa e define seu conteúdo com o texto fornecido como argumento.
 
3. Criação dos botões de ação:
* doneBtn: Cria um botão para sinalizar a conclusão da tarefa.
* editBtn: Cria um botão para editar a tarefa.
* deleteBtn: Cria um botão para remover a tarefa.
 
4. Adição da tarefa à lista:
* Adiciona a div da tarefa (`todo`) à lista de tarefas (`todoList`).
 
5. Limpeza do campo de entrada:
* Limpa o campo de entrada (`todoInput`) e retorna o foco para ele.
 

 
#
 
**Função `toggleForms`:** Essa função alternará a visibilidade entre os formulários de adição e edição de tarefas.
 
* Alternadamente, a classe "hide" é alternada nos formulários de adição (`todoForm`), edição (`editForm`) e na lista de tarefas (`todoList`), exibindo um e ocultando os outros conforme necessário.
 

 
#
 
**Função `updateTodo`:** Essa função atualiza o texto de uma tarefa existente.
 
* Percorre todas as tarefas (todos).
* Se o texto do título da tarefa (todoTitle.innerText) corresponder ao valor antigo da tarefa (oldInputValue), atualiza o texto da tarefa para o novo valor (text).
 
#
 
<h5 align=center>Eventos</h5>
 
*Evento de envio do formulário (submit):* Esse evento lida com a adição de novas tarefas.
 
* Impede o comportamento padrão do formulário para evitar o recarregamento da página.
* Captura o valor presente no campo de entrada (`inputValue`).
* Se o campo não estiver vazio, invoca a função `saveTodo` para adicionar a nova tarefa..
 
 
#
 
*Evento de clique (click):* Esse evento lida com as ações dos botões de concluir, editar e remover tarefas.
 
* Identifica qual elemento foi clicado (targetEl).
* Identifica o div pai mais próximo (parentEl).
* Recupera o título da tarefa se o elemento pai contiver um `h3`.
 
1. Botão de concluir tarefa:
* Alternadamente, adiciona ou remove a classe "done" na div da tarefa, marcando-a como concluída ou não.
 
2. Botão de remover tarefa:
* Remove a div da tarefa.
3. Botão de editar tarefa:
* Alterna os formulários de adição e edição.
* Preenche o campo de edição com o título da tarefa atual.
* Armazena o valor antigo da tarefa para futura comparação.
 

 
#
 
*Evento de cancelar edição:* Esse evento lida com o cancelamento da edição de uma tarefa.
 
* Previne o comportamento padrão do botão.
* Alterna os formulários de adição e edição de volta ao estado inicial.
 

 
#
 
*Evento de envio do formulário de edição (submit):* Esse evento lida com a atualização do texto da tarefa.
 
* Previne o comportamento padrão do formulário.
* Obtém o valor do campo de edição (editInputValue).
* Se o valor não estiver vazio, chama a função updateTodo para atualizar o texto da tarefa.
* Alterna os formulários de volta ao estado inicial.
 

 
Com essas explicações detalhadas, você agora tem um entendimento completo de como cada parte do JavaScript contribui para a funcionalidade da aplicação de lista de tarefas.
 
#### Quer fazer por um toturial? 👇
[Projeto de JavaScript para iniciantes - To Do List com JavaScript puro](https://www.youtube.com/watch?v=HSssE1PRQcA)
 
*Autor:*
[Geovana Aparecida de Lima]
 
*Meu Linkedin*: [Feed](https://www.linkedin.com/in/milla-karoll-776314300/?trk=opento_sprofile_details)