# 智慧金字塔解题练习
## 背景

just for fun

在京东买了这个叫智慧金字塔的玩具给女儿玩

<img src=".\img\hnv_gpic1.png" style="zoom:50%;" />

结果第527道题,她解不开, 我试了很久也没解开...

<img src=".\img\hnv_gpic3.jpg" style="zoom:50%;" />

前面试了一些题目基本都很快解出...

于是编个代码来跑跑看...(不考虑效率,只管暴力)

结果还是代码管用...



## 使用

1. 确保电脑能跑python

2.  在main.py中设置questions. 

    将你要解的题目录入进去, 如图,第588题参考

<img src=".\img\hnv_gpic7.jpg" style="zoom:50%;" />

```python
    questions = {
        '588': {
            'tmap': [
                [O],
                [O, O],
                [O, O, O],
                [O, O, O, O],
                [X, X, X, O, O],
                [X, X, X, X, O, O],
                [X, X, X, X, O, O, O],
                [X, X, X, X, O, O, O, O],
                [X, X, X, X, O, O, O, O, O],
                [X, X, X, X, O, O, O, O, O, O]
            ],
            'unused': [it1, it2, it6, it7, it10, it11, it12]
        },
        '527': {
            'tmap': [
                [O],
                [O, O],
                [O, O, O],
                [O, O, O, O],
                [O, O, O, O, O],
                [O, O, O, O, O, X],
                [O, O, O, O, O, X, X],
                [O, O, O, O, O, X, X, X],
                [X, O, O, O, O, X, X, X, X],
                [X, X, X, X, X, X, X, X, X, X]
            ],
            'unused': [it10, it2, it5, it9, it12, it7, it6]
        },
        # 在此按上面格式继续增加题目
    }
```

​	'tmap': 已使用的位置填大写X, 需要代码放置的位置填大写O.

​	'unused': 将需要代码来放置的块添加进去, 如第一块为 it1 , 编号如下:

<img src=".\img\hnv_gpic5.jpg" style="zoom:50%;" />

​    题目增加完毕之后, 将question变量设置为你要解的题目编号.

```python
question = '588'
```

3. 运行python main.py即可得到答案. (一般很快出解, 找出全部答案需要很久很久很久, 588题有13个解, 不确保没有bug.)

   如玩的是矩形的题目,请自行修改tmap.

   

```shell
start question:  588
************* answer *************
['1']
['1', '1']
['2', '2', 'C']
['2', '2', 'C', 'C']
['X', 'X', 'X', 'C', 'C']
['X', 'X', 'X', 'X', '6', '6']
['X', 'X', 'X', 'X', '6', '6', '6']
['X', 'X', 'X', 'X', '7', '7', '7', '7']
['X', 'X', 'X', 'X', '7', 'A', 'B', 'B', 'B']
['X', 'X', 'X', 'X', 'A', 'A', 'A', 'A', 'B', 'B']

************* answer *************
['1']
['1', '1']
['2', '2', 'C']
['2', '2', 'C', 'C']
['X', 'X', 'X', 'C', 'C']
['X', 'X', 'X', 'X', '6', '6']
['X', 'X', 'X', 'X', '6', '6', '6']
['X', 'X', 'X', 'X', '7', '7', '7', '7']
['X', 'X', 'X', 'X', '7', 'B', 'B', 'B', 'A']
['X', 'X', 'X', 'X', 'B', 'B', 'A', 'A', 'A', 'A']

......
```