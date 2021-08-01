---
title: "selenium爬取优酷页面并下载图片"
date: 2017-07-13T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "selenium爬取优酷页面并下载图片"
---

```
from selenium import webdriver
import requests
driver = webdriver.Chrome()
#打开优酷
driver.get("http://www.youku.com")
#点开优酷片库
driver.find_element_by_xpath("//*[@id='m_2544']/div/ul/li[6]/span[1]/a").click()
#获取所有img元素
listImg = driver.find_elements_by_xpath("//div[@class='vaule_main']//li/div/div/img")
#取img的src值
listSrc = []
for img in listImg:
    src = img.get_attribute('src')
    listSrc.append(src)
print(len(listImg))
#下载图片
session = requests.session()
for index,value in enumerate(listSrc):
    response = session.get(value)
    with open(str(index)+'.png',mode='wb') as f:
        f.write(response.content)

```