# Valdora: Ecos do Véu

RPG 2D de navegador (PC e celular, na horizontal). Jogue em: https://fernandocosta12.github.io/valdora/

- Tudo roda num único `index.html`, sem servidor.
- Modo online (opcional): crie `online.json` ao lado do jogo com `{"url":"https://SEU-PROJETO.supabase.co","key":"CHAVE_ANON_PUBLICA"}`. Nunca use a chave service_role.

## Conta e save na nuvem

- Conta com nome + senha (sem e-mail). Os 3 personagens ficam no navegador e no Supabase (esquema `valdora`, separado do resto do banco).
- O jogo só usa funções RPC públicas (`valdora_registrar`, `valdora_entrar`, `valdora_carregar`, `valdora_sincronizar`, `valdora_sair`, `valdora_ranking`, `valdora_feedback`); as tabelas não são acessíveis diretamente.
- Senhas guardadas com bcrypt. Ao sincronizar, cada personagem fica com a versão de maior progresso (nível, depois XP).

## Ranking e relatos

- Ranking dos 50 personagens de maior nível (só os salvos em conta): botão "Ranking" na ajuda.
- Relatos de bugs e ideias: botão "Relatar bug ou ideia" na ajuda. Ficam na tabela `valdora.feedback` do Supabase (Table Editor → esquema `valdora`).

## Créditos de arte (CC0)
- KayKit (Kay Lousberg): Adventurers, Skeletons, Dungeon, Dungeon Remastered, Forest Nature, Medieval Hexagon, Resource Bits, Halloween Bits
- Kenney: Particle Pack, Tower Defense Kit, Monster Builder
- Quaternius: Ultimate Platformer Pack, Ultimate Monsters, Ultimate Stylized Nature, Monster Pack, Low Poly Medieval Weapons
- Cenji: Low Poly Nature Forest Mega Pack
