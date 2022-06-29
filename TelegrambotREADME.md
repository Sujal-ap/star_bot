
import requests

base_url = "https://api.telegram.org/bot5433576994:AAFGJ3b0cpi99caRD0JxSTpizERLE-bjMS0/sendmessage"

parameters = {
  "chat_id" : "-1001557666214",
   "text" : "hello"
}

resp = requests.get(base_url, data = parameters)

print(resp.text)
