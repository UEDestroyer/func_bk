add function 

sejango - 3 arguments form(django),key(in form cleaned data),var(return if key is not find)


adder - dict,**kwargs 
add to dict all arguments kwargs



iswhiter(color(HEX),porog) - color=color for checking, porog = threshold for lightening
isdarker(color(HEX),porog) - color=color for checking, porog = threshold for darkering
brighness(rgb(RGB)) - rgb to float
hex_to_rgb(hex_xolor(HEX)) - you know


find(lst,sim) - lst=list sim=obj for searching, find obj inlist and return he index
 
and test
def listrand(min,max,kol):
    a=[]
    otch = 0
    while otch<kol:
        a.append(random.randint(min,max))
        otch+=1
    return a

def IsKeyInDict(data, key):
    return key in data
def stepen(number,stepan):
	if stepan==0:
		return 1
	
	else :
		return number * stepen(number,stepan-1)
	
def faktorial(number):
	
	if number==0 or number == 1:
		return 1
	

	else:
		return number * faktorial(number-1)
	
def chibo(number):
	
	if number==0:
		return 1
	
	elif number==1:
		return 0
	
	else:
		return chibo(number-1) + chibo(number-2)
	
def summa(number):
	if number<1:
		return 0
	
	else:
	    return int(number%10) + summa(number/10)

class for django:


Color:
    abstract model
    for inheritance models add to model variable: color and function: isdarker, iswhite, hexrgb, rgbtofloat 


LBASE:
    
    add:
        context_paginator_name = name paginator for context
        page_n =  page-quantity for correct work need paginate_by
        page_n:
            if len(queryset)>=page_n:
                return (calculations for a given number of pages)
            else:
                return=paginate_by

    example:
    class index(LBASE):
        model=Tovar
        template_name="mains/icecream_list.html"
        context_object_name='date'
        paginate_by=5
        paginate_orphans=2
        page_n=5 ...