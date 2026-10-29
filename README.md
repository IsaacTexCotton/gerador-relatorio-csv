# Gerador de Relatórios — Tex Cotton

Aplicação estática para gerar arquivos CSV de cobrança a partir de uma planilha Excel/CSV. O processamento acontece localmente no navegador.

## Executar

Abra `index.html` no Chrome ou Microsoft Edge e selecione a planilha. A base deve estar na primeira aba e usar as colunas A–P esperadas pelo gerador.

1. Selecione a data dos arquivos.
2. Clique em **Gerar CSVs**.
3. Baixe o ZIP ou salve os CSVs e o ZIP em uma pasta compatível com a File System Access API.

As bibliotecas XLSX e JSZip são carregadas por CDN, portanto é necessário acesso à internet para carregá-las.

## Correção do seletor de pastas

O seletor de pastas do navegador não pode ser aberto em alguns contextos de iframe de outra origem. O app detecta quando está incorporado e desabilita **Salvar CSVs + ZIP na pasta**, exibindo uma orientação; o download do ZIP continua disponível. O salvamento direto deve ser usado com a aplicação aberta em uma aba própria do Chrome/Edge.

## Publicar com GitHub Pages

Em **Settings → Pages**, configure a publicação a partir da branch `main` e da pasta `/ (root)`. Depois, abra a URL publicada diretamente em uma aba, em vez de uma pré-visualização incorporada, para usar o seletor de pastas.

A aplicação não envia a planilha para um servidor. Revise os CSVs gerados e os avisos de registros não distribuídos ou números suspeitos antes de usá-los.
