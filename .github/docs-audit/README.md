# Revisão da documentação pública — setembro de 2026

Evidências de manutenção, fora da navegação pública do Mintlify.

## Escopo atual

O acervo tem **81 páginas MDX, 80 entradas de navegação, 20 casos de uso, 66 capturas reais e 20 exemplos visuais originais**. As 58 URLs originais foram preservadas; a página de tags continua como compatibilidade com redirecionamento.

A revisão do produto usa o código `ec67bc01c66cb290efe0d7f6fc6e4fa88caad664` e o Electron aberto, versão 0.99.411. A expansão visual parte do commit de documentação `a7f2752920342ff5833f2c2e33ad1e7f499585d4`. O repositório do aplicativo permaneceu sem alterações.

- [`coverage.json`](coverage.json): 36 construtores de visualização, dez de ação, 13 rotas de configurações, 23 ações de teclado e 38 conexões gerenciadas relacionados aos guias; inclui inventário de páginas, capturas e ilustrações.
- [`gateway-models.json`](gateway-models.json): 42 opções selecionáveis do catálogo do produto. Inclui perfis Pro, G4 OMM e seleção de modelo gratuito; não são 42 provedores distintos.
- [`datasets.json`](datasets.json): estrutura dos cinco XLSX preservados.
- [`expansion-validation.json`](expansion-validation.json): contagens e resultados esperados dos quatro CSVs fictícios.
- [`visual-expansion.json`](visual-expansion.json): 26 novas capturas com regiões ocultadas e hashes das cópias públicas; 20 ilustrações e respectivas páginas.

## Empresa e Configurações

Foram adicionadas 14 capturas de Empresa: visão geral; consumo por dia e usuário; política global; regras por modelo; auditoria; uso extra, formulário e validade; pessoas e formulário de inclusão; documentos, estrutura e solicitações de contexto.

As 12 novas capturas de configurações cobrem IA, uso, resumo do mês, cupom, workspace, permissões, tags, Cloud Sync, preferências, suporte, atalhos e a entrada do Brain. Elas complementam as imagens existentes de App, Entrada e Aparência. Todas as 13 rotas registradas de configurações têm um guia com captura, incluindo rotas de compatibilidade.

A inspeção usou a conta administrativa conectada com autorização explícita. Foram abertas telas, filtros e formulários vazios; os formulários foram cancelados. Nenhuma pessoa foi adicionada, nenhum crédito foi concedido, nenhum cupom foi resgatado e nenhuma política, domínio, modelo, memória ou sincronização foi alterado.

## Casos de uso

Todos os 20 casos incluem um exemplo visual visível e abas **Materiais**, **Pedido** e **Resultado**. O pedido tem botão de copiar, quebra de linha responsiva e link que preenche uma sessão em Perguntar, sem envio automático.

Os visuais são SVGs originais: tabelas, gráficos, pautas e quadros de entrega. Não reproduzem a interface do app nem usam capturas de outros produtos. Contas a pagar e recebimentos seguem os CSVs do exercício; a comparação de fornecedores segue os valores escritos no guia. Nos quatro exemplos de análise comercial, os números são ilustrativos e independentes dos XLSX, condição explícita no visual e na legenda.

As referências fornecidas pelo usuário orientaram a organização por materiais, pedido e resultado. Nenhum prompt extenso, ativo visual ou componente proprietário das referências foi copiado.

## Privacidade das imagens

As 40 capturas anteriores usam workspaces e conteúdo de demonstração. As 26 novas incluem telas reais de uma conta autorizada; por isso, não devem ser descritas coletivamente como dados fictícios. E-mails, nomes identificáveis, notas, títulos e caminhos internos foram cobertos com **tarjas sólidas por código**, método escolhido pelo usuário.

As cópias originais ficaram fora do repositório. Somente PNGs RGB processados e sem metadados textuais/EXIF entram na publicação. As regiões ocultadas foram conferidas visualmente, inclusive faixas parciais entre diálogos e o fundo. Saldos e regras visíveis são acompanhados da ressalva de que refletem a conta fotografada, sem representar plano ou padrão recomendado.

Os 20 SVGs foram abertos em galeria para revisão de composição, legibilidade, valores e legendas. Uma sobreposição no rótulo de encerramento do fluxo foi corrigida antes da publicação.

## Verificações

| Verificação | Resultado |
| --- | --- |
| Mintlify `validate --strict` | Passou. |
| Mintlify `broken-links --check-anchors --check-redirects` | Passou sem links quebrados. |
| `git diff --check` | Passou. |
| Parser real dos links `g4os://` | 42 links válidos, 22 caminhos, 20 pedidos em `ask`, sem envio automático. |
| Cobertura visual | 66 capturas referenciadas; 20 de 20 casos com SVG, abas e pedido copiável. |
| Dados | Cinco XLSX e quatro CSVs preservados; valores financeiros dos visuais conferidos. |
| Prévia de Empresa | 11 imagens carregadas no guia, incluindo abas de pessoas, agrupamento e validade. |
| Prévia de casos de uso | Abas de materiais, pedido e resultado funcionais; imagem ampliável. |
| Responsividade | Empresa e caso de e-mail em 390 px sem transbordamento da página; pedido com quebra de linha sem rolagem horizontal. |
| Privacidade | Regiões ocultadas revisadas e PNGs sem metadados textuais/EXIF. |

## Limites

A matriz comprova cobertura editorial e evidência de implementação; não representa teste de todas as operações de todos os serviços. Não foram exercitados novos logins dos 38 conectores, envios de mensagens, captura de voz, sincronização entre computadores, pagamentos, publicação de sites pelo produto ou mutações corporativas. A publicação desta documentação é uma atividade separada do recurso de publicar sites no G4 OS.

A busca local do Mintlify exige autenticação e não foi exercitada. Recursos de conta, empresa e beta variam conforme versão e permissões. A publicação é confirmada pelo deployment do commit e pela leitura do domínio público após o merge.
