# 📝 Sistema de Gerenciamento de Notas em Python

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Educação](https://img.shields.io/badge/Aplicação-Gestão%20Acadêmica-blue?style=for-the-badge)](https://www.python.org/)
[![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)](LICENSE)

Sistema acadêmico em **Python** para cadastro de turmas, processamento de avaliações teóricas e práticas, cálculo de médias ponderadas e emissão do status final de aprovação dos estudantes.

---

## 📐 Fórmulas e Regras de Negócio

O sistema aplica os seguintes critérios de avaliação para cada estudante:

1. **Média Teórica ($MT$):** Ponderação entre as provas teóricas $T_1$ e $T_2$:
   $$MT = 0.4 \times T_1 + 0.6 \times T_2$$

2. **Média Prática ($MP$):** Média aritmética simples entre os projetos práticos $P_1$ e $P_2$:
   $$MP = \frac{P_1 + P_2}{2}$$

3. **Média Final ($MF$):**
   - Se $MT > 5.0$ e $MP > 5.0$:
     $$MF = 0.3 \times MP + 0.7 \times MT$$
   - Caso contrário (se alguma das médias for $\le 5.0$):
     $$MF = \min(MT, MP)$$

4. **Resultado Acadêmico:**
   - **Aprovado:** $MF \ge 5.0$
   - **Reprovado:** $MF < 5.0$

---

## 📊 Relatório Gerado

Ao finalizar o processamento da turma, o programa exibe uma listagem formatada com:
- Nome do estudante
- Notas individuais ($T_1, T_2, P_1, P_2$)
- Médias parciais ($MT, MP$)
- Média Final calculada ($MF$)
- Situação final (**Aprovado** ou **Reprovado**)

---

## 🚀 Como Executar

```bash
# Clonar o repositório
git clone https://github.com/lucaxaviers/sistema-notas-python.git

# Acessar a pasta
cd sistema-notas-python

# Executar o programa
python SistemaNota.py
```

---

> **Desenvolvido por Lucas Rodrigues Xavier**  
> *Projeto acadêmico focado em computação matemática e algoritmos estruturados.*
