<h1>Chapter I: Fundamentos do ReactJS</h1>

<p>Neste módulo foi criado a aplicação <b>01-Github-Expolorer</b> que consome a API do github em uma estrutura base React utilizando:<p>

  <li>Webpack Dev Server: utilizado para automatizar tarefas</li>
  <li>SASS: é um dos principais pré-processadores CSS disponíveis atualmente</li>
  <li>Source Maps</li>
  <li>Fast Referesh: Utilizado para que se possa obter atualizações instantaneas em componentes React</li>
  <li>git-commit-msg-linter: utilizado para padronizar mensagens de commit do git (de acordo com convensões já difundidas pelas comunidade)</li>

<h2>Conceitos</h2>

<h4>React<h4>
  É uma biblioteca de criação de interface, tanto na web, quanto mobile, televisão, realidade virtual.<li>criação de SPA (Single Pages Applications): faz a separação da parte visual (frontend) da regras de negócio (backend). Fazendo a conexão através da API (Application Program Interface).</li>

  <li>Diferente das interfaces SSR (Server Side Render), utilizados pelas linguagens PHP, Ruby, Pyton. Faz 
  com que	o backend renderize o HTML, CSS, JS da aplicação que é servido pelo backend, ou seja, este é responsavel pelas regras de negócio e a parte visual.</li>

<h4>Typescript</h4>
	De acordo com o site do desenvolvedor é um superset, ou seja, ele adiciona um conjunto de funcionalidades a uma linguagem (javascritp), é uma maneira de tipagem.
	Quando é feito uma alteração de codigo, uma chamada em a variáveis ou funções, sem a tipagem do Typescript é dificil identificar o formato dessas informações e é este a problemática que o typescript se propõe a resolver (javascript utiliza tipagem dinamica).

  <li><b>Exemplo:</b></li>
	
	* Sem tipagem
	<i>function showWelcomeMessage(user) {
		return `Welcome ${user.name}, your  e-mail is ${user.email}. 
		Your city is ${user.city} and your state is ${user.state}`;
	}
	
	// Cidade - UF</i>
	
	* Com tipagem
	type User = {
		name: string,
		email: string,
		address: {
			city: string,
			state?: string,
		}
	}
	
	function showWelcomeMessage(user: User) {
		return `Welcome ${user.name}, your  e-mail is ${user.email}. 
		Your city is ${user.address.city} and your state is ${user.address.state}`;
	}

  <h4>Hooks utilizados</h4>
  <li>useState: Hook que controla variávies de estado de um componente funcional no React. Exemplo: <i>const [count, setCount] = useState(0); o qual o primeiro valor (count) representa o estado que será manipulado e pela função setCount</i> </li>
  <li>useEffect: Hook de efeito, sendo este criado para lidar com a deficiencia de side-effects. Com o useEffect é possivel contornar os efeitos colaterais durante a renderização destes componentes. <b>Obs:<i>* cuidado para não deixar sem o ultimo parametro do useEffect(()=> {}, []) (no caso sem os colchetes) isso ocasionará um loop infinito. Existe outra maneira de ocasionar o loop infinto, que é colocar a propria variavel a ser atualizada como o segundo parametro. </i></b> </li>