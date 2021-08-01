---
title: "selenium破解人人登陆验证码"
date: 2017-07-18T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "selenium破解人人登陆验证码"
---
```
from selenium import webdriver
from PIL import Image
from chaojiying import Chaojiying_Client
import time

driver = webdriver.Chrome()

driver.get('http://ww.renren.com')

driver.find_element_by_xpath('//*[@id="email"]').send_keys("人人网账号")
driver.find_element_by_xpath('//*[@id="password"]').send_keys('password')
#截屏
driver.save_screenshot("renren.png")
#获取宽高和坐标（查找验证码所在元素，获取验证码的坐标和宽高，）
img = driver.find_element_by_xpath('//*[@id="verifyPic_login"]')
#获取x坐标
x = img.location['x']
#y坐标
y = img.location['y']
#获取宽
width = img.size['width']
#获取高
height = img.size['height']
#抠图(在renren.png中抠图)  pip install PIL
screen = Image.open('renren.png') #加载截屏

code = screen.crop((x,y,x+width,y+height))#截出验证码
code.save('code.png') #将验证码保存
time.sleep(2)
#发送给超级鹰破解
chaojiying = Chaojiying_Client('超级鹰账号', 'password', '96001')
im = open('code.png', 'rb').read()
#2004 是超级鹰破解验证码的验证码类型
c = chaojiying.PostPic(im,2004)['pic_str']
print(c)
#将验证码输入到框里
driver.find_element_by_xpath('//*[@id="icode"]').send_keys(c)
time.sleep(3)
#点击登陆
driver.find_element_by_xpath('//*[@id="login"]').click()

```