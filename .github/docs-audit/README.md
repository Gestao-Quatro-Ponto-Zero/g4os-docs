# Revisão da documentação pública — outubro de 2026

Evidências de manutenção, fora da navegação pública do Mintlify. O conteúdo publicado continua voltado ao uso do produto.

## Referência e escopo

Revisão em **12/10/2026**, no **main público `e642a043079215c886d3702e8163cd1b62c4a8e9`, versão 0.99.431**. O app foi construído e aberto em um checkout isolado com workspace e conteúdo fictícios. O checkout de desenvolvimento da pessoa não foi alterado. **Galts não faz parte deste escopo.**

O acervo tem **82 páginas MDX, 81 entradas de navegação, 20 casos de uso, 82 imagens de interface e 20 ilustrações originais**. URLs existentes e exemplos de exercício foram preservados. A nova página é `support/documents`.

Foram revisados Documentos e sites, OS Docs, edição visual e Melhorar, referências com `$`, páginas de reunião, transcrição, compartilhamento de cópia de leitura, nomes de Configurações, atalhos, formulários de automação, Marketplace, Desk, contexto de projetos e Empresa e catálogos de IA. Quatro casos de uso receberam instruções para continuar nos novos fluxos.

## Evidências

- [`coverage.json`](coverage.json): 37 construtores de visualização, dez de ação, 13 rotas de configurações, 25 ações de teclado e 38 conexões relacionados aos guias. Inventário de páginas e imagens com hashes, origem e data da evidência.
- [`october-validation.json`](october-validation.json): 71 aberturas de rotas no app isolado, validação dos 43 links `g4os://`, revisão da prévia e limites dos testes.
- [`gateway-models.json`](gateway-models.json): 50 opções selecionáveis exportadas do catálogo público. Inclui perfis Pro, G4 OMM e roteador gratuito; não representa 50 provedores. O catálogo Codex Subscription tem oito opções nesta versão.
- [`datasets.json`](datasets.json), [`expansion-validation.json`](expansion-validation.json) e [`visual-expansion.json`](visual-expansion.json): evidência histórica de setembro para arquivos de exercício, valores dos exemplos e expansão visual anterior. As datas desses arquivos foram preservadas.

A matriz diferencia navegação local e barreiras de acesso. Empresa, Plano e uso e Marketplace exigem acesso ao serviço; abrir a rota não comprova uma operação autenticada. A rota Pessoas de projeto pessoal retorna à área de sessões, conforme a interface.

## Imagens e privacidade

**25 capturas renovadas e 16 adicionadas.** As telas de documentos, reuniões, configurações, conexões, automações e seletores foram fotografadas no Electron de demonstração. O conteúdo da conversa e da transcrição foi preparado como exemplo fictício; não é resposta de uma nova chamada de IA ou gravação de pessoas.

Desk e Marketplace usam os **componentes de produção com fixtures oficiais do produto**. As legendas identificam a simulação. Não houve chamada de voz, acesso ao catálogo de uma conta, instalação nem publicação no serviço.

As capturas administrativas de setembro continuam com as identificações ocultadas. Valores exibidos pertencem à conta autorizada fotografada e não representam um plano padrão. Não foi aberta uma conta real para renovar essas telas nesta revisão.

Foram removidos metadados de 24 imagens anteriores sem alterar os pixels codificados. As novas imagens e as cópias preservadas foram inspecionadas quanto a EXIF e metadados textuais. Hashes atuais ficam em `coverage.json`; hashes históricos em `visual-expansion.json` descrevem aquela revisão anterior.

## Verificações

- Mintlify `validate --strict` e `broken-links --check-anchors --check-redirects`.
- `git diff --check`.
- Parser compartilhado real: 43 links válidos, sem `send=true`; os 20 pedidos dos casos de uso mantêm `mode=ask`.
- 71 rotas abertas no app isolado, sem exceções de página; inclui estados vazios, detalhes, aliases e barreiras de acesso.
- Todas as 82 páginas abertas na prévia desktop, sem erros de página ou imagens indisponíveis; páginas principais também verificadas sem transbordamento em 390 px.
- Revisão visual das imagens novas e renovadas, legendas e texto alternativo; limpeza de metadados das imagens anteriores.

## Limites

Não foram exercitados novos logins dos 38 conectores, envios de mensagens, captura de voz, transcrição remota, análise paga, sincronização entre computadores, pagamentos, publicação de sites pelo produto nem mutações corporativas. Editor e biblioteca foram usados localmente. Publicar a documentação é uma operação separada de publicar materiais pelo G4 OS.

A busca local Mintlify exige autenticação e não foi exercitada. Disponibilidade de conta, empresa e recursos beta varia conforme versão e permissões. Evidência de interface e de implementação não equivale a teste completo dos serviços externos.
