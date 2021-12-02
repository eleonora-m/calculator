# calculator
program: # which asks the user for a number and an action, # to do with it: # display the sum of its digits, # output the maximum digit or output the minimum digit.
def max_n(x):
  maxx = 0
  while x >0:
    if x %10>=maxx:
      maxx = x %10
      x= x //10
    else:
      x = x//10
  print()
  print('Максимальная цифра числа: ', maxx)

def min_n(x):
  minn = x%10
  while x>0:
    if x %10<=minn:
      minn = x %10
      x = x//10
    else:
      x = x//10
  print()
  print('Минимальная цифра числа: ', minn)
  
def sum_number(x):
  sum_n = 0
  while x > 0:
    sum_n += x % 10
    x //= 10
  print('Сумма цифр числа =', sum_n)
x = int(input('Enter  number: '))
choice = int(input('Введите действие, которое хотите совершить(0 - вывести сумму его цифр; 1 - вывести максимальную цифру; 2 - вывести минимальную цифру): ')) 
if choice== 0:
  sum_number(x)
elif choice == 1:
  max_n(x)
elif choice == 2:
  min_n(x)
else:
  print('Ошибка')
