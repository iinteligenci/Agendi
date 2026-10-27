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


## Área profissional de gestão

Acesse a página administrativa em: https://iinteligenci.github.io/Agendi/admin.html

### Configuração inicial obrigatória
1. No Supabase do projeto conectado ao Agendi, abra **SQL Editor**.
2. Abra o arquivo `supabase/migrations/202610270001_management.sql` deste repositório, copie todo o conteúdo e execute no SQL Editor.
3. No Supabase, entre em **Authentication → Users** e crie o usuário com o e-mail e senha que serão usados na área administrativa. Não coloque senhas no código.
4. Abra a página `admin.html` e entre com esse usuário.

### O que já está incluído na área profissional
- Agenda por dia, filtro por status e ações para confirmar, concluir, marcar falta ou cancelar.
- Cadastro e busca de clientes, com telefone, aniversário, e-mail e observações.
- Lançamento de receitas e despesas, totais mensais e exportação CSV.
- Ficha de anamnese com campo de consentimento.
- Relatório resumido do mês.

**Importante:** a página pública de agendamento continua separada. As fichas de anamnese podem conter dados pessoais sensíveis; mantenha o acesso ao usuário autorizado. O dashboard depende da execução da migração SQL no Supabase. Os lançamentos financeiros são manuais e não representam lucro contábil automaticamente. Mensagens automáticas de WhatsApp, controle de comissões, lembretes automáticos, metas e multas ainda precisam de integrações e módulos adicionais.
