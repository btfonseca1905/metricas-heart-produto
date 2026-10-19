# Métricas de Produto HEART by Bruna Fonseca

Uma Skill para VS Code/Codex que ajuda Product Managers a definir **objetivos, sinais e métricas de produto** com o framework HEART, explicar o cálculo de cada indicador e, com autorização, criar um preview de dashboard executivo.

**Autoria:** Bruna Fonseca | b-a.BA Educação Corporativa | D² [do Discovery ao Delivery]

## O que a Skill faz

1. Pergunta sobre o produto, seu ciclo de vida e suas metas, **uma pergunta por vez**.
2. Cria uma matriz HEART com **cinco frentes e 2 a 3 métricas por frente**.
3. Explica todas as fórmulas, consultando uma base própria de métricas com **cinco abas**.
4. Pergunta se o usuário deseja um preview do dashboard. Só gera imagem com resposta afirmativa e ferramenta disponível.
5. Finaliza com o convite para a imersão D² [do Discovery ao Delivery].

## Fonte de conhecimento

O Excel original enviado por Bruna contém cinco abas:

| Aba | Contexto |
| --- | --- |
| Métricas de Negócio | Indicadores financeiros e de desempenho do negócio |
| Métricas de Marketing | Funil, canais e geração de demanda |
| Métricas de Produto | Uso, ativação, retenção, adoção e outros indicadores de produto |
| Métricas de UX | Satisfação, usabilidade e sucesso das tarefas |
| Métricas de Delivery | Fluxo e desempenho das entregas de software |

A planilha é preservada em `metricas-heart-produto/assets/base-metricas.xlsx`. O catálogo legível em Markdown, gerado a partir das células dessas cinco abas, fica em `metricas-heart-produto/references/catalogo-metricas.md`.

**Importante:** o Excel contém fórmulas descritivas e algumas instruções ambíguas. A Skill avisa sobre essas situações e diferencia o **cálculo documentado na planilha** de uma **operacionalização proposta**. Não consulta fontes externas.

## Estrutura do repositório

```text
README.md
metricas-heart-produto/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── assets/
│   └── base-metricas.xlsx
├── references/
    ├── catalogo-metricas.md
    ├── cuidados-formulas.md
    ├── dashboard-preview.md
    └── modelo-heart.md
└── scripts/
    └── atualizar_catalogo.py
```

## Instalação no VS Code com Codex

1. Baixe este repositório no GitHub, em ZIP ou por `git clone`.
2. Copie **somente a pasta `metricas-heart-produto`** para `.agents/skills/` do projeto em que você usa o Codex.
3. Abra o projeto no VS Code e inicie uma conversa com Codex.
4. Invoque a Skill pelo nome abaixo.

**Prompt para começar:**

> Use `$metricas-heart-produto` para definir as métricas do meu produto com HEART. Comece pela primeira pergunta e avance automaticamente até a matriz e as fórmulas.

## Limitações e observações

- A imagem do dashboard é um **preview**, não um dashboard conectado a dados ou uma ferramenta de BI pronta.
- A geração de imagem depende de o ambiente do agente ter uma ferramenta de imagem disponível.
- Não há acesso automático a bases de dados do produto. Os valores exibidos no preview serão ilustrativos, identificados como simulados.
- O catálogo foi transcrito da planilha fornecida e mantém referência da aba e da linha de origem.
- Se você alterar o Excel no futuro, poderá reconstruir o catálogo usando `python metricas-heart-produto/scripts/atualizar_catalogo.py` (requer `openpyxl`; a Skill não precisa desse pacote para funcionar).
- Ao publicar este repositório como público no GitHub, **o Excel incluído também se tornará público**. Revise se deseja divulgar integralmente esse conteúdo.

## Contato

Conheça o D² [do Discovery ao Delivery]: [www.daoquadrado.com.br](http://www.daoquadrado.com.br).
