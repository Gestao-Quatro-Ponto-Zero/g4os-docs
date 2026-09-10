# Revisão da documentação pública — setembro de 2026

Esta pasta registra evidências para manutenção e revisão do PR. Não faz parte da navegação pública do Mintlify.

## Escopo e base

A revisão partiu dos 58 arquivos MDX existentes, preservou suas URLs e acrescentou 14 guias. São 72 arquivos: 71 entradas de navegação e uma página de compatibilidade de tags, cujo redirecionamento foi mantido. O conteúdo foi organizado em português para usuários não técnicos.

O comportamento foi confrontado com o Electron aberto e o código do produto no commit `ec67bc01c66cb290efe0d7f6fc6e4fa88caad664`. Nenhum arquivo do repositório do aplicativo foi alterado. A base dos docs é `33c8636`.

[`coverage.json`](coverage.json) relaciona cada construtor de rota, área de configurações, atalho e conexão gerenciada às páginas correspondentes. Inclui a referência de implementação, a forma de verificação e as limitações. O inventário de rotas contém todos os 36 construtores de visualização e 10 construtores de ação de `routes.ts`; os parâmetros finitos estão em `routeVariants`, e as 13 subpáginas de configurações estão enumeradas separadamente. IDs de sessões, projetos e itens são variáveis, não novas páginas de documentação.

## Correções relevantes

- Entrada incorporada a App, Tags como nome apresentado ao usuário, Marketplace/Meus Itens na rota atual e aliases de Empresa tratados como compatibilidade.
- Artigo antigo de Modo reparo preservado como resolução de problemas, sem indicar uma tela geral que não existe na navegação atual.
- Menções `@`, `#`, `>` e menu `/`, 23 ações de teclado registradas, atalho do Desk e comandos atuais do Telegram.
- Distinção entre conexão de IA, conexão de trabalho, agente gerenciado e agente personalizado; catálogo completo com 38 conexões.
- Guias novos de entregáveis, planilhas nativas, slides, sites, Apps, Desk, navegador, parceiros e mapa da interface.
- Distinção entre prévia, edição nativa e exportação; entre publicar uma conversa, colaborar e controlar uma sessão remotamente; entre Brain e Cloud Sync.
- Remoção de preços fixos, ciclos universais de crédito e promessas amplas de criptografia que não descreviam corretamente todos os caminhos do produto.
- Cinco casos cotidianos novos: reuniões, e-mails, acompanhamento, documentos e pesquisa. Os sete casos existentes foram revistos. Todos os 12 pedidos de exemplo são preparados para revisão, sem envio automático.
- Três botões de download da página independente `landing.html` agora apontam para a página oficial. Essa página de marketing não compõe o inventário de guias.

## Capturas e experiência no aplicativo

Foram criados um workspace fictício, sessões de exemplo, um projeto com marco e um agente personalizado. A planilha nativa foi aberta, uma célula foi alterada, a diferença foi revisada e a alteração foi aplicada com confirmação de estado salvo. A apresentação nativa foi gerada e aberta no G4 Slide Studio. Os controles de exportação foram inspecionados, sem afirmar que os arquivos exportados foram testados.

As 13 capturas novas foram inspecionadas individualmente, incluindo nomes, cabeçalhos, caminhos e texto visível. Contêm somente cenários fictícios e controles do produto. As 30 imagens antigas, que deixaram de ser referenciadas, foram removidas; não foram produzidos GIFs.

## Arquivos de exercício

Os cinco XLSX foram preservados byte a byte. [`datasets.json`](datasets.json) registra abas, cabeçalhos e dimensões relevantes, sem copiar registros completos.

Os exercícios comerciais contêm divergências entre subtítulos, períodos nas células e descrições antigas. Os novos guias orientam a conferir o período real, separar totais e evitar dupla contagem. Não se presume taxa de churn sem denominador, retenção de pessoas a partir de receita nem curva de ramp sem data de entrada. A referência APQC é identificada como versão 8.0, sem tratá-la como a versão mais recente.

## Verificação concluída

| Verificação | Resultado |
| --- | --- |
| `npx mint validate --strict` | Passou. |
| `npx mint broken-links --check-anchors --check-redirects` | Passou, sem links quebrados. |
| `git diff --check` | Passou. |
| Comparação dos construtores de `routes.ts` com a matriz | 36 de visualização e 10 de ação cobertos; nenhuma entrada ausente. |
| Configurações e catálogo exportado do produto | 13 subpáginas e 38 conexões cobertas. |
| Links `g4os://` pelo parser real do aplicativo | 34 links válidos em 22 caminhos; 12 pedidos em modo `ask`, sem `send=true`. |
| Navegação e arquivos | 71 entradas únicas e uma compatibilidade; nenhuma página antiga removida. |
| Capturas | 13 arquivos referenciados e revisados visualmente. |
| Dados de exercício | Cinco arquivos idênticos à base. |
| Prévia visual | Página inicial, planilhas com ampliação de imagem, catálogo, navegação por links, tema escuro e menu em largura de 390 px. Sem transbordamento horizontal da página; tabelas em região rolável. |
| Busca por caminhos pessoais e links antigos inválidos nos guias | Nenhuma ocorrência dos padrões revisados. |

## Limites da verificação

A matriz documenta cobertura editorial e evidência de implementação; não equivale a teste de todas as operações de todos os serviços. Autenticação das 38 integrações, envio de mensagens, voz, sincronização entre computadores, publicação, pagamentos e alterações corporativas não foram executados. As instruções desses recursos foram conferidas em componentes, contratos e referências atuais do produto.

A busca da prévia Mintlify exige autenticação e não foi exercitada. Recursos corporativos ou beta podem variar com permissões, conta e versão. As páginas explicam essas condições nos pontos relevantes.
