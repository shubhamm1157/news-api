# news-api
import requests

api="6f36a56c984a456cbde6df6e3719e05e"
query=input("what type of news are you interested now ?")
url=f"https://newsapi.org/v2/everything?q={query}&from=2025-04-14&sortBy=publishedAt&apiKey={api}"
print(url)
r=requests.get(url)

data= r.json()
articles=data["articles"]

for article in articles:
    print(article["title"])
    print(article["url"])
    print("\n***********************************\n")

