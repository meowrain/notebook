# GIT SSH免密登录

## 第一步

`ssh-keygen -t rsa -C  your email`

![image-20220814183238272](https://static.meowrain.cn/i/2022/08/14/uay6gx-3.png)

## 第二步

`cat ~/.ssh/id_rsa.pub`

![image-20220814183309666](https://static.meowrain.cn/i/2022/08/14/ubdblt-3.png)

## 第三步

打开设置

![image-20220814183341798](https://static.meowrain.cn/i/2022/08/14/ubkb7p-3.png)



![image-20220814183413549](https://static.meowrain.cn/i/2022/08/14/ubznux-3.png)

![image-20220814183438821](https://static.meowrain.cn/i/2022/08/14/uc580w-3.png)

![image-20220814183501342](https://static.meowrain.cn/i/2022/08/14/uciium-3.png)

![image-20220814183539872](https://static.meowrain.cn/i/2022/08/14/ucqx4u-3.png)

![image-20220814183644022](https://static.meowrain.cn/i/2022/08/14/udd8lh-3.png)

这样克隆下来以后，git pull和git push就不需要身份验证了