# Site JsTelas

Site institucional em um único arquivo (`index.html`), responsivo, com pedido de orçamento direto pelo WhatsApp.

## Arquivos

- `index.html`: o site completo (HTML, CSS, JavaScript, fotos e logo no mesmo arquivo).
- `README.md`: este guia.

## Como publicar

1. Escolha uma hospedagem de site estático (Netlify, Cloudflare Pages, GitHub Pages, Vercel ou uma hospedagem comum com FTP).
2. Envie o `index.html` para a raiz do site.
3. Aponte o domínio da empresa para a hospedagem.

Para testar antes, basta abrir o `index.html` no navegador.

## Como editar os dados

Abra o `index.html` em um editor de texto e procure por `const CFG`. Tudo o que muda com frequência fica ali:

| Campo | O que é |
|---|---|
| `nome` | Nome da empresa (aparece no topo, no título e nas mensagens) |
| `whatsapp` | Número do WhatsApp só com dígitos: país + DDD + número (ex.: `5511997023746`) |
| `whatsView` | Número como aparece na tela |
| `tel` | Telefone para ligação |
| `end` | Endereço (também usado no botão "Ver no Google Maps") |
| `horario` | Horário de atendimento |
| `cnpj` | CNPJ exibido no rodapé |
| `fotos` | Fotos do site (veja abaixo) |

## Como trocar as fotos

Dentro de `CFG`, o campo `fotos` tem estes espaços:

- `hero`: foto do banner principal
- `s1` a `s5`: fotos dos cards de serviços (portas, telas para gatos, grades, corrimãos, box em acrílico)
- `g1` a `g6`: fotos da galeria

As fotos atuais estão embutidas no arquivo. Para trocar uma, substitua o valor pelo caminho de uma imagem enviada junto com o site, por exemplo `"imagens/grade.jpg"`. Prefira fotos em JPG, com até 1000 px de largura, para o site carregar rápido.

## Textos para conferir antes de divulgar

- **CNPJ:** ainda está como exemplo (`00.000.000/0001-00`). Preencha em `cnpj` ou apague a linha do rodapé.
- **Promessas do site:** frases como instalação com garantia, visita e medição no local, orçamento sem compromisso e suporte depois da entrega foram escritas como sugestão. Remova ou ajuste o que a empresa não oferece.
- **Fotos de clientes:** confirme que os clientes autorizaram o uso das imagens.

## Como funciona o orçamento

O formulário pede nome, telefone, serviço e descrição. Ao enviar, abre o WhatsApp da empresa com a mensagem pronta, e o cliente só precisa tocar em enviar. Nenhum dado fica guardado no site.

## Observações

- As fontes (Barlow) vêm do Google Fonts. Sem internet, o site usa uma fonte do sistema.
- Não há Instagram nem depoimentos no site. Para incluir, é preciso acrescentar as seções no HTML.
