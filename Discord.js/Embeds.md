# Embeds

Embeds têm uma borda colorida, são frequentemente enviados por bots e têm imagens embutidas, campos de texto e outras coisas extravagantes.

Aqui estão alguns exemplos de uso dos Embeds.

## Embed preview

Aqui está um exemplo do que um Embed pode parecer. Vamos passar por cima da construção deles na próxima parte deste guia.

<div is="discord-messages">
	<discord-message author="cGmBot Tutorial" avatar="blue" :bot="true">
		<discord-embed
			slot="embeds"
			color="#0099ff"
			title="Algum título aqui"
			url="https://discord.js.org/"
			thumbnail="https://github.com/cogumm/cogumm.net/blob/master/2014/images/work/cgm_labs.png"
			image="https://github.com/cogumm/cogumm.net/blob/master/2014/images/work/cgm_labs.png"
			footer-image="https://github.com/cogumm/cogumm.net/blob/master/2014/images/work/cgm_labs.png"
			timestamp="01/01/2019"
			authorName="Algum nome"
			authorImage="https://github.com/cogumm/cogumm.net/blob/master/2014/images/work/cgm_labs.png"
			authorUrl="https://discord.js.org/"
		>
			Alguma descrição aqui
			<embed-fields>
				<embed-field title="Título do campo">
					Algum valor aqui
				</embed-field>
				<embed-field title="​">
					​
				</embed-field>
				<embed-field :inline="true" title="Inline field title">
					Algum valor aqui
				</embed-field>
				<embed-field :inline="true" title="Inline field title">
					Algum valor aqui
				</embed-field>
				<embed-field :inline="true" title="Inline field title">
					Algum valor aqui
				</embed-field>
			</embed-fields>
			<span slot="footer">Algum texto de footer aqui</span>
		</discord-embed>
	</discord-message>
</div>

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
	.setAuthor('Algum nome', 'https://github.com/cogumm/cogumm.net/blob/master/2014/images/work/cgm_labs.png', 'https://discord.js.org')
	.setDescription('Alguma descrição aqui')
	.setThumbnail('https://github.com/cogumm/cogumm.net/blob/master/2014/images/work/cgm_labs.png')
	.addField('Regular field title', 'Algum valor aqui')
	.addBlankField()
	.addField('Inline field title', 'Algum valor aqui', true)
	.addField('Inline field title', 'Algum valor aqui', true)
	.addField('Inline field title', 'Algum valor aqui', true)
	.setImage('https://github.com/cogumm/cogumm.net/blob/master/2014/images/work/cgm_labs.png')
	.setTimestamp()
	.setFooter('Algum texto de footer aqui', 'https://github.com/cogumm/cogumm.net/blob/master/2014/images/work/cgm_labs.png');

channel.send(embedExemplo);
```