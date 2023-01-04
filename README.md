# **160 Coding Interview Questions with Solutions**
[![Ask Me Anything !](https://img.shields.io/badge/Ask%20me-anything-1abc9c.svg)](https://GitHub.com/Naereen/ama)
[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)
[![Documentation Status](https://readthedocs.org/projects/ansicolortags/badge/?version=latest)](http://ansicolortags.readthedocs.io/?badge=latest)

- [Two Number Sum](#two-number-sum)


## Two Number Sum
> Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

> You may assume that each input would have exactly one solution, and you may not use the same element twice.

> You can return the answer in any order.

>Input: nums = [2,7,11,15], target = 9
Output: [0,1]

> Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].

> Follow-up: Can you come up with an algorithm that is less than O(n2) time complexity?


```python
#O(n^2) time | O(1) space
def twoNumberSum(array,targetSum):
    for i in range(len(array)-1):
        firstNum=array[i]
        for j in range(i+1,len(array):
            secondNum=array[j]
            if firstNum+ secondNum==targetNum:
                return [firstNum,secondNum]
    return []

# O(n) time | O(n) space
def twoNumberSum(array,targetSum):
    nums={}
    for num in array:
        potentialMatch=targetSum - num
        if targetMatch in nums:
            return [targetSum-num,num]
        else:
            nums[num]=True
    return []
        
# O(n) time | O(n) space
def twoNumberSum(array,targetSum):
    array.sort()
    left = 0
    right = len(array) -1 
    while left < right:
        currrentSum = array[left]+array[right]
        if currentSum == targetSum:
            return array[left],array[right]
        elif currentSum < targetSum:
            left +=1
        elif currentSum > targetSum:
            right -=1


```