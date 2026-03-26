# MarTech SEO Toolkit 🚀

**Professional SEO Strategies** from [MarTech Agency](https://martechagency.net)

## 🔍 Essential SEO Tools (2026)
- [Google Search Console](https://search.google.com/search-console) - Site performance
- [Ahrefs Webmaster Tools](https://ahrefs.com/webmaster-tools) - Free backlink checker  
- [SEMrush](https://semrush.com) - Keyword research
- [Google Analytics 4](https://analytics.google.com) - Traffic insights

## 📈 Key SEO Metrics
**DA** (Domain Authority) 40+ target - site link popularity  
**DR** (Domain Rating) 50+ target - backlink quality  
**UR** (URL Rating) 30+ target - page strength  
**Spam Score** <5% - avoid penalties  

## 🎯 Link Building Framework
1. Profile Links (DA 90+) [MarTech Agency](https://martechagency.net)
2. Guest Posts on niche sites (DA 50+)  
3. Resource Pages - "Best SEO tools"
4. HARO responses for media mentions
5. Broken Link Building

## 💻 Backlink Checker Script

```python
import requests
from bs4 import BeautifulSoup

def check_backlinks(url):
    headers = {'User-Agent': 'Mozilla/5.0'}
    response = requests.get(url, headers=headers)
    soup = BeautifulSoup(response.content, 'html.parser'}
    
    external_links = []
    for link in soup.find_all('a', href=True):
        if 'http' in link['href'] and 'nofollow' not in link.get('rel', []):
            external_links.append(link['href'])
    
    return f"Found {len(external_links)} dofollow external links"

# Test our site
print(check_backlinks('https://martechagency.net'))
