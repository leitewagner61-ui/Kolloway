# Kolloway

Site estático da Kolloway, pronto para ser enviado à raiz de um repositório no GitHub e publicado em uma hospedagem de sites comerciais.

**Domínio de destino:** https://kolloway.com.br/  
**Atendimento:** https://wa.me/5511985146611

## Uso

Não há instalação, compilação, backend, banco de dados ou chaves de API. O arquivo de entrada é `index.html`. Para uma visualização rápida, abra esse arquivo no navegador. Para validar a publicação, use o endereço fornecido pela hospedagem.

## Enviar ao GitHub

1. Crie ou abra o repositório desejado.
2. Envie **o conteúdo desta pasta**, mantendo `index.html` na raiz. Não envie apenas o ZIP nem crie uma pasta intermediária.
3. Preserve `.gitignore` e `.gitattributes`, que podem ficar ocultos no explorador de arquivos.
4. Salve o primeiro commit. O pacote não inclui histórico Git, credenciais ou configuração interna do ambiente de criação.

## Publicação e domínio

O repositório guarda o código; ele não conecta o domínio nem publica o site automaticamente. Importe o repositório na hospedagem escolhida, com suporte a uso comercial, e configure:

- Tipo: site estático, HTML/CSS/JavaScript.
- Pasta raiz e pasta de publicação: a raiz do repositório (`.`).
- Comando de instalação/compilação: nenhum.
- Entrada: `index.html`.
- Página de erro: servir `404.html` com status HTTP 404.
- Domínio principal: `kolloway.com.br`, usando HTTPS.

Use os registros DNS fornecidos pela hospedagem. Configure `www.kolloway.com.br` para redirecionar ao domínio principal e HTTP para HTTPS. Não foram incluídos IPs ou registros CNAME de um provedor ainda não escolhido.

O GitHub Pages não foi configurado neste pacote: o GitHub pode servir como repositório independentemente da hospedagem final.

## Arquivos

| Arquivo | Finalidade |
| --- | --- |
| `index.html` | Página completa, textos, perguntas frequentes e metadados |
| `styles.css` | Identidade visual e layout responsivo |
| `app.js` | Pacotes, preços, seleção de rede, detalhes e WhatsApp |
| `logo.svg`, `favicon.svg`, `sculpture.svg` | Elementos vetoriais da marca |
| `favicon.ico`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png` | Ícones para navegadores e dispositivos |
| `social-preview.png` | Imagem de compartilhamento, 1200 × 630 |
| `site.webmanifest` | Nome, cores e ícones do site; não implementa modo offline |
| `robots.txt` | Permite rastreamento e informa o endereço do sitemap |
| `sitemap.xml` | Lista a URL principal; seções com âncora não são páginas separadas |
| `404.html` | Página de endereço não encontrado |
| `.gitignore`, `.gitattributes` | Organização e padronização do repositório |

## Editar

- Textos e seções: `index.html`.
- Preços, volumes e benefícios: atualize a lista `plans` em `app.js` e os quatro cartões correspondentes em `index.html`, dentro de `#plan-grid`. Os valores devem permanecer iguais nas duas versões.
- WhatsApp: função `contactUrl` em `app.js` e links de fallback no HTML.
- Aparência: `styles.css`.
- Após mudanças relevantes na página, atualize `lastmod` em `sitemap.xml` com a data real da alteração.
- Ao trocar de domínio, atualize canonical, Open Graph, JSON-LD, `robots.txt`, `sitemap.xml` e o link de retorno de `404.html`.

## Integrações e funcionamento

Os botões abrem uma mensagem pré-preenchida no WhatsApp; o visitante confirma o envio no aplicativo. Não há checkout, cobrança automática ou formulário que armazene dados. As fontes DM Sans e Manrope são carregadas do Google Fonts; a página utiliza fontes de fallback quando esse serviço não está disponível. Os ícones e a ilustração são locais.

## Conferência após publicar

Abra a página no celular e no computador; verifique os quatro planos, o menu, os detalhes e o destino do WhatsApp. Confira os endereços `/robots.txt`, `/sitemap.xml` e `/social-preview.png`, o HTTPS e o retorno HTTP 404 em uma URL inexistente. Depois, envie o sitemap à ferramenta de busca que desejar. Metadados e sitemap ajudam o rastreamento, mas não garantem indexação ou posicionamento.

## Estado da entrega

Arquivos preparados localmente. Nenhum repositório remoto foi criado, nenhum envio ao GitHub foi realizado e nenhum DNS foi alterado por este pacote.

## SEO e buscas com IA

Título e descrição resumem a oferta paga. Os dados estruturados identificam a organização, o site e a página, usando o domínio oficial. Os quatro planos estão no HTML inicial, com os mesmos valores da versão renderizada por JavaScript. Nenhuma lista oculta de palavras-chave foi inserida.

Não há marcação especial que garanta recomendações por IA. Preserve conteúdo claro, acessível e coerente com o serviço efetivamente entregue. Após publicar, solicite o rastreamento da URL e envie o sitemap no Google Search Console.
