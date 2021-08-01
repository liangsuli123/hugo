---
title: "python打印💗"
date: 2016-04-25T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "Python1"
---



```

#打印爱心
import time
sentence = "forever"
for char in sentence.split():
   allChar = []
   for y in range(12, -12, -1):
       lst = []
       lst_con = ''
       for x in range(-30, 30):
            formula = ((x*0.05)**2+(y*0.1)**2-1)**3-(x*0.05)**2*(y*0.1)**3
            if formula <= 0:
                lst_con += char[(x) % len(char)]
            else:
                lst_con += ' '
       lst.append(lst_con)
       allChar += lst
   print('\n'.join(allChar))
   time.sleep(1)




                foreverfo           rforeverf               
            everforeverforeve   reverforeverforev           
          oreverforeverforeverforeverforeverforever         
         foreverforeverforeverforeverforeverforeverf        
        rforeverforeverforeverforeverforeverforeverfo       
        rforeverforeverforeverforeverforeverforeverfo       
        rforeverforeverforeverforeverforeverforeverfo       
        rforeverforeverforeverforeverforeverforeverfo       
        rforeverforeverforeverforeverforeverforeverfo       
        rforeverforeverforeverforeverforeverforeverfo       
         foreverforeverforeverforeverforeverforeverf        
          oreverforeverforeverforeverforeverforever         
          oreverforeverforeverforeverforeverforever         
            everforeverforeverforeverforeverforev           
             verforeverforeverforeverforeverfore            
              erforeverforeverforeverforeverfor             
                foreverforeverforeverforeverf               
                  reverforeverforeverforeve                 
                    verforeverforeverfore                   
                       foreverforeverf                      
                          everforev                         
                             rfo                            
                              f                       

```







    


