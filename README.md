## Arquivos
- Em Projeto Completo - Final, há um arquivo chamado explicação, nele você tem um contéudo para entender sobre React. Nesse arquivo, foi utilizado React para seu desenvolvimento;
- Em Projeto Completo - Final, também há um outro arquivo chamado aplicação onde nele foi feito um site em React para Exemplo de desenvolvimento.

## Tutorial: Como abrir um arquivo React, instalar dependências e rodar a aplicação
[1. Pré-requisitos](#) 
- Node.js: Certifique-se de ter o Node.js instalado na sua máquina. Você pode baixar e instalar o Node.js a partir do site oficial.
- NPM: O Node.js já inclui o NPM (Node Package Manager), que será necessário para instalar as dependências do projeto.

[2. Baixando o projeto](#)
- Baixe o arquivo (Preferencialmente o Projeto Completo - Final);
- Extraia o arquivo .zip;
- Abra o Visual Studio Code;
- Abra a pasta que deseja executar;

[3. Abrir o projeto no terminal](#)
- Abra o terminal ou o Prompt de Comando (no Windows) e navegue até o diretório onde o projeto React está localizado; 
- Se você baixou o projeto e o extraiu para a pasta meu-projeto, por exemplo, navegue até ela com o seguinte comando:
``` js
cd caminho/para/a/pasta-do-projeto
```

[4. Instalar as dependências do projeto](#)
- Agora, instale as dependências do projeto usando o NPM. Execute o seguinte comando no terminal:
``` js
npm install
```
Este comando vai ler o arquivo package.json e instalar todas as bibliotecas e pacotes necessários para rodar o projeto.

[5. Rodar o servidor de desenvolvimento](#)
- Após a instalação das dependências, você pode rodar o servidor de desenvolvimento com o seguinte comando:
``` js
npm run dev
```
O React rodará o servidor de desenvolvimento e fornecerá um link no terminal, algo como:
``` js
Local: http://localhost:3000
```

[6. Abrir o projeto no navegador](#)

Copie o link fornecido pelo terminal (normalmente http://localhost:3000) e cole no seu navegador de internet. A aplicação React agora estará rodando localmente no seu navegador!

- - -
A estrutura de projeto do Next.js organiza o desenvolvimento de aplicações web em uma estrutura modular, visando facilitar
 a construção de rotas, a gestão de componentes, e a utilização de APIs e estilos. Ela segue convenções que ajudam a manter o projeto organizado, escalável e fácil de manter.

 Aqui está um resumo detalhado sobre os principais diretórios e arquivos que compõem um projeto Next.js:
 ## 1. Diretório Raiz 
 No nível raiz, você encontrará os principais arquivos de configuração e pastas que definem o comportamento da aplicação. Entre eles temos:
 - .gitignore: Define quais arquivos ou diretórios o Git deve ignorar. É comum ignorar node_modules, arquivos de log, e outros arquivos temporários;
 - package.json: Gerencia as dependências do projeto e os scripts de execução como npm run dev para iniciar o servidor de desenvolvimento;
 - README.md: Contém informações sobre o projeto, como como configurá-lo, executá-lo e contribuir. É uma boa prática incluir instruções para outros desenvolvedores.
- - - 
## 2. Diretórios Principais
[src/app](#) 
- src: O diretório src é um dos diretórios principais do Next.js.
- app: Introduzido nas versões mais recentes do Next.js, o diretório app é o novo sistema de roteamento. Cada subdiretório dentro de app corresponde a uma rota. Ele permite um roteamento baseado em layout, possibilitando layouts persistentes entre diferentes páginas. No diretório app, os componentes são definidos como Server Components por padrão. Isso permite criar aplicativos que abrangem tanto o servidor quanto o cliente.
  
[global.css](#)
- Este arquivo contém estilos globais que serão aplicados a toda a aplicação. Ao incluir estilos nesse arquivo, você garante que eles afetem todas as páginas e componentes da sua aplicação Next.js.

[layout.js](#)
- Este arquivo define um layout que pode ser aplicado a uma ou mais páginas dentro da aplicação. O layout permite que você mantenha uma estrutura consistente, como cabeçalhos, rodapés e menus, em várias páginas sem repetir código.

- No Next.js, o layout.js é colocado dentro de um diretório em app/. Quando você define um layout, todas as páginas que estão dentro desse diretório herdarão esse layout automaticamente.

[page.js](#)
- Este arquivo define o conteúdo de uma página específica em seu aplicativo Next.js. Ele renderiza a interface do usuário que será exibida quando a rota correspondente for acessada. Normalmente será a página principal, como se fosse o index.html

[page.module.css](#)
- Este arquivo contém estilos que são aplicados exclusivamente a uma página ou a um componente específico. A principal característica dos módulos CSS é que eles são escopados automaticamente, ou seja, as classes CSS definidas dentro desse arquivo não afetarão outras partes da aplicação, evitando conflitos de nomes. Normalmente será o estilo da página principal, no caso o page.js
- - - 
## 3. Diretórios ignorados/instalados 
[.next](#)
- A pasta next é uma estrutura gerada pelo Next.js que contém o código necessário para compilar e executar sua aplicação. É importante notar que você não cria essa pasta manualmente; ela é gerada automaticamente durante o desenvolvimento, construção e execução do seu projeto.
- Essa pasta é essencial para a entrega do seu aplicativo, pois o Next.js a utiliza para gerar as páginas que serão enviadas ao cliente.
- *Como a pasta é gerada automaticamente, você não deve alterar ou manipular os arquivos dentro dela.*

[node modules](#)
- A pasta node_modules é criada quando você instala as dependências do seu projeto usando o gerenciador de pacotes npm (install). Ela contém todos os pacotes e bibliotecas que o seu projeto precisa para funcionar corretamente.
- Todos os pacotes listados no arquivo package.json são instalados nessa pasta. Isso inclui não apenas o Next.js, mas também outras bibliotecas que você pode estar usando, como React
- A pasta geralmente é ignorada no controle de versão (Git) devido ao seu tamanho e à sua natureza gerada automaticamente. Por isso, você geralmente verá um arquivo .gitignore que inclui node_modules/.
- - - 
# Criação de componentes simples (sem estado)
[O que são Componentes em React?](#)

Os componentes são a base do React. Eles permitem que você divida a interface do usuário em partes independentes e reutilizáveis. Um componente pode ser uma função ou uma classe que retorna um elemento React (geralmente JSX). Componentes simples, ou componentes de apresentação, não gerenciam estado e são usados principalmente para renderizar a interface.

No Next.js, os componentes são criados da mesma forma que em um aplicativo React padrão. Vamos criar um componente simples de apresentação como exemplo.

## Passo 1: Criando um Componente Simples.
- Crie o Componente/Arquivo (preferencialmente dentro da pasta src/app) HelloWorld.js
- Agora vamos fazer com que esse componente exiba uma mensagem simples.
  
![Criando](https://github.com/ArthurEdu05/POC5-react-TechMack/blob/main/Imagens%20para%20o%20readme/criando.png)

## Passo 2: Usando um componente da página 
- Agora, vamos usar o componente HelloWorld na nossa página principal.
- Importe o componente:
  
![Importando](https://github.com/ArthurEdu05/POC5-react-TechMack/blob/main/Imagens%20para%20o%20readme/importando.png)

Importamos o componente HelloWorld e o usamos dentro do componente Home. Isso nos permite modularizar nossa aplicação e reutilizar componentes conforme necessário.
- Depois de importar, chame o componente quando quiser usar! Por exemplo aqui está o componente criado sendo executado:
``` js
***

Olá, Mundo!

Bem-vindo à sua aplicação Next.js!

***
```
- Para executar o componente use chamando seu nome:

![Executando](https://github.com/ArthurEdu05/POC5-react-TechMack/blob/main/Imagens%20para%20o%20readme/executando.png)
- - -
## Estilo CSS (global e módulo).
[Estilo globais](#)

Estilos globais são regras CSS que são aplicadas a todo o aplicativo, ou seja, todos os componentes e páginas. Eles definem a aparência geral da aplicação, como cores, fontes, espaçamentos e layout. Você pode utilizar os estilos globais no arquivo globals.css

**Vantagens dos Estilos Globais:** 
- Consistência: Estilos globais garantem uma aparência consistente em todas as páginas da aplicação.

- Facilidade de Uso: São simples de implementar e ideais para definir temas ou estilos universais.

**Vantagens dos Estilos de Módulo:**
- Escopo Garantido: Os estilos são aplicados apenas aos componentes que os importam, evitando conflitos de nome.

- Manutenção Facilitada: Com estilos escopados, é mais fácil entender quais estilos pertencem a quais componentes, melhorando a manutenção do código.

- Reutilização de Estilos: Os módulos CSS permitem que você reutilize estilos em diferentes componentes sem preocupações com sobreposição.

## Tecnologias Utilizadas 
- Next.js – Framework React para desenvolvimento de aplicações web.
- React – Biblioteca JavaScript para criação de interfaces de usuário.
- CSS Modules – Para o escopo local de estilos CSS.
- JavaScript (ES6+) – Sintaxe moderna de JavaScript.
- Editor – Visual Studio Code.
  
## Autores
- Arthur Eduardo - 10437356
- Felipe Melantonio - 10443843
- Guilherme Sampaio Silva - 10443768


  
