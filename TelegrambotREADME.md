from aiogram import Bot, Dispatcher, executor, types 

bot = Bot(token='5562962906:AAFiAQPkfnD0TZ8vi6WGL-w0iHm5cl_3a6g')
dp = Dispatcher(bot)

@dp.message_handler(commands=['start', 'help'])
async def welcome(message: types,Message):
    await message.reply("hello I'm STAR BOT")
  
@dp.message_handler()
async def echo(message: types.Message):
  await message.answer(message.text)


executor.start_polling(dp)
