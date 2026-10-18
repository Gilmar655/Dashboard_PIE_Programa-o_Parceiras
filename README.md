# Painel PIE — Programação das Parceiras

Site público: https://gilmar655.github.io/Dashboard_PIE_Programa-o_Parceiras/

Repositório: https://github.com/Gilmar655/Dashboard_PIE_Programa-o_Parceiras

## Correção dos caminhos (18/10/2026)

**Os arquivos foram publicados diretamente na raiz do repositório.** O HTML agora aponta para esses arquivos com o prefixo `./` e não mais para as pastas inexistentes `assets/` e `dados/`. Assim, a base inicial de **65 programações** é carregada automaticamente por `programacoes.js`.

**Estrutura exigida na branch main, pasta / (root):**

```text
index.html
styles.css
app.js
charts.js
excel.js
programacoes.js
programacoes.csv
enel-brasil-logo.png
favicon.svg
README.md
RELATORIO_ANALISE.md
```

O arquivo XLSX original é apenas um documento de referência; os visitantes não precisam importar a planilha para visualizar o painel.

## Atualização pelo GitHub Pages

1. Em **Settings → Pages**, verifique se a publicação está configurada para **Deploy from a branch → main → / (root)**.
2. Aguarde o Pages atualizar o commit e abra o link acima.
3. Se aparecer a versão antiga, pressione **Ctrl + F5**.
4. Para publicar dados atualizados, importe a nova planilha no painel, clique **Base para GitHub** e substitua o arquivo `programacoes.js` **na raiz**, fazendo commit. A importação no navegador não sincroniza automaticamente com o GitHub.

O painel oferece filtros, 6 gráficos interativos, tabela de registros, alertas, Excel/CSV e logomarca da Enel Brasil. O relógio utiliza o fuso `America/Sao_Paulo` e atualiza a cada segundo.

**Atenção:** este repositório é público. Confirme autorização para divulgação externa de informações operacionais antes de incluir outras bases ou dados sensíveis.
