# hackercode
solutions to various hacker rank questions
# find the lowest score in physics test and sort the names if one or more students have low scores
names=[]
marks=[]
for _ in range(int(input())):  #takes no of inputs in the range bracket
    name=input()
    names.append(name)
    mark=float(input())
    marks.append(mark)
max_score=max(marks)
min_score=min(marks)
for i in range(len(names)):
    if marks[i]<max_score and marks[i]>min_score:
        max_score=marks[i]
lst=[]        
for j in range(len(names)):
    if marks[j]==max_score:
        lst.append(names[j])
        j=j+1
lst2=sorted(lst)
for i in lst2:
    print(i)
