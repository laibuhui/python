

```python
'1'*10#十个字符串相乘
```




    '1111111111'




```python
print 25**0.5# 开根号
'''
多行注释
'''
print 3
#module
import math
math.sqrt(25)

start = 0
end = 10
print range(start,end)#range函数
print range(10,0)#默认增加步长为1，这里得到一个空字符，可加上第三个增量调整步长
print range(9,-1,-1)
#print range(0,10,0.3)#希望是整形步长
#浮点型步长
max_num = 15
array = range(0,max_num+1)
print array
float_array = [x/float(max_num) for x in array]#也可以写成10.0
print float_array

#换种复杂的写法
'''
num_of_elements = len(arryay)
float_array = []
for i in range(0,num_of_elements):
    temp = array[i]/(max_num+1.0)#这里加1.0是为了变成浮点型
    float_array.append(temp)
'''

candidates = range(0,20)

#for n in range(0,20)两种写法都可以

for n in candidates:
    a1 = n**0.5
    a2 = math.sqrt(n)
    assert((a1-a2)==0)
    print (n,a1,a1-a2)
```

    5.0
    3
    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    []
    [9, 8, 7, 6, 5, 4, 3, 2, 1, 0]
    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15]
    [0.0, 0.06666666666666667, 0.13333333333333333, 0.2, 0.26666666666666666, 0.3333333333333333, 0.4, 0.4666666666666667, 0.5333333333333333, 0.6, 0.6666666666666666, 0.7333333333333333, 0.8, 0.8666666666666667, 0.9333333333333333, 1.0]
    (0, 0.0, 0.0)
    (1, 1.0, 0.0)
    (2, 1.4142135623730951, 0.0)
    (3, 1.7320508075688772, 0.0)
    (4, 2.0, 0.0)
    (5, 2.23606797749979, 0.0)
    (6, 2.449489742783178, 0.0)
    (7, 2.6457513110645907, 0.0)
    (8, 2.8284271247461903, 0.0)
    (9, 3.0, 0.0)
    (10, 3.1622776601683795, 0.0)
    (11, 3.3166247903554, 0.0)
    (12, 3.4641016151377544, 0.0)
    (13, 3.605551275463989, 0.0)
    (14, 3.7416573867739413, 0.0)
    (15, 3.872983346207417, 0.0)
    (16, 4.0, 0.0)
    (17, 4.123105625617661, 0.0)
    (18, 4.242640687119285, 0.0)
    (19, 4.358898943540674, 0.0)



```python
#循环终止
for i in range(100):
    if (i>=10):
        break

for i in range(10):
    if i%2 == 1:
        print i
        
for i in range(10):
    if i%2 == 0:
        continue  #break
    print i#没有
    
```

    1
    3
    5
    7
    9
    1
    3
    5
    7
    9



```python
#指数函数  e^x==>math.exp(x)
#对数函数  log_b^x==>math.log(x,b)
#自然对数  ln(x)==>math.log(x)
#二进制对数ln(x)==>math.log(x,2)
math.exp(1)
```




    2.718281828459045




```python
#变量赋值：从右边往左边赋值.不能用python保留字作为变量名
x = 1
y = 2
print (x,y)
y = x#把x的值赋给y
x = 5
print (x,y)
import keyword
print keyword.kwlist
```

    (1, 2)
    (5, 1)
    ['and', 'as', 'assert', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'exec', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'not', 'or', 'pass', 'print', 'raise', 'return', 'try', 'while', 'with', 'yield']



```python
#课堂练习1:
base = 250000
year = input("year:")
base_year = 2017
rate = 0.012
P = base*math.exp(rate*(year-2017))
print ("population at year %d:%g"%(year,P))
target = float(input("target:"))#400000.0
#target/base = math.exp(rate*t)
#math.log(target/base) = rate*t
t = math.log(target/base)/rate
print int(t+2017)


```

    year:2020
    population at year 2020:259164
    target:400000
    2056



```python
# 函数：
def power_function(x,a):
    return x**a

def squar_function(x):
    return power_function(x,2)

print power_function(5,2)
print squar_function(5)
```

    25
    25



```python
#课堂练习2:
base = 250000
base_year = 2017
rate = 0.012

def compute_population(year):
    return base*math.exp(rate*(year-2017))

def which_year(target):
    t = math.log(target/base)/rate
    return int(t+2017)

year = input("year:")
print ("population at year %d:%g"%(year,compute_population(year)))

taget = float(input("target:"))#400000.0
print which_year(target)



```

    year:2020
    population at year 2020:259164
    target:400000
    2056



```python
#条件控制语句:控制语句后都以冒号结尾
def my_max(x,y,z):
    if x >= y:
        if x >= z:
            return x
        else:
            return z
    else:
        if y >= z:
            return y
        else:
            return z
        
x = input("x:")
y = input("y:")
z = input("z:")

my_max(x,y,z)
```

    x:2
    y:5
    z:3





    5




```python

```
