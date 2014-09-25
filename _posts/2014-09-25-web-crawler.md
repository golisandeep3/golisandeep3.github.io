---
layout: post
title: How to write your own WebCrawler
---

Writing your own web crawler is very easy.There are many standard libraries for parsing html pages. Jsoup ([link) ](http://jsoup.org/)is one of the Java library that parses an html page and returns all the elements in that page.
To connect to a particular website just use

***Document doc = Jsoup.connect(encodeUrl("www.sandeepgoli.com")).get();***

Use above doc object to get all links in that particular website

***Elements link = doc.select("a");***

Then you can recusrively call to get in depth links from current links

Example:

    public  void  getLinksRecursive(String url,int depth) {
    		if(depth<=0)
    			return;
    		Elements children= parseurls(url);
    		if(children!=null)
    		{
    			for(Element link : children) {
    			String relHref = link.absUrl("href");
    					addNodesRecursive(relHref,depth-1);
    			} 
    		}
    	}*
You have to add more constraints to eliminate loops in your crawler.Use tree based data structure to store all the links.
