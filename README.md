# Ferramenta de Simulação de Autômato Finito

## Descrição

Esta ferramenta é projetada para simular um autômato finito determinístico (DFA). A ferramenta lê a definição do autômato a partir de um arquivo JSON e uma série de strings de entrada a partir de um arquivo CSV. Em seguida, processa cada string de entrada através do autômato e gera um arquivo CSV de saída com os resultados.

## Funcionamento

A ferramenta realiza as seguintes etapas:

1. **Leitura da Definição do Autômato (JSON)**:
   - O arquivo JSON contém a definição do autômato, incluindo o estado inicial, os estados finais e as transições entre estados.

2. **Leitura das Strings de Entrada (CSV)**:
   - O arquivo CSV contém uma lista de strings que serão processadas pelo autômato.

3. **Processamento das Entradas**:
   - Cada string de entrada é processada pelo autômato, começando no estado inicial e seguindo as transições definidas. Se a string leva o autômato a um dos estados finais, a entrada é aceita.

4. **Geração do Arquivo de Saída (CSV)**:
   - Um arquivo CSV é gerado com o resultado do processamento de cada string de entrada, incluindo o tempo gasto no processamento.

## Exemplo de Uso

### Arquivo JSON de Exemplo (`ex1.json`)

```json
{
    "initial": 0,
    "final": [1],
    "transitions": [
        {"from": 0, "read": "a", "to": 1},
        {"from": 1, "read": "b", "to": 0}
    ]
}
