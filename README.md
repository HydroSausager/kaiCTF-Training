# kaiCTF-Training
# RecoStego100 <br> 
+ [картинка](https://vk.com/doc232954835_499412059)<br>
+ Решение:<br>Если скормить файл тулзе exiftool или любым иным другим способом прочитаем метаданные, то увидим, что присутствует GeoTag.<br>Если мы скормим этот файл на сайт (https://www.geoimgr.com/) или любой другой аналог из гугла, то приблизив карту увидим флаг.<br>
# Is it an archive?
+ Дан [архив .rar](https://drive.google.com/file/d/0BzfPP2u0U3CscEpoNW5ndnBfdTA/view?usp=sharing)<br>
Если посмотреть на файл в HEX-редакторе, то первым делом увидим [сигнатуру](https://ru.wikipedia.org/wiki/%D0%A1%D0%BF%D0%B8%D1%81%D0%BE%D0%BA_%D1%81%D0%B8%D0%B3%D0%BD%D0%B0%D1%82%D1%83%D1%80_%D1%84%D0%B0%D0%B9%D0%BB%D0%BE%D0%B2) PNG файла:<br>
![alt text](https://pp.userapi.com/c852232/v852232249/11429c/EJxqgWRH9jQ.jpg)
Если же просканируем BinWalk'ом, то он тоже уведомит нас о наличии png картинки.
+ Решение 1:<br> Если попробуем ```binwalk -e Wrong.rar``` , то он выплюнет нам какую-то дичь. Поэтому стоит ему дать понять, что мы ожидаем от него png картинку командой ```binwalk -D 'png image:png' Wrong.rar```. Получаем огромную картинку.<br> Идем в StegSolve, чтобы картинка помещалась, можно воспользоваться командой ```convert 0.png -resize 50% 1.png```
+ Решение 2:<br> ```foremost Wrong.rar``` -> StegSolve
+ Решение 3:<br> Изменяем расширение файла на .png -> StegSolve
# VapeNation
+ Решение: StegSolve
# AudaCity
Дан [.waw файл](https://vk.com/doc232954835_499514389)
+ Решение: в подсказке сказано, что нам нужен spetrum analyzer, берем [первый из гугла](https://academo.org/demos/spectrum-analyzer/)
![](https://pp.userapi.com/c851024/v851024089/116fb1/VVjlT6QnKRs.jpg)
# The Vault
+ Решение: (https://www.youtube.com/watch?v=VRgAL5y4HAQ)
