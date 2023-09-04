#:-{(
import re
print ('Задание на 60 баллов')
print('Искомый смайлик:')
test = input().strip()#стрип убирает пробелы
smile = re.compile(re.escape(test))
test1 = "PO\[-{-[\XP=:{:;:{;[XP\(O)){/9P/OX;:{-{][:-{(<-O|{POO99:;\{[[|\/;:<-{-[\XO=:{:;(:Х{)(|/9PXP|{P-XO}/\:-O"
match = smile.findall(test1)
print( 'Тест:', len(match))
print ('--------------------------------')
print ('Задание +18 баллов', 'Вариант 0')
print('Введите хайку:')
test1 = str(input())
slash = re.compile(r'/')
ifnot = slash.findall(test1)
gl = "[уеыаоэёяию].*"
haiku = ".*" + gl*5 + "\/.*" + gl*7 + "\/.*" + gl*5 #паттерн с заданной переменной
print(re.findall(haiku, test1, re.IGNORECASE)) # паттерн, исходный текст, игнор регистра
if (re.findall(haiku, test1, re.IGNORECASE)) == []: print ('Не хайку!')
if (re.findall(haiku, test1, re.IGNORECASE)) == [test1]: print ('Хайку!')
if len(ifnot) <2: print('Должно быть 3 строки.')
print ('--------------------------------')
print ('Задание +22 балла', 'Вариант 2')
shifr = re.compile('\d\d?\d?\s?[+|\-|*|\/]\s?\d\d?\d?')
test1 = str(input())
match = shifr.findall(test1)

print ("Найденный пример:",match)
a = match
a = str(a).split(' ')
x1 = a[0][2:]
x2 = a[-1][:-2]
x3 = a[1]
#вытаскиваем из строки первое, второе число и знак между
newx1 = 4*int(x1)*int(x1) - 7
newx2 = 4*int(x2)*int(x2) - 7
#Шифруем
if x3 == '+': print("Шифр:", newx1 + newx2)
if x3 == '-': print("Шифр:",newx1 - newx2)
if x3 == '*': print("Шифр:",newx1 * newx2)
if x3 == '/': print("Шифр:",newx1 / newx2)

#ПРОВЕРКА
#4*32^2 - 7  = 4893
#4*12^2 - 7 = 569
#Шифр: 4893 - 569 = 4324 - верно
print('-------------------------------')
print('Дополнительное задание с почтой:')
import re
print('Введите почту:')
test1 = str(input())
domen = re.compile(r'^\w*\d*\.?\w*\d*@([a-z]*\.(?:ru|com|ua|by)\b)')#регулярка проверки на почту, удовлетворяет ли условиям существования почты
match = domen.findall(test1)
if len(match) == 0: print('Неверная почта')
else:
    print('\033[92m' + '\033[1m'+ 'Верная почта')
    print('\033[0m' + 'Введите пароль:')
    strl = 'Верная почта'
    pswrd = input()
    for i in range(0, len(pswrd)-2):
        line = pswrd[i]+pswrd[i+1]+pswrd[i+2]
        if len(re.findall(r''+line, test1))!=0:
            print('\033[91m' + '\033[1m'+'Слабый пароль. Повторяется три символа из названия почты')
            strl = '1'
            break
    if strl != '1': print('Верный пароль')

