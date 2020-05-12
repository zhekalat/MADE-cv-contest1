Как запускать - ```-n resnext50_140crop_aug_30ep -d data -b 112 -e 15 -lr 0.005 --gpu --draw```

Из дополнительных библиотек используется оптимизатор RAdam из [репозитория на GitHub](https://github.com/LiyuanLucasLiu/RAdam)

Результат:
![Kaggle submit score](https://i.imgur.com/O96smAn.png)

Что изменилось по сравнению с бейзлайном:
- Добавил аугментации: повороты/сдвиги/масштабирование/яркость/контрастность/размытие
- Заменил resnet18 на resnext50
- Заменил Adam на RAdam
- Добавил LR scheduler
- Повысил CROP_SIZE до 140
- Пришлось снизить размер батча из-за ограничений видеопамяти
