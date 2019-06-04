# Embeds

Embeds têm uma borda colorida, são frequentemente enviados por bots e têm imagens embutidas, campos de texto e outras coisas extravagantes.

Aqui estão alguns exemplos de uso dos Embeds.

## Embed preview

Aqui está um exemplo do que um Embed pode parecer. Vamos passar por cima da construção deles na próxima parte deste guia.

![embedExemplo](https://raw.githubusercontent.com/cogumm/Discord/master/Discord.js/images/embedExemplo.png)

## Usando o constructor do RichEmbed

A classe [RichEmbed](https://discord.js.org/#/docs/main/stable/class/RichEmbed) do Discord.js facilitar a construção e manipulação das Embeds.

```js
// Realize o require do discord.js no seu arquivo
const Discord = require('discord.js');

// Pode se utilizar dentro do seu comando, ou em qualquer lugar
const embedExemplo = new Discord.RichEmbed()
	.setColor('#0099ff')
	.setTitle('Algum título aqui')
	.setURL('https://discord.js.org/')
	.setAuthor('Algum nome', 'https://IMAGEM/imagem.png', 'https://discord.js.org')
	.setDescription('Alguma descrição aqui')
	.setThumbnail('https://IMAGEM/imagem.png')
	.addField('Regular field title', 'Algum valor aqui')
	.addBlankField()
	.addField('Inline field title', 'Algum valor aqui', true)
	.addField('Inline field title', 'Algum valor aqui', true)
	.addField('Inline field title', 'Algum valor aqui', true)
	.setImage('https://IMAGEM/imagem.png')
	.setTimestamp()
	.setFooter('Algum texto de footer aqui', 'https://IMAGEM/imagem.png');

channel.send(embedExemplo);
```