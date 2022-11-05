# LR6
## Лабораторная работа №6
## Система контроля версий
#### **Цель лабораторной работы:** изучение базовых возможностей системы управления версиями, опыт работы с _Git Api_, опыт работы с локальным и удаленным репозиторием.
### **Ход работы**  
После создания аккаунта на GitHub, была создана копия в личное хранилище.  
![This is an image](/images/1.png)  
После установки Git был настроен клиент git.  
```
git config --global user.name "4118SibatovaYR"  
git config --global user.email "sibatova.yana66@gmail.com"  
git config --list  
```
![This is an image](/images/2.png)  
Далее личный удаленный репозиторий был копирован на компьютер.  
```
git clone https://github.com/4118SibatovaYR/LR6.git  
```
![This is an image](/images/3.png)  
Создадим файл 12345.txt, который закоммитим в ветку branch1.  
![This is an image](/images/4.png)  
![This is an image](/images/5.png)  
Подтянем изменения в локальный репозиторий. 
```
git pull  
```
![This is an image](/images/6.png)  
Посмотрим историю изменений веток master и branch1, соответственно.  
```
git log  
```
```
git checkout branch1  
git log  
```
![This is an image](/images/7.png)  
![This is an image](/images/8.png)  
Посмотрим последние изменения.  
```
git status  
```
![This is an image](/images/9.png)  
Выполним слияние веток, разрешив конфликт.  
```
git merge branch1  
git status  
```
![This is an image](/images/10.png)  
![This is an image](/images/11.png)  
Тогда файл до редактирования выглядит так.  
![This is an image](/images/12.png)  
После редактирования завершим слияние веток.  
```
git add mergefile.txt  
git commit -m "well done"  
```
![This is an image](/images/13.png)  
Удалим ветку branch1.  
```
git branch -d branch1  
``` 
![This is an image](/images/14.png)  
Далее создадим файл new.txt, где будут происходить изменения.  
```
nano new.txt  
git add new.txt  
``` 
![This is an image](/images/15.png)  
И закоммитим его.  
```
git commit -m "new file"  
```
![This is an image](/images/16.png)  
Сделаем так еще два раза.  
![This is an image](/images/17.png)  
Файл new.txt выглядит так.  
![This is an image](/images/19.png)  
Сделаем откат коммита. Последнее изменение исчезло.  
```
git reset --hard HEAD~  
git log  
```
![This is an image](/images/20.png)  
Создадим ветку report для отчета.  
```
git branch report  
git checkout report  
```
![This is an image](/images/21.png)  