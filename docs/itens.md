# Itens em Minimine

Os itens são aqueles objetos que ficam em seu inventário e tem uma função tipo uma espada.

### Como adiocionar um item ao jogo?

É bem simples! Cada item é um arquivo **json** separado.

Primeiro passo: Defina a pastas dos itens no `info.json`. Crie a pasta dos itens com nome que você colocou.

Segundo passo: Dentro da pasta,por exemplo,"Itens" você criar um arquivo **json** com nome do item

`Itens/itemexemplo.json`

| Nome | Função |
|---|---|
| nome | Define o nome do item para jogo. |
| textura | Diz qual textura será usada pelo nome definido no `base.json` para o jogo. |
| receita | Define o craft do item no jogo e quantidade que é obtida,se não defindo,ele não pode ser craftado. |

Exemplo:

```json
{
  "nome":"meumod:itemexemplo",
  "textura":"textura_item_exemplo",

  "receita": {
    "grade":[
      null,"minimine:terra",null,
      null,null,"minimine:tabua_madeira",
      null,null,null
    ],

    "quantidade":1
  }
}
```

### Propriedades de um item

As propriedades são completamente opcionais.

```json
  "propriedades":{
    ... Propriedades aqui!
  }
```

| Nome | Função |
|---|---|
| pilhaMax | Define a quantidade máxima que  o item pode ser agrupado. |
| categoria | Define a categoria do item. |
| categoriaFerramenta | Define qual categoria de ferramenta,ele pertence (`espada,picareta,machado`). |
| nivel | Define que blocos do mesmo nivel ou inferior podem ser quebrados. |
| mineracao | Define quanto de "dureza" a ferramenta tira por segundo|
| dano | Define quanto de dano o item tira de uma entidade por golpe |

### Um item pode ser um projetil?

Sim! é bem simples de fazer:

```json
	"projetil": {
		"dano": 2,
		"itemAoBater": "minimine:coco_aberto",
		"velocidade": 16.0
	}
```

| Nome | Função |
|---|---|
| dano | Define o dano ao colider com uma entidade |
| itemAoBater | Define se ele vai virar outro item ao bater em algum bloco ou entidade |
| velocidade | Define o impulso ao ser jogado