# Painel PIE | Programação das Parceiras

**Site HTML estático, pronto para GitHub Pages.** Construído a partir da aba `PIE` da planilha fornecida, com apoio do HTML e do PDF de referência. A base original possui 65 registros (20/10/2026–22/11/2026). Não há dependências de JavaScript externas: os gráficos são SVG nativos e o leitor/escritor XLSX funciona diretamente no navegador Chrome/Edge atualizado.

## 1. Publicar no GitHub Pages

1. Crie um repositório no GitHub ou abra o repositório em que deseja publicar o site.
2. Extraia o ZIP **antes de enviar os arquivos**.
3. Envie o conteúdo da pasta `PIE_Painel_GitHub` para a **raiz** do repositório, mantendo `index.html` na raiz e as pastas `assets` e `dados`.
4. Abra **Settings → Pages**, selecione **Deploy from a branch**, escolha a branch `main` e a pasta `/ (root)`; salve.
5. O link ficará no formato `https://SEU_USUARIO.github.io/NOME_DO_REPOSITORIO/`. Aguarde a publicação e recarregue o navegador.

**Importante:** não envie a pasta ZIP sem extrair; o GitHub Pages precisa encontrar `index.html` na raiz da branch configurada.

## 2. O que o site oferece

- KPIs: total de programações, soma de horas, duração média, liberação de execução, pendências e ausência de número PowerON.
- Filtros cumulativos: pesquisa em todos os campos operacionais, intervalo de datas, status, região, contratada, serviço, PowerON, semana, equipamento, tipo de intervenção e finais de semana.
- Seis gráficos SVG interativos, incluindo carga diária, distribuição por status, contratadas, serviços, semanas e PowerON; clicar em um elemento aplica/remove filtro.
- Pontos de atenção calculados a cada filtro: aprovação pendente, status PowerON que merece conferência, projetos em múltiplas datas, programações aos fins de semana, concentração equipamento/dia e horários fora do padrão.
- Tabela inferior com **as 13 colunas originais** e uma coluna derivada para classificação PowerON; rolagem, ordenação e paginação.
- Importar arquivos `.xlsx`, `.xlsm` ou `.csv` com cabeçalhos equivalentes aos da aba `PIE`. Importações **substituem** a base da sessão/navegador, sem juntar com os dados antigos.
- Exportar **apenas os registros atualmente filtrados** em `.csv` ou `.xlsx`.
- Relógio local com data, layout responsivo e modo de impressão.

## 3. Atualizar a base e publicar novos dados

O GitHub Pages é um **site estático**. Um site aberto no navegador **não pode ler continuamente um arquivo de `C:\...` ou OneDrive de outra pessoa** e **não grava automaticamente** mudanças no repositório.

A atualização foi desenhada para ser transparente:

1. No site, clique **Importar Excel / CSV** e escolha a nova planilha.
2. Confira contagens, filtros, gráficos e registros na tabela. A importação fica armazenada **somente no navegador usado** (se o navegador permitir armazenamento local).
3. Clique **Base para GitHub**. Isso baixa um arquivo chamado `programacoes.js` com a base importada completa, independentemente dos filtros atuais.
4. No GitHub, substitua `dados/programacoes.js` pelo arquivo baixado e faça o commit. O site passa a apresentar a nova base para **todos** os visitantes quando o GitHub Pages publicar a alteração.
5. Se quiser atualizar também os arquivos de referência, substitua `dados/programacoes.csv` e o `.xlsx` original. Para isso, exporte primeiro toda a base (limpe os filtros).

**Restaurar** descarta as importações locais do navegador e volta para a base publicada no arquivo `dados/programacoes.js`.

## 4. Estrutura

```text
PIE_Painel_GitHub/
├── index.html                 site principal
├── .nojekyll                  GitHub Pages serve os arquivos diretamente
├── assets/
│   ├── styles.css             identidade visual, responsividade e impressão
│   ├── app.js                 filtros, KPIs, tabela, auditoria e ações
│   ├── charts.js              gráficos SVG interativos
│   ├── excel.js               importação/exportação CSV e XLSX sem bibliotecas externas
│   └── favicon.svg
├── dados/
│   ├── programacoes.js        dados que o site lê (65 registros no lançamento)
│   ├── programacoes.csv       cópia tabular inicial
│   └── PROGRAMAÇÃO_PIE_Parceiras_outubro_novembro.xlsx
└── RELATORIO_ANALISE.md       validação dos dados e observações
```

## 5. Atenção sobre privacidade e acesso

Se usar um repositório **público**, o site e as planilhas publicadas poderão ser consultados por qualquer pessoa com acesso ao endereço — inclusive números PowerON, equipamentos e nomes de contratadas. Confirme previamente se a divulgação externa desses dados é autorizada pela organização.

## 6. Compatibilidade e limitações

- Abra `index.html` diretamente para visualizar a base incluída; não precisa de hospedagem para a visualização inicial.
- Importação de XLSX usa recursos modernos de descompactação presentes nas versões recentes de Chrome e Edge. Se o navegador não suportar, use exportação CSV no Excel e importe o `.csv` no site.
- CSV utiliza ponto e vírgula (com valores entre aspas, quando necessário). Datas devem estar em `dd/mm/aaaa` ou `aaaa-mm-dd`.
- Para manter a rastreabilidade, o site não presume que duas programações do mesmo projeto representam erro: ele apenas as sinaliza para verificação.
- Duração total é uma **soma de horas por registro**; quando há vários projetos na mesma janela não corresponde automaticamente a horas de equipes, recursos exclusivos ou horas de indisponibilidade sem sobreposição.
- A coluna `Tipo Intervencao` está preenchida como `PIE` em todos os 65 registros; os tipos de serviço do gráfico são extraídos de `Descrição do Projeto`.
