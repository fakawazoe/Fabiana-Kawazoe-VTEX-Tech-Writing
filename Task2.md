# Métodos de pagamento na VTEX
O método de pagamento que você oferece em seu estabelecimento pode infulenciar diretamente as suas vendas. Por isso, na VETX, oferecemos os seguintes métodos de pagamento:
- Cartão de crédito
- Cartão de débito
- Dinheiro
- Pagamentos pesonalisados
  - Promissórias
  - Private-label
  - Co-branded

Além de pagamentos regionais:
- Pagamentos instantâneos (como o Pix no Brasil)
- Boletos bancários

> ##### Nota
>
> Os método de pagamento variam de país para país. Confira nossa documentação [aqui](https://help.vtex.com/en/tutorial/list-of-payment-providers-by-country--2im3BEGXxSAcRuxEaIHPvp) para uma lista de provedores de pagamento que temos disponível para cada país. 

## Fluxo de transação
A troca de ativos durante uma compra e venda de produtos e serviços é também conhecida como transação. Na VTEX, as transações seguem o fluxo demosntrado no gráfico e explicado mais abaixo:

``` mermaid
stateDiagram-v2 
s1: 1. Processo de autorização
s2: 2. Análise de risco (opcional)
s3: 3. Transação aprovada
s4: 4. Processo de liquidação financeira
s5: 5. Transação concluída

    [*] --> s1
    s1 --> s2
    s2 --> s3
    s3 --> s4
    s4 --> s5
    s5 --> [*]
```

#### 1. Processo de autorização
Este é o primeiro passo. Neste passo, as informações são mandadas para o adquirente (ou para um *gateway* de pagamento). O adquirente manda as informações para o banco emissor, que responde se a transação deve ser autorizada ou não.
Se a transação não for autorizada, ela será cancelada.

#### 2. Análise de risco (opcional)
Após a autorização do banco emissor, caso o cliente queira, o sistema anti-fraude analisará o risco da transação. Caso o sistema identifique uma fraude, a transação será cancelada.

> Apesar desse passo ser opcional, ele é altamente recomendado para a verificação de suas transações.

#### 3. Transação aprovada
Uma vez que todas as verificações tenham sido feitas, a transação é marcada como aprovada. No entando, o valor da transação ainda não foi liquidado.

#### 4. Processo de liquidação financeira
Este processo contem três passos:
- Início da liquidação: este é apenas um aviso de que o processo foi iniciado;
- Liquidação em andamento: Os sistemas de liquidação estão verificando se os valores estão realmente disponíveis para à transação;
- Liquidação concluída: Os valores foram liquidados e os conectores passam a ser responsáveis por debitar/creditar os valores nas respectivas contas.

#### 5. Transação concluída
Por último, a transação é faturada e o recibo é emitido (em tela ou em papel). 
