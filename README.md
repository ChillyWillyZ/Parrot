import telebot
from telebot import types
token = "5685064691:AAGHTtwOXOvyMWKrU9ximd9eBQEar4y1950"
bot = telebot.TeleBot(token)

@bot.message_handler(content_types=['text'])
def start(message):
    bot.send_message(message.chat.id, message.text)

bot.polling(non_stop=True)
