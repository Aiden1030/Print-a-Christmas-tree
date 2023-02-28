#author: Aiden Hyun, 260974945
import math
def is_triangle(a,b,c):
    ''' (float, float, float) -> string

indicates if it is possible to make a triangle using the three side lengths given as input.

>>>  is_triangle(10,5,16)
No, there isn't a triangle with side lengths a, b and c!
>>> is_triangle(5,5,5)
Yes, there is a triangle with side lengths a, b and c!

'''
    #Triangle inequality theorum
    if a <= 0 or b <= 0 or c<= 0:
        print("No, there isn't a triangle with side lengths a, b and c!")
    if a+b >= c and a+c >= b and b+c>=a:
       print('Yes, there is a triangle with side lengths a, b and c!')
    else:
        print("No, there isn't a triangle with side lengths a, b and c!")
    

def is_special_triangle(a,b,c):
    '''(float,float,float) -> string
 indicates whether the triangle is equilateral, isoceles, or right-angle
 
 >>> is_special_triangle(1,1,1)
The triangle is equilateral
The triangle is isosceles
 
>>> is_special_triangle(2,2,16)
The triangle is isosceles

>>> is_special_triangle(4,3,5)
The triangle is right-angle


 '''
    if a == b and b ==c:
        print("The triangle is equilateral")
    if a == b or b==c or c==a:
        print('The triangle is isosceles')
    ab = a**2+b**2
    bc= b**2+c**2
    ac = c**2+a**2
    
    if c**2==ab or a**2 == bc or b**2 ==ac:
        print('The triangle is right-angle')

def perimeter_of_triangle(a,b,c):
    ''' (float, float, float)-> float

prints the perimeter of the triangle

>>> perimeter_of_triangle(1,1,1)
3
>>> perimeter_of_triangle(1,2,3)
6

'''
    print(a+b+c)

def area_of_triangle(a,b,c):
    ''' (float, float, float) -> float
prints the area of the triangle

>>> area_of_triangle(4,5,6)
10
>>> area_of_triangle(40,50,6)
Traceback (most recent call last):
  File "<pyshell>", line 1, in <module>
  File "/Users/aidenhyun/triangles.py", line 64, in area_of_triangle
    s = round(math.sqrt(t*(t-a)*(t-b)*(t-c)))
ValueError: math domain error
>>> area_of_triangle(40,50,60)
992
>>> area_of_triangle(1,2,3)
0

'''
    
    
    t= (a+b+c)/2
    
    s = round((math.sqrt(t*(t-a)*(t-b)*(t-c))),15)
    print(s)
    
def angles_of_triangle(a,b,c):
    '''(float, float, float) -> float,float,float
prints three angles of the triangle, in degrees

>>> angles_of_triangle(1,1,1)
60
60
60
180
>>> angles_of_triangle(1235120,23512351,23512)
Traceback (most recent call last):
  File "<pyshell>", line 1, in <module>
  File "/Users/aidenhyun/triangles.py", line 72, in angles_of_triangle
    angle1 = round(57.29*(math.acos((b**2+c**2-a**2)/(2*b*c))))
ValueError: math domain error
>>> angles_of_triangle(10000000,10000000,10000000)
60
60
60
180
'''
    angle1 = round((180/math.pi)*(math.acos((b**2+c**2-a**2)/(2*b*c))),15)
    angle2 = round((180/math.pi)*(math.acos((a**2+c**2-b**2)/(2*a*c))),15)
    angle3 = round((180/math.pi)*(math.acos((a**2+b**2-c**2)/(2*a*b))),15)
    
    print(angle1)
    print(angle2)
    print(angle3)
    
    
def circumscribed_circle(a,b,c):
    ''' (float, float, float)-> float
prints the radius of the circumscribed circle

>>>  circumscribed_circle(10,10,10)
5.773502691896258

>>>  circumscribed_circle(4,5,6)
3.023715784073818
'''
   
    angle1 = math.radians((180/math.pi)*(math.acos((b**2+c**2-a**2)/(2*b*c))))
    angle2 = math.radians((180/math.pi)*(math.acos((a**2+c**2-b**2)/(2*a*c))))
    angle3 = math.radians((180/math.pi)*(math.acos((a**2+b**2-c**2)/(2*a*b))))
    
    
    r= (a/math.sin(angle1))/2
    r2=(b/math.sin(angle2))/2
    r3=(c/math.sin(angle3))/2
    
    average_r=round( ((r+r2+r3)/3),15)
    
    print(average_r)

def inscribed_circle(a,b,c):
    ''' (float, float, float) -> float
prints the radius of the inscribed circle

>>> inscribed_circle(4,5,6)
1.3228756555322954
>>>  inscribed_circle(24,35,26)
7.339458226519417
'''
    
    angle1 = math.radians((180/math.pi)*(math.acos((b**2+c**2-a**2)/(2*b*c))))
    angle2 = math.radians((180/math.pi)*(math.acos((a**2+c**2-b**2)/(2*a*c))))
    angle3 = math.radians((180/math.pi)*(math.acos((a**2+b**2-c**2)/(2*a*b))))
    
    t= (a+b+c)/2
     
    r= (t-a)*(math.tan(angle1/2))
    r2= (t-b)*(math.tan(angle2/2))
    r3= (t-c)*(math.tan(angle3/2))
    
    average_r= r
     
    print(average_r)
    
def approximate_pi(n):
    '''(int) ->float
approximate the area of a circle with radius 1 calculating the area of an inscribed polygon

>>> approximate_pi(5)
2.377641290737884

>>> approximate_pi(100000)
3.141592651522707
'''
    
    angle = math.radians(360)/n
    h= math.cos(angle/2)
    a=2*math.sin(angle/2)
    
    area = round(n*0.5*h*a,15)
    print(area)
    
    
