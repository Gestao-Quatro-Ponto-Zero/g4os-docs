# Revisão da documentação pública — setembro de 2026

Esta pasta guarda evidências de manutenção, fora da navegação pública do Mintlify.

## Escopo atual

A primeira revisão, no PR #118, preservou as 58 URLs originais e levou o acervo a 72 páginas. Esta ampliação parte de `2fe07c6` e acrescenta nove páginas: catálogo de IA e oito casos de uso. O resultado tem **81 MDX, 80 entradas de navegação, 20 casos de uso e 40 capturas reais**. A página de tags continua como compatibilidade com redirecionamento.

O produto foi conferido no código `ec67bc01c66cb290efe0d7f6fc6e4fa88caad664` e no Electron aberto, cuja tela informa versão 0.99.411. O repositório do aplicativo permaneceu sem alterações.

- [`coverage.json`](coverage.json): todos os 36 construtores de visualização, dez de ação, 13 subpáginas de configurações, 23 ações de teclado e 38 conexões gerenciadas relacionados aos guias. Inclui inventário das páginas e capturas.
- [`gateway-models.json`](gateway-models.json): 42 opções selecionáveis exportadas do catálogo do produto, com nome, família, entrada, raciocínio e classificação de acesso. O número inclui perfis Pro, G4 OMM e seleção de modelo gratuito; não são 42 provedores distintos.
- [`datasets.json`](datasets.json): estrutura dos cinco XLSX preservados.
- [`expansion-validation.json`](expansion-validation.json): contagens e resultados esperados dos quatro CSVs fictícios.

## Conteúdo ampliado

O assistente de workspace agora tem oito passos ilustrados, incluindo importação, perfil, objetivos, conexões e primeira experiência. IA ganhou capturas de Gateway e Codex, perfis automáticos, busca, escolha exata e ajuste de raciocínio. O catálogo lista todas as opções efetivas do produto, sem presumir catálogos externos ou fixar preços.

Conexões ganhou buscas Google/Microsoft, explicação de identidade detectada e ações disponíveis. Workflows mostra o pedido de criação e o item salvo com entradas obrigatórias. Documentos mostra leitura e edição de fonte. Dashboards mostra cinco tarefas e regras de contagem. Automações mostra agenda, prompt e opções. App, entrada e aparência receberam capturas próprias. Agentes e integrações ganharam instruções e testes de exemplo mais completos.

Os oito novos casos cobrem 1:1, resumo semanal, fornecedores, reunião com cliente, recebimentos, contas a pagar, conteúdo e treinamento. Todos incluem contexto, pedido preparado em Perguntar e critérios de revisão.

## Experiência e privacidade das capturas

Foram acrescentadas **27 capturas**, totalizando 40, todas abertas e inspecionadas individualmente. Os cenários usam Pessoa Exemplo, Empresa Exemplo, tarefas e valores fictícios. A revisão abrangeu nomes, cabeçalhos, texto, caminhos e possíveis identidades. Não há GIFs ou imagens de interface geradas por IA.

Foi criado outro workspace de demonstração, um dashboard estático e um documento editável; ambos foram abertos. O detalhe do workflow criado foi verificado. O formulário de automação foi preenchido e cancelado: não foi deixada uma rotina ativa. A revisão anterior também exercitou uma edição de célula com comparação e salvamento e abriu uma apresentação nativa no Studio.

Com autorização do usuário, descrições de rotinas de seu workspace foram consultadas para inspirar temas. Nenhum texto privado, nome de cliente, valor real ou inventário desse workspace foi copiado para o repositório. Conexões podem reconhecer autorizações prévias; as telas com identidade de conta foram excluídas das capturas públicas.

## Verificações concluídas

| Verificação | Resultado |
| --- | --- |
| `npx mint validate --strict` | Passou. |
| `npx mint broken-links --check-anchors --check-redirects` | Passou sem links quebrados. |
| `git diff --check` | Passou. |
| Navegação e compatibilidade | 80 entradas únicas, 81 MDX; nenhuma URL anterior removida. |
| Parser real dos links `g4os://` | 42 links válidos, 22 caminhos; 20 pedidos em `ask`, sem envio automático. |
| Capturas e referências | 40 imagens referenciadas e revisadas visualmente, 27 novas. |
| CSVs de exercício | Contagens, totais, correspondências, exceções e duplicidade conferidos por cálculo. |
| XLSX existentes | Cinco arquivos idênticos à base. |
| Prévia de workspace | Oito imagens carregadas e leitura em desktop conferida. |
| Prévia de IA e casos de uso | Conteúdo, tabelas e navegação conferidos; catálogo em 390 px sem transbordamento horizontal da página. |
| Privacidade dos guias | Sem caminhos pessoais, tokens ou identificadores de contas nos padrões revisados. |

## Limites

A matriz comprova cobertura editorial e evidência de implementação; não representa teste de todas as operações de todos os serviços. Não foram exercitados novos logins dos 38 conectores, envios de mensagens, captura de voz, sincronização entre computadores, pagamentos, publicação de sites pelo produto ou alterações corporativas. O deploy da documentação é uma atividade separada da funcionalidade de publicar sites no G4 OS.

A busca local do Mintlify exige autenticação e não foi exercitada. Recursos de conta, empresa e beta podem variar conforme versão e permissões. A publicação deve ser confirmada pelo deployment do commit e pela leitura do domínio público após o merge.
