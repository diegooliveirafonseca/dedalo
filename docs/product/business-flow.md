# Fluxo de Negócio

# Fluxo de Ajustes (MVP)

## Objetivo

Esse documento tem como objetivo representar como ocorre o fluxo de atendimento dentro de um ateliê de costura, desde a recepção do cliente até a entrega da peça ao final do(s) serviço(s).

Esse documento servira como base para a modelagem de entidades, regras de negócios e funcionalidades do Dedalo.

## Fluxo Principal

1. Cliente chega ao ateliê para solicitação de um ou mais serviços.

2. É verificado se o mesmo cliente já possui cadastro. 
    2. 1. Se sim, segue o atendimento
    2. 2. Se não, efetua o cadastro do cliente

3. Recebe uma ou mais peças
    3. 1. Cadastrar peça(s)
    3. 2. Registrar medidas se necessário

4. Selecionar serviços desejados

5. Criar orçamento
    5. 1. Se cliente não aprovou, encerra o orçamento
    5. 2. Se aprovar, gera um pedido

6. Entra em produção

7. Serviço finalizado
    7. 1. Cliente é avisado
    7. 2. Se não aprovar o serviço, volta para produção

8. Pagamento

9. Entrega

10. Pedido finalizado

## Regras de Negócio

# RN-001
- Um orçamento pode conter uma ou mais peças.

# RN-002
- Cada peça pode possuir um ou mais serviços.

# RN-003
- Um orçamento somente poderá gerar um pedido após aprovação

# RN-004
- Um pedido deve estar vinculado a exatamente um orçamento

# RN-005
- Um orçamento rejeitado nunca poderá gerar um pedido

## Possíveis Cenários Futuros

# Fluxo de Confecção (Versão Futura)

- Não implementado na versão 1.0.

- Planejado para versão 2.0.

## Fluxo Principal

1. Cliente chega ao ateliê para solicitação de um ou mais serviços.

2. É verificado se o mesmo cliente já possui cadastro. 
    2. 1. Se sim, segue o atendimento
    2. 2. Se não, efetua o cadastro do cliente

3. Entender a necessidade do cliente quanto a confecção da peça.

4. Definir o modelo

5. Tirar medidas

6. Escolher tecido 

7. Criar orçamento
    7. 1. Se cliente não aprovou, encerra o orçamento
    7. 2. Se aprovar, gera um pedido

8. Entra em produção

9. Primeira prova

10. Ajustes se necessário

11. Nova prova se necessária

12. Serviço finalizado
    12. 1. Cliente é avisado
    12. 2. Se não aprovar o serviço, volta para produção

13. Pagamento

14. Entrega

15. Pedido finalizado

## Regras de Negócio

# RN-001
- Utilizará as mesmas regras do serviço de ajustes acrescentadas das regras abaixo

# RN-002
- No momento do orçamento é decidido com o cliente se o mesmo irá fornecer o tecido. Caso ele forneça o tecido, o pagamento será somente na entrega do serviço. Caso não forneça o tecido, é necessário pagar 50% do valor do orçamento para que o serviço entre em produção.