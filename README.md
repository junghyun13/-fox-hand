# -fox-hand
# python
#The first row is given the number of N (1 ≤ N ≤ 10) pairs of fingers touching each other. From the second line to N lines, two numbers between 1 and 5, which mean two fingers touching each other, are given, separated by a space. 1 means thumb, 2 means index finger, 3 means middle finger, 4 means ring finger, and 5 means little finger. There is never a case where the same pair is given multiple times, including in different order of input, or a pair consisting of only one finger is given. 첫 번째 줄에 서로 닿아 있는 손가락 쌍의 개수 N(1 ≤ N ≤ 10)이 주어진다. 두 번째 줄부터 N개의 줄에 걸쳐 서로 닿아 있는 두 손가락을 의미하는 1 이상 5 이하의 숫자 두 개가 공백으로 구분되어 주어진다. 1은 엄지손가락, 2는 검지, 3은 중지, 4는 약지, 5는 새끼손가락을 의미한다. 입력 순서가 다른 것을 포함하여 같은 쌍이 여러 번 주어지거나 한 손가락만으로 이루어진 쌍이 주어지는 경우는 없다.(첫 번째 줄에 도주의 손 모양을 여우 사인이라고 할 수 있으면 Wa-pa-pa-pa-pa-pa-pow!를, 그렇지 않으면 Woof-meow-tweet-squeek을 출력한다.)
N=int(input())
finger=[[]]
answer=True
for i in range(5):
    finger.append([])
for i in range(N):
    a,b=map(int,input().split())
    finger[a].append(b)
    finger[b].append(a)
if (3 and 4 not in finger[1]) or len(finger[1])!=2:
    answer=False
elif (1 and 4 not in finger[3]) or len(finger[3])!=2:
    answer=False
elif(1 and 3 not in finger[4]) or len(finger[4])!=2:
    answer=False
if answer==True:
    print('Wa-pa-pa-pa-pa-pa-pow')
else:
    print('Woof-meow-tweet-squeek')
#result--> 3  1 3  4 3  1 4  Wa-pa-pa-pa-pa-pa-pow
