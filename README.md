# lume-jogos

Arquivo público `jogos.json` com os jogos de vôlei dos clubes que o app Lume acompanha. Uma rotina agendada o atualiza todo dia e o app da TV o lê (ver `ROTINA.md`). Não há dado pessoal aqui, só calendário público.

## Formato de `jogos.json`

```json
{
  "updatedAt": "2026-11-10T09:00:00-03:00",
  "games": [
    {
      "league": "Superliga Feminina",
      "home": "Osasco",
      "away": "Gerdau Minas",
      "start": "2026-11-10T21:00:00-03:00",
      "channel": "SporTV 2",
      "platform": "tv"
    }
  ]
}
```

- `updatedAt`: quando a rotina rodou (ISO 8601 com fuso). O app ignora o arquivo se ele tiver mais de 36 horas.
- `games`: jogos de hoje e de amanhã (horário de Brasília). Lista vazia = não há jogos.
- `start`: início em ISO 8601 com fuso (Brasília, `-03:00`).
- `channel`: onde passa no Brasil ("SporTV 2", "TV Brasil", "YouTube Canal Vôlei Brasil"…).
- `platform`: `tv` ou `youtube`.

Só entram jogos em que joga pelo menos um destes clubes: Gerdau Minas, Osasco, Praia Clube, Sesc Flamengo, Sada Cruzeiro, Sesi Bauru, Prosecco Conegliano, Vero Volley Milano, Scandicci, Novara, Perugia, Trentino, Lube Civitanova, VakıfBank, Fenerbahçe, Eczacıbaşı, Suntory Sunbirds, Osaka Bluteon, Denso Airybees.
