
`Atividade prática de excel.`

# Gigs IRPF

Planilha em Excel para juntar de um jeito organizado, tudo que você precisa na hora de declarar o Imposto de Renda.

## O que ela faz

- **Menu lateral**
- **Aba TITULAR**: seus dados pessoais com máscara automática de CPF, CEP `00000-000`, celular `(21) 90000-0000` e checagem de e-mail. Tem um mini formulário **Sim/Não** com lista suspensa.
- **Aba INFORMES**: um informe de rendimento por linha. Escolha o tipo e a planilha descobre a **ficha do IRPF** onde ele entra. Dá pra filtrar por qualquer coluna, e o total acompanha o filtro.
- **Aba GUIA & LINKS**: atalhos oficiais da Receita, contagem regressiva do prazo e checklist de documentos.

## Como usar

1. Abra a aba **TITULAR** e preencha só as células (as 3 primeiras linhas de INFORMES e os dados do titular são exemplos fictícios: apague e use os seus).
2. Digite CPF, CEP, celular e CNPJ **só com números**: a máscara aparece sozinha.
3. Em **INFORMES**, registre cada rendimento. A coluna **Status** avisa o que está faltando ou errado.
4. Use o **checklist** da aba GUIA para não esquecer nenhum documento.

## Casos de uso

- Juntar informes de várias fontes (empresa, banco, corretora) num lugar só.
- Ver na hora quanto recebeu e quanto de IR foi retido.
- Descobrir quais informes ainda estão sem comprovante.
- Saber quantos dias faltam para o prazo de entrega.

## Funções usadas

| Funções | Onde aparece |
|---|---|
| `PROCV` | INFORMES busca a ficha e a tributação do tipo de rendimento na tabela da aba GUIA |
| `DIREITA` | Exibe os 2 últimos dígitos do CPF (mascarado) e monta o mês da competência |
| `DATADIF` | Idade do titular (anos e meses), dias desde o recebimento e dias até o prazo |
| `ANO`, `MÊS`, `DIA` | Competência (mm/aaaa) e checagem do ano-base dos informes |
| Filtros | Cabeçalho da tabela de INFORMES, com `SUBTOTAL` que respeita o filtro |
| Formatação condicional | Status verde/amarelo/vermelho, Sim/Não colorido, campos que não se aplicam ficam cinza, alerta de prazo |
| Validação de dados | Listas Sim/Não, estado civil, UF, tipos, datas, CPF, CNPJ e valores |
| Máscaras de formato | CPF, CEP, celular, CNPJ, título de eleitor |

## Observações

- Os dados e o prazo de entrega que vêm preenchidos são **exemplos**: confira a data no calendário oficial da Receita.
- A tabela de tipos de rendimento (aba GUIA) é editável. Ela alimenta a lista suspensa e o `PROCV`.
- É uma ferramenta de **organização**, não substitui o programa oficial da Receita nem orientação de contador.
- Feito para Excel. Em outros programas o visual pode variar um pouco.
