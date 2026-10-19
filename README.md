# Agendi — Beautycare
Protótipo web de agendamento para depilação, massagem relaxante e drenagem linfática.

## Recursos
- Catálogo inicial de nove procedimentos com preços editáveis.
- Cálculo automático do sinal de 50% e do saldo.
- Data e horário desejados.
- Mensagem pronta para WhatsApp com o resumo do pedido.
- Área administrativa local para atualizar preços, horários e número de WhatsApp.
- Deploy estático no GitHub Pages via GitHub Actions.

## Como publicar
O GitHub Pages está configurado para publicar diretamente a branch `main`, pasta `/(root)`. Em Settings → Pages → Build and deployment, mantenha a fonte como `Deploy from a branch`, branch `main` e pasta `/(root)`.

## Importante
Este é um protótipo inicial. As configurações administrativas são salvas apenas no navegador utilizado; não existe banco de dados compartilhado, sincronização entre dispositivos, autenticação administrativa ou bloqueio real de horários. O formulário solicita uma data e hora desejadas, e a disponibilidade deve ser confirmada pelo estabelecimento. O WhatsApp abre com a mensagem preenchida, sem envio automático. Configure o número real do WhatsApp na Área administrativa antes de testar o fluxo.
