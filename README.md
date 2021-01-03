# compute-gross-pay
num = 0
largest = -1
smallest = None
while True:
    num = input("Enter a number: ")
    if num == "done":
        break
    try :
        ival = int(num)
    except :
        print('Invalid input')
#print(ival)
    if smallest is None :
        smallest = ival
    elif ival < smallest :
        smallest = ival
    elif ival > largest :
        largest = ival
#print("ALL DONE")
print("Maximum is",largest)
print("Minimum is",smallest)

hrs = input("Enter Hours:")
rt = input("Enter Rate:")
try:
    h = float(hrs)
    r = float(rt)
except:
    print("Error, please enter numeric input")
    quit()
#print(h,r)
if h > 40:
    reg = h * r
    otp = (h - 40) * (r * 0.5)
    p = reg + otp
else:
    p= hrs * h
print("Pay:",p)
