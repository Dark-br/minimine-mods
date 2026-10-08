# Introdução aos mods em Minimine

### Onde fica os mods no Minimine?

Os mods do Minimine ficam na pasta `Android/media/com.minimine/MiniMine/mods/`.Os mods são separados por pastas.

```text
mods/
|——— MeuMod/
|——— ordem.json
```

Dentro da pasta do mod,deve haver um ***info.json***. Ele vai informar ao jogo onde fica os recursos do mod (Separado por pasta).

Seguindo o formato `<recurso>:<nome da pasta>`

```json
{
  "textura":"Textura",
  "blocos":"Blocos",
  "itens":"Itens",
  "biomas":"Biomas"
}
```

## Importante!

O seu mod deve ter um indentificador para jogo diferenciar o que interno e externo.

Tipo como jogo faz:

```json
  "nome":"minimine:terra"
```

### Proximos Guias:

+ [Texturas](docs/texturas.md)
+ [Itens](docs/itens.md)