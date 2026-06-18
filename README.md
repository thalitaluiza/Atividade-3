# Casa della Nonna - Projeto HTML Semântico

Simulação de um site institucional e cardápio de um restaurante italiano tradicional e familiar.

O site foi construido em uma única página.

Segue a explicação de como cada tag foi utilizada:
### 1. Estrutura Principal e Topo
* `<html lang="pt-br">`: Define o idioma principal da página. Isso ajuda os motores de busca (SEO) a indexarem o site na região correta e orienta os leitores de tela a usarem a pronúncia certa em português (Acessibilidade).
* `<header>`: Define o cabeçalho do site. Indica aos robôs de busca onde estão os elementos introdutórios e de identidade da marca, separando do conteúdo principal.
* `<h1>`: É o título principal do site. É o elemento mais importante para o SEO, pois resume o assunto central do site. Deve ser único na página.
* `<nav>`**: Agrupa os links de navegação. Essencial para a acessibilidade, pois permite que usuários com deficiência visual pulem direto para o menu usando leitores de tela.
*  `aria-label="Navegação Principal"`**: Ajuda deficientes visuais a identificarem rapidamente que aquele bloco serve para navegar pelo site.

### 2. Seção de Destaque (Hero)
*  `<section>`: Usada para separar os grandes blocos de conteúdo logicamente relacionados (Boas-vindas, História, Cardápio, Reservas). Isso divide o site em capítulos organizados.
*  `<video>`: Insere o vídeo de fundo no banner principal. Atributos como `autoplay`, `loop` e `muted` foram usados para o vídeo rodar sozinho como fundo decorativo. O `playsinline` impede que celulares quebrem o layout abrindo o vídeo em tela cheia automática.
* `<figure>` e `<figcaption>`: Agrupam uma imagem e sua respectiva legenda. Cria uma associação semântica direta entre a foto e o texto descritivo, facilitando a leitura por robôs e sistemas assistivos.
* `<img>` com `alt`: Insere imagens na página. O atributo `alt` descreve o que está na imagem. Se a imagem falhar, o texto aparece. Além disso, permite que deficientes visuais "escutem" a foto e ajuda no rankeamento do Google Imagens.
* `<article>`: Conteúdo autônomo e independente (o destaque da semana). Indica que este bloco faz sentido por si só e poderia ser compartilhado isoladamente em outros portais ou feeds.
* `<aside>` com `aria-describedby`: Conteúdo de curiosidade. O atributo conecta o bloco ao seu título interno (`id="info-tomate"`), melhorando a navegação estruturada para leitores de tela.

### 3. Conteúdo Institucional e Destaques
* `<main>`: Envolve todo o conteúdo exclusivo da página. Só existe um por site, ajudando leitores de tela a irem direto ao que interessa, ignorando o topo e o rodapé.
* `<time datetime="1952-10-12">`: Usado para marcar a data de fundação de forma que os robôs de busca (SEO) consigam ler e catalogar o tempo exatamente, independente de como ele esteja escrito para o usuário.
* `<i>accogliente</i>`: Usado para dar ênfase visual a termos em outros idiomas (italiano, no nosso caso).
* `<figure>` e `<figcaption>`: O `figure` agrupa elementos ilustrativos (imagens) ao seu contexto, e o `figcaption` adiciona a legenda ligada diretamente à foto. Isso ajuda muito no SEO de imagens do Google.
* `alt="..."` nas imagens: Texto alternativo obrigatório para acessibilidade. Ele descreve a imagem em detalhes para quem não pode enxergar e também ajuda o Google a entender o conteúdo da foto.
* `<article>`: Usado na seção "Destaque da Semana" porque é um conteúdo autônomo. Indica que este bloco faz sentido por si só e poderia ser compartilhado isoladamente em outros portais ou feeds.
* `<abbr title="...">`: Define uma abreviação. Quando o usuário passa o mouse, o significado aparece na tela, melhorando a experiência do usuário.
*  `<strong>` e `<em>`: Usados para dar destaque a palavras importantes. Diferente de tags antigas, estas possuem peso semântico, avisando os leitores de tela para mudarem o tom de voz ao ler essas palavras.
* `<aside>`: Conteúdo lateral ou curiosidade que complementa o assunto principal sem quebrar o fluxo do texto.

### 4. Cardápio
*  `<table>`: Usada estritamente para dados tabulares organizados em colunas (Prato, Ingrediente, Preço). Nunca deve ser usada para criar layouts, apenas para dados.
* `<caption>`: Funciona como o título descritivo da tabela, contextualizando o conteúdo para leitores de tela imediatamente.
* `<thead>`, `<tbody>` e `<tfoot>`: Dividem a tabela em cabeçalho, corpo e rodapé de dados. Isso ajuda na organização do código e na leitura acessível.

### 5. Interação e Formulários
*  `<details>` e `<summary>`: Criam um sistema interativo onde o usuário clica e revela informações (como os horários), sem precisar de códigos complexos.
* `<form>` e `<fieldset>`: O `form` cria a área de envio de dados e o `fieldset` agrupa os campos de forma organizada para navegação via teclado.
* `<legend>`: Dá o título do grupo de campos do formulário, essencial para acessibilidade.
* `<label for="...">`: Conecta o texto explicativo diretamente ao campo de entrada (`<input>`) através do `id`. Se o usuário clicar no texto da etiqueta, o cursor ativa o campo de texto automaticamente.
* `<dialog>`: Cria uma janela de alerta nativa do navegador para mostrar as políticas de cancelamento.

### 6. Contatos e Encerramento
* `<footer>`: Delimita o rodapé da página com informações de encerramento, direitos autorais.
* `<address>`: Tag específica para dados de contato e localização geográfica da empresa, utilizada por mecanismos de busca locais.


