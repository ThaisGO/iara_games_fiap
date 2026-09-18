# Iara Games - Plataforma de Jogos Brasileiros
A Iara Games é um projeto desenvolvido para um trabalho da [Fiap.com](http://Fiap.com) que consiste em uma plataforma digital voltada ao universo dos games.

Para quem quer **jogar algo novo mas não sabe o quê**, a Iara Games é uma plataforma de descoberta que organiza jogos de forma clara e acessível, com uma identidade brasileira própria — diferente das lojas globais, que otimizam para transação, e das agregadoras, que otimizam para volume.

Conceito visual: *"Um universo gamer inspirado na identidade brasileira."* Água, natureza e tecnologia — a figura mitológica da Iara traduzida em estética contemporânea, não em folclore literal.

## Contexto e Problema
O mercado brasileiro de games consome majoritariamente através de plataformas internacionais de distribuição digital. Cada uma tem uma proposta de valor distinta — catálogo e comunidade (Steam), preço e localização (Nuuvem), curadoria e apresentação visual (Epic) — mas nenhuma foi desenhada primariamente para a *descoberta* como experiência central.

**Como criar uma plataforma de games visualmente atrativa, intuitiva e acessível, que facilite a descoberta e o acesso aos conteúdos e jogos disponíveis?**

**Quando quero jogar algo novo mas não sei o quê, quero navegar por um catálogo organizado de forma clara e visualmente convidativa, para que eu encontre um jogo que combine comigo sem gastar 40 minutos garimpando.**

## Proposta

A proposta da Iara Games é inverter essa prioridade — organizar a experiência em torno de *encontrar algo interessante*, não de *comprar algo específico* — e fazer isso com uma identidade visual ancorada na cultura brasileira, em vez da estética escura e futurista genérica que praticamente todas as concorrentes usam.

## Público Alvo e Benchmark

### Público alvo

#### Público primário
Pessoas interessadas em jogos digitais que usam plataformas online para descobrir novos games, conhecer lançamentos, pesquisar títulos e acompanhar conteúdos do universo gamer.

#### Público secundário
Desenvolvedores independentes, estúdios, criadores de conteúdo, comunidades gamer e pessoas iniciando no mercado de jogos digitais.

### Benchmark

#### Comparativo
| **Critério** | **Steam** | **Nuuvem** | **Epic Games Store** |
| --- | --- | --- | --- |
| Força principal | Catálogo e comunidade | Localização para o Brasil | Apresentação visual |
| Organização | Categorias + tags + recomendação | Ofertas e coleções | Banners e curadoria |
| Densidade de informação | Muito alta | Média | Baixa |
| Descoberta para novatos | Difícil | Média | Fácil, porém rasa |
| Contexto brasileiro | Fraco | Forte (PT-BR, R$, promoções) | Médio |
| Identidade visual | Funcional, pouco marcante | Comercial | Forte, mas genérica no gênero |

#### **Aprendizados**

- **Steam:** a organização do conteúdo é o que impede que um catálogo grande vire uma experiência confusa. → *Adotar hierarquia rígida; evitar densidade.*
- **Nuuvem:** comunicação adaptada ao público brasileiro aproxima e dá relevância. → *Adotar linguagem e referências locais.*
- **Epic:** A apresentação visual dirige a atenção sem comprometer a clareza. → *Adotar hero + destaques; evitar banner promocional dominando a tela.*

## Identidade Visual
![Imagem da home do site Iara Games](/public/assets/home.png)

## Paleta de Cores e Tipografia
### Cores
- #FDF9E9
- #F0B933
- #062D15
- #24B956

### Tipografia
- Big Shoulders
- Raleway


## Decisões de UX

### Header com navegação principal
- *Descrição:* cabeçalho fixo no topo com logo e cinco links: Início, Jogos, Categorias, Comunidade, Sobre.
- *História:* Como visitante, quero ver as seções disponíveis logo ao entrar, para entender o que a plataforma oferece.
- Marcado com <header> contendo <nav> e lista <ul>
- Todos os links alcançáveis por Tab na ordem visual

### Hero section

- *Descrição:* área de destaque com chamada principal, descrição de apoio e um CTA primário.
- *História:* Como visitante novo, quero entender em segundos o que é a plataforma, para decidir se continuo.
- Contém exatamente um ``<h1>`` na página inteira
- Descrição com no máximo 2 linhas em desktop
- Um único CTA primário, com verbo de ação claro (evitar "Saiba mais")
- Legível sobre a imagem de fundo com contraste ≥ 4,5:1 (usar overlay se necessário)

### Seção "Jogos em destaque" com cards

- *Descrição:* grade com 4 cards de jogo.
- *História:* Como explorador, quero comparar rapidamente alguns jogos, para escolher um sem abrir várias páginas.
- 4 cards, cada um com: imagem de capa, nome, gênero/categoria, informação complementar (ex.: preço ou nota)
- Toda imagem com alt descritivo (ex.: "Capa do jogo Correnteza")
- Nome do jogo em <h3> (sob um <h2> de seção)
- Cards com altura consistente independentemente do tamanho do título
- Card inteiro claramente clicável
- Grade responsiva: 4 col. (≥1024px) → 2 col. (≥640px) → 1 col. (<640px)

### Seção de categorias

- *Descrição:* cinco categorias — RPG, Ação, Aventura, Estratégia, Indie.
- *História:* Como visitante sem título em mente, quero navegar por gênero, para reduzir o catálogo a algo administrável.
- 5 categorias visíveis sem scroll horizontal em desktop
- Cada item é link com área clicável ≥ 44×44px
- Identificação não depende só de ícone — sempre com rótulo textual

### Seção "Sobre a Iara Games"
- Texto de 2 a 4 frases explicando proposta e diferencial
- Linha de medida entre 45 e 75 caracteres
- Marcado com <section> e <h2>

### Footer
- Marcado com <footer>
- Contém nome do projeto, links secundários e crédito acadêmico
- Contraste de texto ≥ 4,5:1

### Design e experiência
**"O usuário deve entender onde está, o que pode fazer e para onde pode ir."**

| **Princípio** | **Aplicação concreta na Home** |
| --- | --- |
| **Clareza** | CTA com verbo de ação; máximo 5 itens de menu; texto de apoio curto |
| **Consistência** | Um único componente de card, botão e link em toda a página |
| **Hierarquia** | Hero > Destaques > Categorias > Sobre; escala tipográfica de razão fixa |
| **Feedback visual** | :hover, :focus-visible e :active definidos em todo elemento interativo |
| **Previsibilidade** | Rótulos descrevem o destino; nada muda de posição ao passar o mouse |

## Acessibilidade
| **Critério** | **Requisito** |
| --- | --- |
| Contraste de texto (1.4.3) | ≥ 4,5:1 texto normal; ≥ 3:1 texto grande (≥24px ou ≥19px bold) |
| Contraste não textual (1.4.11) | ≥ 3:1 para bordas de componentes, ícones e anel de foco |
| Foco visível (2.4.7) | :focus-visible com anel de 2px e offset de 2px |
| Textos alternativos (1.1.1) | alt descritivo em imagens de conteúdo; alt="" em decorativas |
| Cabeçalhos e regiões (1.3.1, 2.4.6) | Hierarquia correta, landmarks semânticos |
| Redimensionamento (1.4.4) | Legível e funcional com zoom 200% |
| Uso da cor (1.4.1) | Nenhuma informação transmitida só por cor |
| Alvo de toque (2.5.5, AAA — adotado como meta) | ≥ 44×44px |

## Tecnologias utilizadas
- **HTML** → Estrutura moderna com tags semânticas.
- **Tailwind CSS** → Estilização rápida, responsiva e consistente.
- **Iconify** → Icones próprios que ajudam a reforçar a identidade visual.
- **Google Fonts** → Tipografia personalizada para reforçar identidade visual.

## Deploy
Para ver o site no ar use o link → [https://iara-games-fiap.vercel.app/](https://iara-games-fiap.vercel.app/)

## Autores
Esse projeto foi possível graças a uma equipe foda:

- Ananda - Time de Produto
- Vidal - Time de Ilustração
- Pamella - Time de Marketing
- Vinicius - Time de UI Design
- Thais - Time de desenvolvimento

## Usando o projeto
Primeiramente rode o projeto com o comando abaixo para criar os arquivos necessários:

```
npm run dev
```


2. Depois utilize o live server.
