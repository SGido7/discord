import discord
from discord.ext import commands

bot = commands.Bot(command_prefix='/')

@bot.event
async def on_ready():
        print(from'Bot is connected as {bot.user}')

@bot.command()
async def kickvc(ctx, member: discord.Member):
     if ctx.author.voice:
            await member.move_to(None)
            await ctx.send(f'{member.name} is disconnected')
    else:
        await ctx.send('wait bro!!the user is not here...')

bot run('MTE5NzIzMTYzNjg0NTE4MzEwNg.GNvAJ0.RU9rThK_G6ic6uJy0I-mSLAUJuQtTTWSUc8Ht0')
