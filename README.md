# Painel Financeiro: Imóveis e Carros

Página estática (`index.html`) que lê uma planilha do Google Sheets e mostra
cartões de totais, quatro gráficos (Chart.js), tabelas e filtros, comparando o
rendimento dos imóveis com 12% ao ano da LCI.

## Privacidade

- O link ou ID da planilha **não está no código**. Ele é colado no campo a cada
  uso e não fica salvo no navegador.
- A página tem `noindex`, então buscadores não devem listá-la.
- A planilha precisa estar compartilhada como **"Qualquer pessoa com o link: Leitor"**,
  porque a página a lê direto do navegador. Ou seja: quem tiver o link da
  planilha consegue ver os dados. O link da página, sozinho, não mostra nada.

## Como usar

1. Abra a página publicada.
2. Cole o link da planilha (ou só o ID) e clique em **Processar**.

## Formato da planilha

As abas têm que manter estes nomes e esta ordem de colunas (a linha 1 é o cabeçalho):

**Página1 (imóveis):** Imóvel, Valor de compra, Manutenção acumulada,
Valor investido total, Aluguel mensal, Meses vagos no ano, Receita anual líquida,
Rendimento mensal (%), Rendimento anual (%), Valor de mercado atual.

**Carros:** Carro, Valor de compra, Gastos, Valor de venda, Lucro, Lucro (%),
Valor encaixado no imóvel, Imóvel comprado, Valor de mercado do imóvel,
Ganho de patrimônio.

Valores em reais podem estar como `R$ 1.234,56`, e porcentagens como `12,5%`.

## Publicação

GitHub Pages: Settings → Pages → Source: *Deploy from a branch* → `main` / `(root)`.

Alternativa com senha: Cloudflare Pages ligado a este repositório, com
Cloudflare Access (Zero Trust) liberando só o seu e-mail. Nesse caso o
repositório pode ser privado.
