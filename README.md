def nwd(a,b):
    while b!=0:
        a,b = b,a%b
    return a


licznik = 0
with open("liczby.txt") as dane:
    for wiersz in dane:
        liczby=wiersz.split()
        liczby = [int(x) for x in liczby] #zamiana na int
        #liczby_int=[]
        #for liczba in liczby: zamiana na int 2 sposob
            #liczby_int.append(int(liczba))
        print(wiersz)
        print(liczby)
        liczby_do_sort=liczby.copy()
        liczby_do_sort.sort()

        if liczby_do_sort == liczby:
            licznik=licznik+1
            print(wiersz)
            print(liczby)
            print(liczby_do_sort)
            print(licznik)

        nwd3 = nwd(liczby[0],liczby[1],liczby[2])
        print(nwd3)
