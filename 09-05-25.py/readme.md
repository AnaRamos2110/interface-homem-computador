# Exercício 1 - Análise de Lucro/Prejuízo em Vendas de Refrigerantes

## Objetivo
Calcular se uma empresa obteve lucro ou prejuízo na venda de latas de refrigerante (Coca-Cola e Pepsi), comparando o faturamento com o investimento inicial.

## Código
```python
# Quantidades vendidas
qnt_coca = 100  # Quantidade de latas de Coca-Cola vendidas
qnt_pepsi = 50  # Quantidade de latas de Pepsi vendidas

# Valores unitários
valor_da_coca = 4.50  # Preço de cada lata de Coca-Cola
valor_da_pepsi = 3.90  # Preço de cada lata de Pepsi

investimento = 6000  # Valor total investido nos produtos
linha = '-' * 63  # Linha divisória para formatação

# Cálculo e exibição do faturamento
print('\n' + linha)
print(f"Total de vendas de Coca-Cola: R$ {qnt_coca * valor_da_coca:,.2f}")
print(f"Total de vendas de Pepsi: R$ {qnt_pepsi * valor_da_pepsi:,.2f}")

faturamento = (qnt_coca * valor_da_coca) + (qnt_pepsi * valor_da_pepsi)
print(f"\nFaturamento total: R$ {faturamento:,.2f}")
print(linha)

# Verificação de lucro ou prejuízo
if faturamento > investimento:
    print('\n' + linha)
    print('Resultado: A empresa obteve LUCRO nas vendas.')
    print(linha)
else:
    print('\n' + linha)
    print('Resultado: A empresa obteve PREJUÍZO nas vendas.')
    print(linha)
Explicação
Variáveis:

qnt_coca e qnt_pepsi armazenam as quantidades vendidas.

valor_da_coca e valor_da_pepsi definem os preços unitários.

investimento é o custo total inicial.

Cálculos:

Multiplica quantidade pelo preço para cada produto.

Soma os resultados para obter o faturamento total.

Condicional (if):

Compara faturamento com investimento para determinar lucro ou prejuízo.

Formatação:

Usa linha para separar visualmente as seções no terminal.


---

### **📁 Exercicio2.py**  
```markdown
# Exercício 2 - Classificação de Bebidas por Código

## Objetivo
Identificar se uma bebida é alcoólica ou não com base no código inserido pelo usuário, utilizando a função `in` para verificar padrões.

## Código
```python
# Códigos de referência
cod_bebida_alcoolica = 'BCA001'  # Padrão para bebidas alcoólicas
cod_bebida_nao_alcoolica = 'BSA001'  # Padrão para bebidas não alcoólicas
linha = '-' * 63  # Linha divisória

# Entrada do usuário
print('\n' + linha)
codigo = input("Insira o código da bebida (em MAIÚSCULAS): ")

# Verificação do código
if 'BCA' in codigo:
    print('\n' + linha)
    print(f"Classificação: Bebida ALCOÓLICA. Código: {cod_bebida_alcoolica}")
    print(linha)
else:
    print('\n' + linha)
    print(f"Classificação: Bebida NÃO ALCOÓLICA. Código: {cod_bebida_nao_alcoolica}")
    print(linha)
Explicação
Lógica:

Se o código contém a substring 'BCA', a bebida é classificada como alcoólica.

Caso contrário, é considerada não alcoólica.

Função in:

Verifica a existência de uma substring dentro da string inserida pelo usuário.

Formatação:

linha melhora a legibilidade da saída no terminal.


---

### **📁 Exercicio3.py**  
```markdown
# Exercício 3 - Análise de Lucro Mensal

## Objetivo
Calcular o lucro ou prejuízo de uma empresa com base no faturamento e custos mensais.

## Código
```python
linha = '-' * 63  # Linha divisória

# Entrada de dados
faturamento = int(input("Faturamento mensal (R$): "))
custo = int(input("Custo mensal (R$): "))

# Cálculo do lucro
lucro = faturamento - custo
print('\n' + linha)
print(f"Lucro/Prejuízo: R$ {lucro:.2f}")
print(linha)

# Condicional
if lucro > 0:
    print('\n' + linha)
    print("Resultado: Lucro positivo.")
    print(linha)
else:
    print('\n' + linha)
    print("Resultado: Prejuízo.")
    print(linha)
Explicação
Variáveis:

faturamento e custo são inputs do usuário.

lucro é a diferença entre os dois valores.

Condicional:

Se lucro > 0, há lucro. Senão, há prejuízo.

Formatação:

Valores monetários são exibidos com 2 casas decimais (:.2f).


---

### **📁 Exercicio4.py**  
```markdown
# Exercício 4 - Sistema de Metas de Vendas com Bônus

## Objetivo
Verificar se uma equipe atingiu a meta de vendas e calcular bônus conforme o desempenho (2x ou 3x a meta).

## Código
```python
meta = 40000  # Valor da meta base
linha = '-' * 63  # Linha divisória

# Entrada de dados
print(linha)
equipe = input("Nome da equipe: ")
vendas = float(input("Total de vendas (R$): "))

# Lógica de bônus
if vendas >= meta * 3:
    bonus = 0.07 * vendas
    print(f"Status: Meta superada (3x). Bônus de 7%: R$ {bonus:.2f}")
elif vendas >= meta * 2:
    bonus = 0.03 * vendas
    print(f"Status: Meta superada (2x). Bônus de 3%: R$ {bonus:.2f}")
elif vendas >= meta:
    print("Status: Meta atingida.")
else:
    print(f"Status: Meta não atingida. Faltam: R$ {meta - vendas:.2f}")
print(linha)
Explicação
Hierarquia de Condições:

Verifica primeiro os cenários mais lucrativos (3x a meta).

Depois, 2x a meta e, por fim, meta simples.

Bônus:

7% para vendas ≥ 3x a meta.

3% para vendas ≥ 2x a meta.

Formatação:

Valores monetários formatados com 2 casas decimais.


---

### **Instruções para GitHub/VSCode**  
1. **Para cada arquivo `.py`**:  
   - Copie apenas o conteúdo dentro dos blocos ````python`.  
   - Salve com os nomes `Exercicio1.py`, `Exercicio2.py`, etc.  

2. **Para documentação (README.md)**:  
   - Cole os Markdowns completos acima em um arquivo `README.md`.  

Cada seção inclui:  
- **Objetivo**: Descrição clara do propósito do código.  
- **Código**: Estrutura completa e comentada.  
- **Explicação**: Detalhamento de variáveis, lógica e formatação.  
