{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 177,
   "id": "7587b674",
   "metadata": {},
   "outputs": [],
   "source": [
    "from itertools import permutations ,combinations\n",
    "A = ['1','2','3','4']\n",
    "B = ['a','b','c','d']\n",
    "C = ['a','1','@','boy']"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 178,
   "id": "c4aadce0",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[('1', '2', '3', '4'), ('1', '2', '4', '3'), ('1', '3', '2', '4'), ('1', '3', '4', '2'), ('1', '4', '2', '3'), ('1', '4', '3', '2'), ('2', '1', '3', '4'), ('2', '1', '4', '3'), ('2', '3', '1', '4'), ('2', '3', '4', '1'), ('2', '4', '1', '3'), ('2', '4', '3', '1'), ('3', '1', '2', '4'), ('3', '1', '4', '2'), ('3', '2', '1', '4'), ('3', '2', '4', '1'), ('3', '4', '1', '2'), ('3', '4', '2', '1'), ('4', '1', '2', '3'), ('4', '1', '3', '2'), ('4', '2', '1', '3'), ('4', '2', '3', '1'), ('4', '3', '1', '2'), ('4', '3', '2', '1')]\n"
     ]
    },
    {
     "data": {
      "text/plain": [
       "24"
      ]
     },
     "execution_count": 178,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "per_A=list(permutations(A)) #will give all permutation possible pf list A\n",
    "print(per_A)\n",
    "len(per_A)   #number of permutation of list A"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 179,
   "id": "320e5c9b",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[('1', '2'), ('1', '3'), ('1', '4'), ('2', '1'), ('2', '3'), ('2', '4'), ('3', '1'), ('3', '2'), ('3', '4'), ('4', '1'), ('4', '2'), ('4', '3')]\n"
     ]
    },
    {
     "data": {
      "text/plain": [
       "12"
      ]
     },
     "execution_count": 179,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "per_A1=list(permutations(A,2)) #will give 2- permutation possible pf list A\n",
    "print(per_A1)\n",
    "len (per_A1)   #number of 2-permutation of list A"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 180,
   "id": "cc513e36",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[('a', 'b', 'c', 'd'), ('a', 'b', 'd', 'c'), ('a', 'c', 'b', 'd'), ('a', 'c', 'd', 'b'), ('a', 'd', 'b', 'c'), ('a', 'd', 'c', 'b'), ('b', 'a', 'c', 'd'), ('b', 'a', 'd', 'c'), ('b', 'c', 'a', 'd'), ('b', 'c', 'd', 'a'), ('b', 'd', 'a', 'c'), ('b', 'd', 'c', 'a'), ('c', 'a', 'b', 'd'), ('c', 'a', 'd', 'b'), ('c', 'b', 'a', 'd'), ('c', 'b', 'd', 'a'), ('c', 'd', 'a', 'b'), ('c', 'd', 'b', 'a'), ('d', 'a', 'b', 'c'), ('d', 'a', 'c', 'b'), ('d', 'b', 'a', 'c'), ('d', 'b', 'c', 'a'), ('d', 'c', 'a', 'b'), ('d', 'c', 'b', 'a')]\n"
     ]
    },
    {
     "data": {
      "text/plain": [
       "24"
      ]
     },
     "execution_count": 180,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    " per_B=list(permutations(B)) #will give all permutation possible pf list B\n",
    "print(per_B)\n",
    "len(per_B) #number of permutation of list B"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 181,
   "id": "72288370",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[('a', 'b'), ('a', 'c'), ('a', 'd'), ('b', 'a'), ('b', 'c'), ('b', 'd'), ('c', 'a'), ('c', 'b'), ('c', 'd'), ('d', 'a'), ('d', 'b'), ('d', 'c')]\n"
     ]
    },
    {
     "data": {
      "text/plain": [
       "12"
      ]
     },
     "execution_count": 181,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "per_B1=list(permutations(B,2)) #will give 2-permutation possible pf list B\n",
    "print(per_B1)\n",
    "len(per_B1) #number of 2- permutation of list B"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 182,
   "id": "0372e89c",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[('a', '1', '@', 'boy'), ('a', '1', 'boy', '@'), ('a', '@', '1', 'boy'), ('a', '@', 'boy', '1'), ('a', 'boy', '1', '@'), ('a', 'boy', '@', '1'), ('1', 'a', '@', 'boy'), ('1', 'a', 'boy', '@'), ('1', '@', 'a', 'boy'), ('1', '@', 'boy', 'a'), ('1', 'boy', 'a', '@'), ('1', 'boy', '@', 'a'), ('@', 'a', '1', 'boy'), ('@', 'a', 'boy', '1'), ('@', '1', 'a', 'boy'), ('@', '1', 'boy', 'a'), ('@', 'boy', 'a', '1'), ('@', 'boy', '1', 'a'), ('boy', 'a', '1', '@'), ('boy', 'a', '@', '1'), ('boy', '1', 'a', '@'), ('boy', '1', '@', 'a'), ('boy', '@', 'a', '1'), ('boy', '@', '1', 'a')]\n"
     ]
    },
    {
     "data": {
      "text/plain": [
       "24"
      ]
     },
     "execution_count": 182,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#will give all permutation possible pf list C\n",
    "per_C=list(permutations(C))\n",
    "print(per_C)\n",
    "len(per_C) #number of permutation of list C"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 187,
   "id": "fd4228e3",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[('1', '2', '3', '4')]\n"
     ]
    },
    {
     "data": {
      "text/plain": [
       "1"
      ]
     },
     "execution_count": 187,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "com_A= list(combinations(A,4)) #will give all combinations possible pf list A\n",
    "print(com_A)\n",
    "len(com_A) #number of combinations of list A"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 186,
   "id": "ceb10045",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[('1', '2'), ('1', '3'), ('1', '4'), ('2', '3'), ('2', '4'), ('3', '4')]\n"
     ]
    },
    {
     "data": {
      "text/plain": [
       "6"
      ]
     },
     "execution_count": 186,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "com_A1= list(combinations(A,2)) #will give 2-combinations possible pf list A\n",
    "print(com_A1)\n",
    "len(com_A1)  #number of 2-combinations of list A"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 188,
   "id": "d3f6a27d",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[('a', 'b', 'c', 'd')]\n"
     ]
    },
    {
     "data": {
      "text/plain": [
       "1"
      ]
     },
     "execution_count": 188,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "com_B=list(combinations(B,4))  #will give all combinations possible pf list B\n",
    "print(com_B)\n",
    "len(com_B)  #number of combinations of list B"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 189,
   "id": "f8d71068",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[('a', 'b'), ('a', 'c'), ('a', 'd'), ('b', 'c'), ('b', 'd'), ('c', 'd')]\n"
     ]
    },
    {
     "data": {
      "text/plain": [
       "6"
      ]
     },
     "execution_count": 189,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "com_B1=list(combinations(B,2))  # will give 2-combinations possible pf list B\n",
    "print(com_B1)\n",
    "len(com_B1)   #number of 2-combinations of list B"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 185,
   "id": "1a2c8840",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[('a', '1', '@', 'boy')]\n"
     ]
    },
    {
     "data": {
      "text/plain": [
       "1"
      ]
     },
     "execution_count": 185,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#will give all combinations possible pf list C\n",
    "com_C=list(combinations(C,4))\n",
    "print(com_C)\n",
    "len(com_C)  #number of combinations of list C"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "04c02c15",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.8.8"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
