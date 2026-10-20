# Cantina del Nonno

Site de um restaurante italiano **fictício** em Pinheiros, São Paulo, criado como projeto de estudo. A Cantina del Nonno serve "cucina toscana, cozinhada como em casa" e tem uma história inventada: o nonno Giuseppe veio do Chianti e abriu a cantina em 1987.

> Nomes, endereço, telefones, pratos e preços são ilustrativos. O formulário de reserva não envia dados para lugar nenhum.

## O que o site tem

- **Início:** tela cheia com fundo escuro, nome da cantina e botão "Ver cardápio".
- **Sobre:** a história do nonno Giuseppe.
- **Cardápio:** 12 pratos carregados do arquivo `cardapio.json`, com filtros por categoria (Antipasti, Pasta, Secondi, Dolci) e selo de prato vegetariano.
- **Reserva:** formulário com máscara de telefone, validação em português e uma janela de confirmação com o resumo da reserva (só no navegador, sem servidor).
- **Localização:** mapa interativo (OpenStreetMap, com o Google Maps como reserva), endereço com botão de copiar, telefone, WhatsApp, horário e links para Google Maps e Waze.
- **Extras:** animações ao rolar a página, botão flutuante de WhatsApp, tema escuro automático e preparação para buscadores e assistentes de IA (meta tags, Open Graph, Schema.org, `robots.txt`, `llms.txt` e `sitemap.xml`).

## Como ficou

1. Uma tela inicial escura e elegante, com "Cantina del Nonno" em letras serifadas creme e um botão terracota que pulsa suavemente.
2. Seções em tons de creme, terracota e verde-oliva que surgem ao rolar: história, cardápio em cards com foto, formulário de reserva e mapa de Pinheiros.
3. Um botão verde do WhatsApp acompanha a rolagem no canto da tela, e o site inteiro escurece em tons de café quando o computador está no modo escuro.

## Como rodar no computador

O cardápio é lido do arquivo `cardapio.json`. Por segurança, os navegadores bloqueiam essa leitura quando o `index.html` é aberto com dois cliques, então é preciso usar um servidor local:

1. Abra o Terminal na pasta do projeto.
2. Rode:
   ```bash
   python3 -m http.server 8000
   ```
3. Acesse <http://localhost:8000> no navegador.

Abrindo o `index.html` direto, todo o resto do site funciona, mas o cardápio mostra um aviso no lugar dos pratos.

## Arquivos

| Arquivo | Função |
|---|---|
| `index.html` | O site completo: estrutura, estilos, textos e JavaScript |
| `cardapio.json` | Os pratos do cardápio |
| `robots.txt` | Permissões para robôs de busca e de IA |
| `llms.txt` | Resumo do restaurante para assistentes de IA |
| `sitemap.xml` | Lista de páginas para buscadores |

## Tecnologias

- HTML
- [Tailwind CSS](https://tailwindcss.com) via CDN
- JavaScript puro (sem bibliotecas)
- JSON
- Google Fonts (Playfair Display e Inter)

## Licença

Distribuído sob a licença MIT. Veja o arquivo [LICENSE](LICENSE).
