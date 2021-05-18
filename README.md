# EmreCraft
const Discord = require('discord.js')
const db = require('quick.db');

exports.run = async (client, message, args) => {
  let tagk = args.slice(0).join(' ');
    if (!tagk) {
        return message.reply(':x: Lütfen bir tag belirleyiniz.')
    }
    var s = db.set(`tagver_${message.guild.id}`, gM)
    const embed = new Discord.RichEmbed()
    .setDescription(":white_check_mark: Başarıyla tag **" + s + "** olarak ayarlandı!")
    .setColor("RANDOM")
    message.channel.send({embed})
}

exports.conf = {
    enabled: true,
    guildOnly: false,
    aliases: ['oto-tag-ayarla'],
    permLevel: 3
  };

  exports.help = {
    name: 'tag-ayarla',
    description: 'Sunucuya katılan üyeye otomatik tag verir',
    usage: 'tag-ayarla <tag>'
  };
