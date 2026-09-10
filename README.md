# G4 OS Docs

Documentação pública em português para pessoas que usam o G4 OS no trabalho. Os guias explicam como pedir, revisar, organizar e compartilhar entregas sem exigir conhecimento de programação.

O acervo atual tem 81 páginas, 20 casos de uso, 66 capturas reais e 20 exemplos visuais originais. Os catálogos cobrem 38 conexões de trabalho e 42 opções selecionáveis do AI Gateway, conforme a revisão de setembro de 2026.

## Prévia e validação

```bash
npx mint dev --port 3334 --no-open
npx mint validate --strict
npx mint broken-links --check-anchors --check-redirects
```

A busca da prévia local pode exigir autenticação do Mintlify. Isso não impede a revisão das páginas e da navegação. Não coloque credenciais no repositório para habilitá-la.

## Estrutura

- `docs.json`: navegação, idioma, marca e redirecionamentos.
- `getting-started/`: primeira tarefa, criação do workspace e mapa da interface.
- `product/`: conceitos, conexões e entregáveis.
- `support/`: instruções por recurso e ajuda para problemas comuns.
- `use-cases/`: exemplos de trabalho com pedidos que podem ser preparados no app.
- `images/guide/`: capturas reais de demonstração e de administração, com identificações ocultadas nas telas de contas autorizadas.
- `images/use-cases/`: exemplos visuais originais, identificados como ilustrativos ou calculados dos CSVs de exercício.
- `use-cases/datasets/`: arquivos de exercício; confira as ressalvas nos respectivos casos de uso.
- `.github/docs-audit/`: evidências e limites da revisão editorial, fora da navegação pública.

`landing.html` é uma página independente, fora da navegação Mintlify; seus botões encaminham para a página oficial de download.

## Atualizar um guia

1. Confira o comportamento na versão atual do aplicativo e no contrato do recurso. Registre a referência em `.github/docs-audit/coverage.json`.
2. Escreva pelo objetivo da pessoa: onde abrir, o que fazer, como conferir o resultado e como resolver os erros comuns. Detalhes de infraestrutura pertencem à documentação técnica do produto.
3. Preserve URLs existentes. Quando precisar mover uma página, configure o redirecionamento e atualize os links internos.
4. Prefira capturas do workspace de demonstração. Para contas reais, obtenha autorização e cubra identificações e conteúdo privado com tarjas sólidas antes de salvar a cópia pública. Revise a imagem inteira, inclusive bordas, fundo de diálogos e metadados. Não publique mensagens privadas, tokens, códigos de conexão, caminhos pessoais ou dados identificáveis de clientes. Inclua texto alternativo e explique quando valores refletem uma conta específica.
5. Todo caso de uso deve ter apoio visual: captura real ou exemplo de entrega claramente identificado. Preserve pedidos copiáveis e critérios de revisão; não apresente ilustrações como resultados reais de arquivos ou contas.
6. Confira todas as integrações e opções de IA do catálogo vigente. Não transforme exemplos de uso em promessas de ações que a conexão não suporta.
7. Execute os dois comandos de validação e revise a prévia, incluindo páginas com imagens, tabelas e pedidos de exemplo.

Os links de casos de uso preenchem um pedido em modo Perguntar. Não use `send=true`: a pessoa deve poder revisar referências e texto antes de enviar.

## Marca

Os ativos de marca seguem os exports do repositório principal:

- `favicon.svg`: `apps/viewer/public/favicon.svg`.
- `logo/light.png` e `logo/dark.png`: `apps/electron/resources/g4os-logos/`.
