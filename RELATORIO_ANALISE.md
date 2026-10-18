# Conferência e análise da base PIE – out/nov 2026

Fonte prioritária: planilha `PROGRAMAÇÃO_PIE_Parceiras_outubro_novembro.xlsx`, aba `PIE` (65 linhas de dados e 13 colunas). Material de apoio: `Painel PIE – Programação das parceiras (out_nov 2026) (1).html` e `Dashboard interativo com gráficos e filtros - 19_10_2026.pdf`.

## Contagens validadas

| Indicador | Resultado |
|---|---:|
| Programações | 65 |
| Projetos distintos | 60 |
| Intervalo de datas | 20/10/2026 a 22/11/2026 |
| Liberado para Execução | 23 (35,4%) |
| Liberado para Documentação | 20 (30,8%) |
| Pendente de Aprovação | 22 (33,8%) |
| Regional LES | 58 |
| Regional ABC | 7 |
| Engelmig | 25 |
| Conecta Obras Extras | 24 |
| Start Engenharia | 15 |
| Start (contrato antigo) | 1 |
| Serviço Rede Compacta | 37 |
| Afastamento de Rede (Clientes) | 15 |
| Alteração de Carga | 5 |
| Ligação Nova | 4 |
| Migração para Média Tensão | 2 |
| Reforma de Rede Secundaria RTRI | 1 |
| Substituição de Poste em Mau Estado | 1 |
| PowerON sem número informado | 42 |
| PowerON com número numérico | 9 |
| PowerON Devolvido | 7 |
| PowerON Resolvido (independente de maiúsculas) | 7 |
| Sábados ou domingos | 22 |
| Soma de duração programada | 261,5 horas |
| Média por registro | 4,023 horas |

## Ocorrências para verificação

1. **22 programações pendentes**; data mais próxima na base: 28/10/2026, com projeto `DMP/A.LES.22.01917` entre os programados nesta data.
2. **14 programações liberadas para execução** com campo PowerON textual `DEVOLVIDO` ou `RESOLVIDO`. Isso é indício de conferência necessária, **não prova de irregularidade**.
3. **5 projetos** aparecem em mais de uma data: `DMP/A.LES.22.02023`, `DMP/A.LES.22.01894`, `DMP/A.LES.21.16603`, `DAC/A.LES.26.00600`, `DMP/A.LES.26.03105`. Podem representar reprogramações ou diferentes registros; não remover automaticamente.
4. **22 registros em fim de semana** (33,8%).
5. **9 programações no equipamento `353ET021648` em 14/11/2026**, agrupadas na mesma janela. São nove projetos, não necessariamente nove equipes ou nove desligamentos.
6. **4 registros** com duração diferente de 4 horas ou início antes de 06h:
   - `DMP/A.LES.26.01039` — 10:00–13:00 (3 h)
   - `DAC/A.LES.26.00849` — 10:00–16:00 (6 h)
   - `DAC/A.LES.26.00586` — 10:00–14:30 (4,5 h)
   - `DAC/A.LES.25.00749` — 00:30–04:30 (4 h, madrugada)

**Diferença em relação ao PDF/HTML de referência:** o painel anterior destacava três casos de duração/horário atípicos e omitia o registro de 3 h `DMP/A.LES.26.01039`; a base Excel contém quatro ocorrências segundo o critério indicado. O valor visual de 262 h no painel anterior resulta do arredondamento de 261,5 h, não de divergência nos lançamentos.

## Critérios de análise

- Indicadores derivam de cada linha, **sem deduplicação**: 65 programações não significam necessariamente 65 projetos únicos.
- `Contratada` é mantida integralmente nos dados e no título da célula da tabela; abreviação de nome é apenas para visualização.
- `PowerON` é classificado como **Com número** se só contém dígitos, **Sem número** se vazio, ou como **Devolvido/Resolvido** por comparação textual sem diferença entre maiúsculas/minúsculas. Nunca transformar estes textos em números.
- `Duração (h)` vem da planilha Excel; horários são apresentados no formato HH:MM e preservados. A soma é por linha, inclusive casos com projetos associados à mesma janela.
- `Visível` tem valor `1` nas 65 linhas originais; não foram excluídos registros dessa coluna.
- `Tipo Intervencao` é `PIE` em todas as linhas. Não se deve confundir essa coluna com `Descrição do Projeto` (usada como categoria de serviço nos gráficos).
- Após importação, todos os indicadores passam a ser recalculados; não foram codificados valores fixos de 65/23/22 no processamento.
