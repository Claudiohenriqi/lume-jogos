# Rotina diária: achar os jogos de vôlei

Texto para criar a rotina agendada (nuvem, sem PC ligado). Frequência sugerida: **todo dia às 08:00 e às 17:00 (Brasília)**, porque horários e canais mudam de manhã e de tarde. O repositório e o `jogos.json` precisam estar acessíveis para a rotina com permissão de escrita.

## Instruções da rotina

Você mantém o arquivo `jogos.json` deste repositório, lido por um app de TV pessoal. Faça isto:

1. Descubra a data de hoje em Brasília (UTC−3).
2. Pesquise na web os jogos de vôlei de **hoje e de amanhã** em que joga pelo menos um destes clubes, em qualquer competição (ligas nacionais, copas e torneios continentais como a CEV Champions League): Gerdau Minas, Osasco, Praia Clube, Sesc Flamengo, Sada Cruzeiro, Sesi Bauru, Prosecco Conegliano (Imoco), Vero Volley Milano, Scandicci, Novara, Perugia, Trentino, Lube Civitanova, VakıfBank, Fenerbahçe, Eczacıbaşı, Suntory Sunbirds, Osaka Bluteon, Denso Airybees.
3. Para cada jogo, confirme em **fonte confiável** (site da liga, do clube, da emissora, ge.globo, Volleyball World): horário de início e **canal de transmissão no Brasil**. Converta o horário para Brasília (`-03:00`). **Não invente**: se o horário ou o canal não estiver confirmado, deixe o jogo de fora.
4. Escreva `jogos.json` no formato do `README.md`. `updatedAt` = agora, em Brasília. Cada jogo: `league`, `home`, `away`, `start` (ISO 8601 com `-03:00`), `channel` ("SporTV 2", "TV Brasil", "Rai Sport", "YouTube Canal Vôlei Brasil"…) e `platform` (`youtube` se passar no YouTube, senão `tv`).
5. Valide: o arquivo é JSON válido, todo `start` é uma data completa com fuso, não há jogo repetido. Sem jogos confirmados, grave `"games": []`.
6. Faça commit com a mensagem `jogos: <data e hora>` e envie (push) para o ramo `main`. Grave sempre, mesmo sem mudança nos jogos, para o `updatedAt` ficar atual (o app ignora arquivo com mais de 36 h).

Regras: edite só `jogos.json`. Nunca coloque chaves, senhas ou dados pessoais no repositório.
