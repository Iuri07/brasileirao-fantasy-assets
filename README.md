# Brasileirão Fantasy — Assets

Repositório só com assets visuais (imagens) do
[brasileirao-fantasy](https://github.com/Ian-costermani/brasileirao-fantasy).

Existe separado pra ser servido via jsDelivr CDN sem expor o código
da aplicação. **Não contém nenhum código.**

## Estrutura

- `atletas/` — cutouts PNG transparentes (foto do jogador sem fundo),
  nomeados por `atleta_id` da Cartola
- `escudos/` — escudos JPG dos clubes do brasileirão
- `players/` — fotos JPG de jogadores (busto/legados)
- `times_escudos/` — logos PNG dos times fantasy da liga

## Uso

Via jsDelivr:
```
https://cdn.jsdelivr.net/gh/Ian-costermani/brasileirao-fantasy-assets@master/atletas/{id}.png
https://cdn.jsdelivr.net/gh/Ian-costermani/brasileirao-fantasy-assets@master/escudos/flamengo.jpg
```

Cache: jsDelivr cacheia agressivamente. Pra forçar refresh use `@vN`
ou `?v=N` na URL.

## Regenerar cutouts

A geração dos PNGs em `atletas/` fica no código principal
(`scripts/baixar-cutouts-faltantes.ts` + rembg local). Quando rodar,
copie os novos PNGs pra cá manualmente:

```bash
cp ~/dev/brasileirao-fantasy/static/atletas/*.png \
   ~/dev/brasileirao-fantasy-assets/atletas/
```
