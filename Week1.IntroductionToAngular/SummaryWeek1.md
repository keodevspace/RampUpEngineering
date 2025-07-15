### Configuração do Ambiente (Node.js, Angular CLI)

* **Node.js**: Angular é construído sobre Node.js. Você precisa ter o Node.js instalado (e consequentemente o npm, que vem com ele) para executar o Angular CLI e as ferramentas de build.
* **Angular CLI (Command Line Interface)**: Esta é a ferramenta essencial para desenvolver em Angular. Ela permite criar novos projetos, gerar componentes, serviços, módulos, e executar comandos para build e teste do seu projeto. Você o instala globalmente via npm: `npm install -g @angular/cli`.

### Criando um Novo Projeto Angular

* Use o Angular CLI para criar um novo projeto. O comando básico é `ng new nome-do-projeto`. Isso configura uma estrutura de projeto completa com todas as configurações e dependências necessárias.

### Estrutura Básica de um Projeto Angular

* **Módulos (Modules - `NgModule`)**: São contêineres que agrupam componentes, serviços, diretivas e pipes relacionados. Todo aplicativo Angular tem pelo menos um módulo raiz (`AppModule`). Eles ajudam a organizar a aplicação e gerenciar dependências.
* **Componentes (Components)**: São os blocos de construção fundamentais da interface do usuário. Cada componente consiste em:
    * Um **Template (HTML)**: Define a estrutura da view do componente.
    * Um **Estilo (CSS/Sass/Less)**: Define a aparência do componente.
    * Uma **Classe TypeScript**: Contém a lógica de negócios e os dados para o template.
* **Templates**: São arquivos HTML associados a componentes. Eles usam a sintaxe de template do Angular (interpolação `{{}}`, binding de propriedades `[]`, binding de eventos `()`, diretivas estruturais `*ngIf`, `*ngFor`) para exibir dados e responder a interações do usuário.

### Criando e Usando Componentes

* **Criação**: Use o Angular CLI para gerar um novo componente: `ng generate component nome-do-componente` (ou `ng g c nome-do-componente`).
* **Seletores (Selectors)**: Cada componente tem um seletor (definido no `@Component` decorator), que é como ele é referenciado no HTML de outros componentes (ex: `<app-my-component></app-my-component>`).
* **Templates e Estilos**: O CLI gera automaticamente os arquivos `.html` e `.css` (ou outro pre-processador de CSS) para o seu componente. Você escreve o HTML no template e o CSS nos arquivos de estilo.

### Ciclo de Vida do Componente (ngOnInit, ngOnDestroy, etc.)

* Componentes Angular passam por um ciclo de vida desde sua criação até sua destruição. O Angular fornece "hooks" (métodos) que você pode implementar em sua classe de componente para executar código em pontos específicos do ciclo de vida.
* **`ngOnInit()`**: É um dos hooks mais importantes. Ele é chamado uma vez que o Angular inicializa as propriedades de data-bound do componente. É um bom lugar para realizar inicializações de dados, chamadas a serviços, etc.
* **`ngOnDestroy()`**: É chamado pouco antes de o Angular destruir o componente. É o local ideal para limpar recursos, como cancelar assinaturas (subscriptions) ou remover event listeners, para evitar vazamentos de memória.
* Outros hooks incluem `ngOnChanges`, `ngDoCheck`, `ngAfterContentInit`, `ngAfterContentChecked`, `ngAfterViewInit`, `ngAfterViewChecked`.

---

### Outros Hooks do Ciclo de Vida do Componente

* **`ngOnChanges()`**:
    * **Quando é chamado:** Sempre que uma ou mais propriedades de entrada (Input properties) do componente mudam. Ele é o primeiro hook a ser executado quando o componente é instanciado e também é executado antes do `ngOnInit` se houver inputs.
    * **Para que serve:** Ideal para reagir a mudanças nos dados que o componente recebe de seu pai. Recebe um objeto `SimpleChanges` que contém os valores atuais e anteriores das propriedades que mudaram.

* **`ngDoCheck()`**:
    * **Quando é chamado:** Imediatamente após o `ngOnChanges` na primeira verificação do ciclo de detecção de mudanças e, subsequentemente, a cada ciclo de detecção de mudanças (mesmo que nenhuma propriedade de entrada tenha mudado).
    * **Para que serve:** Usado para implementar sua própria lógica de detecção de mudanças ou para estender a detecção de mudanças padrão do Angular. É útil em cenários onde você precisa monitorar mudanças que o Angular não detectaria automaticamente (por exemplo, mudanças em objetos ou arrays aninhados). No entanto, deve ser usado com cautela, pois pode impactar o desempenho se não for otimizado.

* **`ngAfterContentInit()`**:
    * **Quando é chamado:** Uma vez após o Angular projetar conteúdo externo (conteúdo vindo de um componente pai via `<ng-content>`) na view do componente.
    * **Para que serve:** É o lugar para interagir com o conteúdo que foi projetado no seu componente. Por exemplo, se você tem um componente que exibe um `<ng-content>` e precisa manipular elementos HTML dentro desse conteúdo, este é o hook para isso.

* **`ngAfterContentChecked()`**:
    * **Quando é chamado:** Após o `ngAfterContentInit` e a cada verificação subsequente do conteúdo projetado.
    * **Para que serve:** Permite que você execute código após o Angular verificar as projeções de conteúdo. É útil se você precisar fazer alguma verificação ou modificação no conteúdo projetado após cada ciclo de detecção de mudanças.

* **`ngAfterViewInit()`**:
    * **Quando é chamado:** Uma vez após o Angular inicializar as visualizações do componente e as visualizações dos componentes filhos.
    * **Para que serve:** O lugar perfeito para acessar elementos DOM que são parte do próprio template do componente, ou para interagir com componentes filhos através de `@ViewChild` ou `@ViewChildren`. É importante notar que as visualizações só estão totalmente disponíveis neste ponto.

* **`ngAfterViewChecked()`: **
    * **Quando é chamado:** Após o `ngAfterViewInit` e a cada verificação subsequente das visualizações do componente e dos seus filhos.
    * **Para que serve:** Similar ao `ngAfterContentChecked`, mas para a própria view do componente e as views de seus filhos. Permite que você execute código após o Angular ter verificado todas as visualizações, sendo útil para realizar operações que dependem da renderização completa da view.
