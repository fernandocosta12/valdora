# Valdora: Ecos do Véu

RPG 2D de navegador (PC e celular, na horizontal). Jogue em: https://fernandocosta12.github.io/valdora/

- Tudo roda num único `index.html`, sem servidor.
- Modo online (opcional): crie `online.json` ao lado do jogo com `{"url":"https://SEU-PROJETO.supabase.co","key":"CHAVE_ANON_PUBLICA"}`. Nunca use a chave service_role.

## Conta e save na nuvem

- Conta com nome + senha (sem e-mail). Os 3 personagens ficam no navegador e no Supabase (esquema `valdora`, separado do resto do banco).
- O jogo só usa funções RPC públicas (`valdora_registrar`, `valdora_entrar`, `valdora_carregar`, `valdora_sincronizar`, `valdora_sair`, `valdora_ranking`, `valdora_feedback`); as tabelas não são acessíveis diretamente.
- Senhas guardadas com bcrypt. Ao sincronizar, cada personagem fica com a versão de maior progresso (nível, depois XP).
