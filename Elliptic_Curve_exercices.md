```python
E = EllipticCurve([0, 7])
print("courbe E =>  " , E)
graph = plot(E,-4,3)
show(graph)

print(" Domaine F103 ")
n = 103
print('n= ', n)
Fp = GF(n)


a = 17
b = 64
y2 = b^2 % 103
x3= (a^3 + 7) % 103
print( y2 )
print ( x3 )
print (" a =" , a ,  "  b = ", b , " sur la courbe ?")
print ( y2 == x3 )


E = EllipticCurve(Fp,[0,7])
print("E =>  " , E)
graph = plot(E)
graph += point([17,64] , size= 20 , color='red')
show(graph)


print("E points" ,E.points())
print("E cardinality " , E.cardinality())
print("facteur " , factor(E.cardinality()))


def cherche(point_):
    t = False
    for P in E.points():
        if P != E(0): 
            
            if (point_ == P.xy()):
                print("Trouve")
                print (P.xy())
                
                t = True
    return t
            
        

# cherche si le point existe sur la courbe ?
mon_point_p = (17,65)
print(cherche(mon_point_p))

mon_point_p = (17,64)
print(cherche(mon_point_p))




# Exercise 1

# Evaluate whether these points are on the curve y2 = x3 + 7 over F223:

#    (192,105), (17,56), (200,119), (1,193), (42,99)



print(" Domaine F223 ")
n = 223
print('n= ', n)
Fp = GF(n)



E = EllipticCurve(Fp,[0,7])
print("E =>  " , E)
graph = plot(E)
show(graph)


mon_point_p = (192,105)
print(cherche(mon_point_p))



mon_point_p = (17,56)
print(cherche(mon_point_p))


mon_point_p = (200,119)
print(cherche(mon_point_p))


mon_point_p = (1,193)
print(cherche(mon_point_p))


mon_point_p = (42,99)
print(cherche(mon_point_p))




graph = plot(E)
graph += point((192,105) , size= 20 , color='red', legend_label = "(192,105)")
graph += point((17,56) , size= 20 , color='red' , legend_label = "(17,56)")
graph += point((1,193) , size= 20 , color='red' , legend_label = "(1,193)")
show(graph)





```

    courbe E =>   Elliptic Curve defined by y^2 = x^3 + 7 over Rational Field



![png](output_0_1.png)


     Domaine F103 
    n=  103
    79
    79
     a = 17   b =  64  sur la courbe ?
    True
    E =>   Elliptic Curve defined by y^2 = x^3 + 7 over Finite Field of size 103



![png](output_0_3.png)


    E points [(0 : 1 : 0), (0 : 25 : 1), (0 : 78 : 1), (1 : 27 : 1), (1 : 76 : 1), (2 : 18 : 1), (2 : 85 : 1), (3 : 31 : 1), (3 : 72 : 1), (5 : 21 : 1), (5 : 82 : 1), (6 : 29 : 1), (6 : 74 : 1), (7 : 12 : 1), (7 : 91 : 1), (8 : 2 : 1), (8 : 101 : 1), (9 : 18 : 1), (9 : 85 : 1), (13 : 12 : 1), (13 : 91 : 1), (17 : 39 : 1), (17 : 64 : 1), (19 : 45 : 1), (19 : 58 : 1), (20 : 30 : 1), (20 : 73 : 1), (22 : 47 : 1), (22 : 56 : 1), (24 : 21 : 1), (24 : 82 : 1), (25 : 39 : 1), (25 : 64 : 1), (27 : 29 : 1), (27 : 74 : 1), (33 : 10 : 1), (33 : 93 : 1), (34 : 45 : 1), (34 : 58 : 1), (35 : 31 : 1), (35 : 72 : 1), (36 : 2 : 1), (36 : 101 : 1), (38 : 17 : 1), (38 : 86 : 1), (42 : 48 : 1), (42 : 55 : 1), (46 : 27 : 1), (46 : 76 : 1), (49 : 37 : 1), (49 : 66 : 1), (50 : 45 : 1), (50 : 58 : 1), (51 : 32 : 1), (51 : 71 : 1), (53 : 7 : 1), (53 : 96 : 1), (56 : 27 : 1), (56 : 76 : 1), (59 : 2 : 1), (59 : 101 : 1), (60 : 4 : 1), (60 : 99 : 1), (61 : 39 : 1), (61 : 64 : 1), (64 : 4 : 1), (64 : 99 : 1), (65 : 31 : 1), (65 : 72 : 1), (66 : 37 : 1), (66 : 66 : 1), (68 : 17 : 1), (68 : 86 : 1), (69 : 7 : 1), (69 : 96 : 1), (70 : 29 : 1), (70 : 74 : 1), (74 : 21 : 1), (74 : 82 : 1), (75 : 32 : 1), (75 : 71 : 1), (76 : 10 : 1), (76 : 93 : 1), (78 : 48 : 1), (78 : 55 : 1), (80 : 32 : 1), (80 : 71 : 1), (82 : 4 : 1), (82 : 99 : 1), (83 : 12 : 1), (83 : 91 : 1), (84 : 7 : 1), (84 : 96 : 1), (85 : 47 : 1), (85 : 56 : 1), (86 : 48 : 1), (86 : 55 : 1), (90 : 30 : 1), (90 : 73 : 1), (91 : 37 : 1), (91 : 66 : 1), (92 : 18 : 1), (92 : 85 : 1), (96 : 30 : 1), (96 : 73 : 1), (97 : 10 : 1), (97 : 93 : 1), (99 : 47 : 1), (99 : 56 : 1), (100 : 17 : 1), (100 : 86 : 1)]
    E cardinality  111
    facteur  3 * 37
    False
    Trouve
    (17, 64)
    True
     Domaine F223 
    n=  223
    E =>   Elliptic Curve defined by y^2 = x^3 + 7 over Finite Field of size 223



![png](output_0_5.png)


    Trouve
    (192, 105)
    True
    Trouve
    (17, 56)
    True
    False
    Trouve
    (1, 193)
    True
    False



![png](output_0_7.png)



```python

```
