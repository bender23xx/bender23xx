- 👋 Hi, I’m @bender23xx
const { MessageEmbed } = require("discord.js")
const { invite, color } = require('../../../config.json')

module.exports.run = async (client, message, args) => {

  const poop = new MessageEmbed()

  .setColor(color)
 .addFields(
  { name: ' Boost', value: `Level ${message.guild.premiumTier >= 1 ? `${message.guild.premiumTier}` : `${message.guild.premiumTier.replace(/tier_/gi, "")}`}\n${message.guild.premiumSubscriptionCount >= 1 ? `${message.guild.premiumSubscriptionCount}` : `0`} Boosts`, inline: true },)

  message.channel.send({ embeds: [poop] })
}

module.exports.config = {
  name: "boost",
  aliases: [],
  description: 'shows bot invite',
  parameters: '',
  permissions: '',
  syntax: 'boost',
  example: 'boost'
}
