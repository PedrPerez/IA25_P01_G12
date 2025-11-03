#  IA25 Project 01 — Class Timetable Generation using CSP

**Unidade Curricular:** Artificial Intelligence  
**Ano letivo:** 2025/26  
**Tema:** Geração automática de horários de aulas usando *Constraint Satisfaction Problems (CSP)*  
**Ferramentas:** Python + Jupyter Notebook + biblioteca `python-constraint`

---

## Equipa de Trabalho

| Nome | Número |
|------|--------|
| Pedro Perez | nº18623 |
| Eduardo Matos | nº25481 |
| Thifany Antoni | nº16077 |
| Vasco Gomes | nº27955 |
| Miguel Carvalho | nº25479 |

---

##  Objetivo do Projeto

Desenvolver um **agente inteligente** capaz de gerar automaticamente horários de aulas respeitando restrições obrigatórias (*hard constraints*) e tentando satisfazer preferências desejáveis (*soft constraints*).

O agente deverá:

- Ler e processar datasets de entrada com informações sobre cursos, professores, turmas e salas
- Formular o problema como um **Constraint Satisfaction Problem (CSP)**
- Definir as variáveis, domínios e restrições de forma estruturada
- Aplicar heurísticas para otimizar a qualidade da solução
- Gerar um horário viável e equilibrado
- Produzir visualizações claras do horário gerado

---

##  Estrutura do Projeto

\`\`\`
IA25_P01_G12/
├── README.md                          # Este ficheiro
├── IA25_P01_G##_Notebook.ipynb       # Jupyter Notebook com solução completa
└── Relatório_ IA.pdf                  # Relatório do projeto
\`\`\`

---

## Tecnologias Utilizadas

- **Python 3.8+** — Linguagem de programação principal
- **Jupyter Notebook** — Ambiente interativo de desenvolvimento e documentação
- **python-constraint** — Biblioteca para resolver Constraint Satisfaction Problems



### **Restrições — Hard Constraints**

1. **Conflito de professor** — Um professor não pode lecionar duas aulas ao mesmo tempo
2. **Conflito de turma** — Uma turma não pode ter duas aulas ao mesmo tempo
3. **Conflito de sala** — Uma sala não pode ter duas aulas ao mesmo tempo
4. **Indisponibilidade de professor** — Respeitar disponibilidades dos professores
5. **Salas fixas** — Alguns cursos têm sala obrigatória
6. **Aulas online** — Aulas online limitadas a máximo 3, no mesmo dia

### **Restrições — Soft Constraints**

1. Aulas da mesma UC em dias distintos
2. Cada turma com apenas 4 dias de aulas (quando possível)
3. Aulas consecutivas no mesmo dia
4. Minimizar número de salas físicas por turma
5. Aulas online no mesmo dia
6. Máximo 3 aulas por dia por turma
