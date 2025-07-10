Course: https://balta.io/player/assistir/5c6b2cc2-e717-9a27-eb62-bae000000000/dc922dc3-1903-45f0-aa25-000071810105

Repo Balta.io: https://github.com/keodevspace/todo_angular
Repo Prf. Ivirson: https://github.com/keodevspace/angular-i-santander?tab=readme-ov-file

- @ na frente: decorator

- Módulo e Componente: dois intens principais do angular

- Component:
	- css - estilo
	- html - visão
	- spec - testes
	- ts - comportamento
````bash
@Component({
		selector: 'app-root', // pode ser qq nome
		templateUrl: './app.component.html',
		styleUrls: ['./app.component.css'] // array
		})
````
Toda vez que eu usar o decorator no component eu estou gerando metadados, ou seja, eu estou criando uma **TAG HTML** - < app-root >

-  export: cria uma classe pública

- bootstrap: inicialiazação

- Angular tem servidor integrado, Browser Link, que, toda vez que eu altero a aplicação, eu não preciso parar e rodar ela novamente, ela altera e atualiza o browser automaticamente

- ng serve       --> rodar a aplicação
- ng serve -o    --> roda e abre o browser

- 'public todos: any [ ] = [ ];'   // vazio
- 'public todos: any [ ];    //undefined
	- : eu estou tipando no ts
	- abre e fecha colchete = array

- ctor + tab    --> cria um construtor

- ts usa o THIS
	- function teste () { this.      }
	- this refere-se à teste()
	- THIS REFERE-SE AO ESCOPO DA CLASSE, entao tenho acesso a todos os métodos da classe.

- Chaves Duplas: para exibir o valor de variáveis
	- < h1> {{ title }}< /h1>

- ol: num
- ul: point

- ngfor - looping

- MODELS
	- crio um objeto
	- qto mais eu tipar melhor
	- crio um tipo, ex, Todo [ ]
	```bash
	export class AppComponent {
		public todos: Todo[] = [];
    ```
	- usar um método construtor dentro do model
		- na assinatura (  ) vai ter que passar o que o Todo tem - id, title e done
		- this.todos.push(new Todo(1, 'Task', false));
	```bash
	export class Todo {
    constructor(
        public id: Number,
        public title: String,
        public done: Boolean,
    )}
    ```


- ngIf
	-


