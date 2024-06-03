# Ferramenta de Simulação de Autômato Finito

## Descrição

Esta ferramenta é projetada para simular um autômato finito determinístico (DFA). A ferramenta lê a definição do autômato a partir de um arquivo JSON e uma série de strings de entrada a partir de um arquivo CSV. Em seguida, processa cada string de entrada através do autômato e gera um arquivo CSV de saída com os resultados.

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
```

### Arquivo CSV de Entrada (ex1_input.csv)
```csv
ba
aaaabbbbbaaaaa
abababab
bbbbbbbb
aaaaaaaaaaaa
aaaaabaaaaa
```

### Resultado (saida_output.csv)

```csv
ba;1;1;0.00000420
aaaabbbbbaaaaa;1;1;0.00000380
abababab;0;0;0.00000160
bbbbbbbb;0;0;0.00000170
aaaaaaaaaaaa;0;0;0.00000210
aaaaabaaaaa;1;1;0.00000190
```