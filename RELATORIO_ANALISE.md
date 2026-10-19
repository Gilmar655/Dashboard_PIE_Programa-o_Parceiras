# Conferência técnica — Comitê PIE (19/10/2026)

Fonte: Comite_19_10_2026_periodo__05_22_novembro.xlsx. Base integral da aba **Base_Sigeo**; aba **Comitê** usada para conferir os registros sujeitos à regra CHI > 1.500. Período **05 a 22/11/2026**.

## Validações principais

| Indicador | Resultado |
|---|---:|
| Programações da Base_Sigeo | **71** |
| Projetos distintos | 70 |
| Projetos FI | 41 |
| Projetos PIE | 30 |
| Liberado para Documentação | 46 |
| Pendente de Aprovação | 25 |
| Região LES | 62 |
| Região ABC | 9 |
| Start Engenharia | 40 |
| Conecta Obras Extras | 20 |
| Engelmig | 10 |
| Start (contrato antigo) | 1 |
| Selecionados para Comitê | **25** |
| Comitê e pendentes de aprovação | 16 |
| CHI somado de todos os registros | **153.183** |
| CHI somado dos registros em Comitê | **137.365** |
| Solicitações textuais de viabilidade de gerador | 18 |
| Programações em fim de semana | 23 |
| PowerON com número preenchido | 0 |

## Regra do Comitê

A coluna **Decisão Comitê** está marcada como `SIM - COMITÊ` em exatamente 25 linhas; todas apresentam CHI superior a 1.500. A aba Comitê contém 25 registros correspondentes aos mesmos projetos da base principal.

Por contratada: Conecta Obras Extras (15), Start Engenharia (6), Engelmig (4).

## Observações de qualidade e interpretação

- O CHI é somado **por registro da base**, sem deduplicação. Há 9 programações no equipamento `353ET021648` em 14/11/2026, cada uma com o mesmo CHI de 10.052. A soma não comprova impactos independentes nem quantidade de clientes únicos.
- `DMP/A.LES.26.03105` consta em mais de uma data/equipamento; manter ambos os registros, sem considerar automaticamente erro ou execução duplicada.
- Todos os 71 registros possuem o campo PowerON vazio. Isso não comprova ausência de tratativa no sistema, apenas ausência do dado no arquivo informado.
- Há registros programados de madrugada. Verificar a fonte original antes de interpretar datas incorporadas aos campos de horários.
- Não inferir conclusão operacional, aprovação externa ou instalação de gerador a partir da solicitação de viabilidade.

## Publicação

O site lê automaticamente `programacoes.js` (71 linhas) no GitHub Pages e permite explorar CHI, status, decisão comitê, solicitação de gerador, filtros e exportações. `programacoes.csv` foi atualizado com os registros da mesma base.

Arquivo de referência não incluído na publicação: a planilha completa contém outras abas e formatação extensa. Todos os dados disponibilizados publicamente devem ser aprovados para divulgação conforme as regras internas.
