# cards
a = list(map(int,input().split()))
n = len(a)
d = 0
m = 0
for i in range(n):
  if i%2 == 0:
    if a[0] > a[-1]:
      d = d + a[0]
      a.pop(0)
    else:
      d = d + a[-1]
      a.pop()
  else:
    if a[0] > a[-1]:
      m = m + a[0]
      a.pop(0)
    else:
      m = m + a[-1]
      a.pop()
#print(d)
#print(m)
x = abs(d-m)
if x > 1:
  if d >= m:
    print(f"Dheeraj wins with {x} cards !")
  else:
    print(f"Mansi wins with {x} cards !")
else:
  if d >= m:
    print(f"Dheeraj wins with {x} card !")
  else:
    print(f"Mansi wins with {x} card !")
