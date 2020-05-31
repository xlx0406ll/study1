# study1
import requests
def getHTMLText(url):
    try:
        r = requests.get(url, timeout=30)
        r.raise_for_status()
        r.encoding = r.apparent_encoding
        return r.text
    except:
        return"产生异常"
if __name__=="__main__":
    url = "http://www.qq.com/robots.txt"
    print(getHTMLText(url))
