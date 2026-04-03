# 新闻API参考

## RSS订阅源

### 主要金融新闻RSS

| 来源 | URL | 覆盖范围 |
|--------|-----|----------|
| 彭博社 | https://bbg.buzzing.cc/feed.json | 全球新闻 |
| 彭博社 | https://feeds.bloomberg.com/markets/news.rss | 市场 |
| CNBC | https://www.cnbc.com/id/100003114/device/rss/rss.html | 商业 |
| 金融时报 | https://www.ft.com/rss/home | 全球金融 |
| 华尔街日报市场 | https://feeds.a.dj.com/rss/RSSMarketsMain.xml | 市场 |
| 经济学人 | https://www.economist.com/finance-and-economics/rss.xml | 宏观/金融 |
| 联合早报 | http://rss.spriple.org/zaobao/realtime/world | 国际-即时 |
| 同花顺 | https://rss.spriple.org/10jqka/realtimenews | 24小时全球财经 |

### 央行RSS

| 来源 | URL | 覆盖范围 |
|--------|-----|----------|
| 美联储 | https://www.federalreserve.gov/feeds/press_all.xml | 美联储声明 |
| 英国央行 | https://www.bankofengland.co.uk/rss | 英央行声明 |

## 指数接口

| 来源 | URL | 数据位置 |
|--------|-----|----------|
| US10YTIP | https://quote.cnbc.com/quote-html-webservice/restQuote/symbolType/symbol?symbols=US10YTIP&requestMethod=itv&noform=1&partnerId=2&fund=1&exthrs=1&output=json&events=1 | FormattedQuoteResult.FormattedQuote[].last |
| ICE U.S. Dollar Index | https://quote.cnbc.com/quote-html-webservice/restQuote/symbolType/symbol?symbols=.DXY&requestMethod=itv&noform=1&partnerId=2&fund=1&exthrs=1&output=json&events=1 | FormattedQuoteResult.FormattedQuote[].last |
