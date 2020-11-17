# basic-machine-learning-code
/*Here i discribe about the machine learning.
we got a question like from we have apple and orange in my hand. you need to confirm which fruit in right hand.
for that we need to writ a code.
firstly we need to find the different features.
1. weight of apple is below <149 grams. And orange is greater than or equal >=150 grams.
2. The skin of apple is smooth, and orange skin is bumpy.
So we can add feature as weight, and skin softness.
we can use Decision tree to solve this problem.
The fruit which is in right hand is 170 grams and bumpy.
we can take "Smooth"=1, "bumpy"=0. Apple =1, Orange=0.*/

from sklearn import tree
features= [[140,1],[130,1],[150,0],[170,0]]
labels = [1,1,0,0]
clf=tree.DecisionTreeClassifier()
clf=clf.fit(features, labels)
print (clf.predict([[150,0]]))
