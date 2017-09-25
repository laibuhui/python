# 基本运算
'1'*10#十个字符串相乘
print 25**0.5# 开根号
'''
多行注释
'''
print 3
#module
import math
math.sqrt(25)

#  range函数
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
    
# 循环终止
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

#指数函数  e^x==>math.exp(x)
#对数函数  log_b^x==>math.log(x,b)
#自然对数  ln(x)==>math.log(x)
#二进制对数ln(x)==>math.log(x,2)
math.exp(1)

# 变量赋值：从右边往左边赋值.不能用python保留字作为变量名
x = 1
y = 2
print (x,y)
y = x#把x的值赋给y
x = 5
print (x,y)
import keyword
print keyword.kwlist


# 课堂练习1:
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

# 函数：
def power_function(x,a):
    return x**a

def squar_function(x):
    return power_function(x,2)

print power_function(5,2)
print squar_function(5)


# 课堂练习2:
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



# 条件控制语句:控制语句后都以冒号结尾
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
