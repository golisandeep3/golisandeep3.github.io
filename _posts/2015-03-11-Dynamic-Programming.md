---
layout: post
title: Dynamic Programming
---
Dynamic programming ,one of the optimization technique used in many problems.Many people find it difficult to apply this concept  on various problems.You can find many tutorials online about Dynamic programming,in this article i will be explaining how to apply this concept.Using Dynamic programming you can reduce the complexity of a program from  exponential to polynomial time.There are two Dynamic Programming (DP) approaches one is top to bottom and other is bottom up.Basically you reuse the solutions to the problems that are already solved before.Lets take a problem and see how dynamic programming applies to it.

**Problem Statement**

There is a staircase and there are n steps on it.You can climb either one step or two steps at a time.The problem is in how many ways you can reach nth step.

As you can see ,there are many ways to reach nth step.Lets solve this for

n=1  number of ways =1

n=2  number of ways =2

n=3 number of ways =3

n=4 number of ways =5

...

To reach nth step number of ways = numbersofways(n-1) + numberofways(n-2).
How did we get this relation? Its easy to reach nth step either you have to come from n-1th step or n-2th step.

int numofways(int n)
{
if(n==1)
return 1;
if(n==2)
return 2;

return numofways(n-1)+numofways(n-2);
}
what is the problem with above problem? Here you are solving the same problem again and again.

n=5    you are solving  n=4, n=2

n=3    you are solving n=2,n=1

As you can see n=2 is repeated.So what is the best way to solve this problem? You guessed it right.. . store the previously computed results.

int numofways(int n)
{
int num[] = new int[n+1];
num[1]=1;
num[2]=2;
for(int i=3;i<=n;i++)
num[i]=num[i-1]+num[i-2];

return num[n];
}
Yahooooooo.. you mastered the Dynamic programming technique..
Let me give you some tips on it.

**Tip 1:**

First write a recurrence relation for your problem .For a problem of size n ,write in terms of problems of smaller sizes ,then you store results in an array either one dimensional or  two dimensional  depending on the problem.

**Tip 2:**

Practice a lot of problems.Don't worry about Dynamic programming ,first solve using recursion.

**Tip 3:** 

These problems are similar to permutations and combinations,try solving some math problems which involves counting ,so that you tune your mind to those problems
