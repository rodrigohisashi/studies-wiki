# Anotações do Livro "O Programador Pragmático"

---

## Capítulo 1 – Uma Filosofia Pragmática

### Dica 1: Assuma as Responsabilidades

- Não culpe outras pessoas pelos problemas ou dificuldades que surgirem. Assuma controle e responsabilidade pelas situações.
- Planeje sempre com antecedência. Se algo puder dar errado, antecipe-se com um plano de contingência.
- Ofereça opções claras e soluções práticas, evitando desculpas superficiais.
- Ao assumir responsabilidades, você ganha credibilidade e confiança, facilitando a resolução efetiva de problemas.

---

### Dica 4: Não Tolere Janelas Quebradas

- Corrija bugs e faça pequenas refatorações sempre que encontrar problemas no código.
- Nunca deixe uma parte do sistema quebrada ou mal estruturada ao passar por ela. Pequenas melhorias frequentes mantêm o sistema limpo e estável.
- Uma única "janela quebrada" (bug ignorado ou código ruim) pode levar rapidamente à degradação geral do projeto.

---

### Dica 7: Encare a Qualidade como um Requisito Essencial

- Qualidade não é um bônus; é parte integrante dos requisitos do projeto.
- Defina critérios claros e mensuráveis de qualidade desde o início, evitando retrabalho e custos adicionais no futuro.

---

### Dica 8: Comunique-se com Clareza

- Comunique-se levando em consideração seu público-alvo, ouvindo atentamente e compreendendo suas necessidades.
- Concentre-se em soluções práticas e evite reclamações ou conflitos improdutivos.
- Comunicação aberta e transparente fortalece a equipe e melhora os resultados.

---

## Capítulo 2 – Uma Abordagem Pragmática

### Dica 11: Não Se Repita (NSR)

Evite duplicações no código e nas informações. Duplicações aumentam a complexidade, favorecem erros e dificultam a manutenção.

#### Tipos de Duplicação

**1. Duplicação Imposta**

- Surge devido a limitações externas (frameworks ou bibliotecas).
- Solução sugerida: Utilize ferramentas, geradores de código ou filtros automáticos para lidar com essas duplicações.

**2. Duplicação Inadvertida**

- Acontece quando você replica informações ou funcionalidades sem perceber.
- Exemplo:

```java
class Line {
  public Point start;
  public Point end;
  public double length;
}
```

Neste caso, o atributo `length` está duplicado, pois pode ser calculado diretamente pelos pontos `start` e `end`.

- Solução sugerida: Revise frequentemente o código e faça revisões entre colegas para identificar e eliminar duplicações inadvertidas.

**3. Duplicação Impaciente**

- Surge quando há pressão por prazos e o desenvolvedor cria duplicações para entregar rápido.
- Alerta: Esses atalhos resultam em custos maiores futuramente. Avalie cuidadosamente antes de duplicar código.

**4. Duplicação Entre Desenvolvedores**

- Ocorre quando diferentes desenvolvedores implementam soluções semelhantes devido à falta de comunicação.
- Solução sugerida: Estimule colaboração constante e promova revisões regulares de código para compartilhar conhecimento.

---

### Dica 12: Facilite a Reutilização

- Escreva código modular, flexível e claramente documentado.
- Utilize padrões e convenções reconhecidas pela equipe, facilitando entendimento e reutilização.
- Compartilhe soluções eficazes para reduzir esforços repetitivos e aumentar a produtividade da equipe.

---

### Dica 13: Ortogonalidade – Elimine Efeitos Colaterais de Elementos Não Relacionados

Ortogonalidade significa independência ou separação clara entre componentes. Em sistemas ortogonais, mudanças em um módulo não afetam módulos não relacionados.

#### Importância da Ortogonalidade

- Problemas ficam isolados em módulos específicos, simplificando correções.
- Código ortogonal facilita testes, permitindo avaliações isoladas.
- Mudanças têm impacto limitado, reduzindo a fragilidade do sistema.
- Melhora a manutenibilidade e estabilidade do sistema ao longo prazo.

#### Teste para Ortogonalidade

Questione-se:  
"Se eu alterar drasticamente os requisitos de uma função específica, quantos módulos serão afetados?"

Em um sistema ortogonal, apenas um módulo deveria ser afetado.

#### Boas Práticas para Ortogonalidade

- Evite usar dados globais, pois eles criam dependências ocultas.
- Mantenha os módulos claramente desacoplados, cada um com responsabilidade única.
- Evite redundância ou funções similares que fazem a mesma coisa.
- Promova reversibilidade, permitindo facilmente desfazer alterações caso necessário.
