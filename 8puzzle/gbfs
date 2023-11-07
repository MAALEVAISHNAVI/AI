from gbfs import Greedy

#initial state
n=int(input("Enter n\n"))
print("Enter your" ,n,"*",n,"puzzle")
root=[]
for i in range(0,n*n):
    p=int(input())
    root.append(p)

print("The given state is", root)

#count the number of inversions
def inv_num(puzzle):
    inv=0
    for i in range(len(puzzle)-1):
        for j in range(i+1, len(puzzle)):
            if ((puzzle[i]>puzzle[j]) and puzzle[i] and puzzle[j]):
                inv+=1
    return inv

def solvable(puzzle):
    inv_counter=inv_num(puzzle)
    if (inv_counter%2==0 ):
        return True
    return False

from time import time
if solvable(root):
    print("Solvable,please wait. \n")

    time3=time()
    Greedy_solution=Greedy(root,n)
    Greedy_time=time()-time3
    print("Greedy solution is",Greedy_solution[0])
    print("Number of explored nodes is",Greedy_solution[1])
    print("Greedy time",Greedy_time,"\n")
else:
    print("Not solvable")
