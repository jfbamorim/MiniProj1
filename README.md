# MiniProj1

CV pessoal em formato de Single Page Application (SPA), desenvolvido no âmbito da Tarefa 2.2 da unidade curricular de Programação Web Avançada (Mestrado em Engenharia Informática e Tecnologias Web, UTAD/UAb).

## Descrição

Aplicação de página única, contida num só ficheiro (`index.html`), construída com Vue 3 carregado por CDN. Tem três secções, **Quem Sou Eu?**, **O que faço?** e **Hobbies**, e um rodapé com ligações para o GitHub e o LinkedIn.

## Como executar

Não é preciso instalar nada nem fazer *build*. Basta abrir o `index.html` no browser (duplo clique ou, por exemplo, com a extensão Live Server do VS Code).

É necessária ligação à internet, porque o Vue é carregado a partir do unpkg.

## Funcionalidades

- Navegação entre secções com links internos (`#/quem-sou-eu`, `#/o-que-faco`, `#/hobbies`), sem recarregar a página. O botão Voltar do browser funciona e cada secção tem um endereço partilhável.
- Hobbies apresentados em cartões; ao clicar abre-se uma janela (modal) com a descrição, que se fecha no botão ou clicando fora dela.
- Menu em hambúrguer em ecrãs estreitos.
- Separador ativo assinalado visualmente e para tecnologias de apoio (`aria-current`, `aria-expanded`, `aria-label`).

## Tecnologias

HTML, CSS e JavaScript, com Vue 3.5.13 (CDN).

## Decisões de implementação

- **Navegação:** o estado da secção ativa vem do `location.hash`, copiado para um `ref` do Vue através do evento `hashchange`, com a função `lerHash()` a validar o valor e a assegurar uma secção por defeito. Evita o servidor e funciona abrindo o ficheiro diretamente.
- **Modal:** um único modal reutilizado, alimentado pelo hobby selecionado (`hobbyAberto`).
- **Ficheiro único:** HTML, CSS e JavaScript no mesmo `index.html`, como pedido no enunciado.

## Utilização de IA

Decisões de estilo, nomeadamente na parte CSS, foram desenvolvidos com apoio de uma ferramenta de AI.
O estilo visual partiu da inspiração no site [justinchi.me](https://justinchi.me) (fundo claro, uma única cor de destaque, menu só com texto). O CSS inicial, mais elaborado, foi gerado com o apoio da ferramenta com essa referência. Considerei-o mais complexo do que o projeto precisava e simplifiquei-o, para perceber e conseguir justificar cada regra.

## Autor

Jorge Amorim
[GitHub](https://github.com/jfbamorim) · [LinkedIn](https://pt.linkedin.com/in/jorge-amorim-316969108)