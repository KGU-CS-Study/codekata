[Kata01 : Karate Chop](http://codekata.com/kata/kata02-karate-chop/)
-------------------------------

Binarh chop(흔히 이진 검색이라고 알려진)은 정렬된 배열에서 탐색하고자 하는 값의 위치를 찾는 방법 중 하나이다. 한번 조사할 때마다 탐색 범위가 반으로 줄어 효율성을 극대화 시킨다.(첫 번째 패스에서 탐색하는 값이 키값 기준으로 배열의 뒤에 있는지 앞에 있는지 결정한다. 두 번째 패스에서는 탐색하는 값이 있는 배열만 검색하고 나머지 절반은 버린다. 탐색하는 값을 찾거나 검색할 배열이 없는 경우 중지한다.)


This Kata is straightforward. Implement a binary search routine (using the specification below) in the language and technique of your choice. Tomorrow, implement it again, using a totally different technique. Do the same the next day, until you have five totally unique implementations of a binary chop. (For example, one solution might be the traditional iterative approach, one might be recursive, one might use a functional style passing array slices around, and so on).

## Goal

This Kata has three separate goals:  
```이  카타는 세가지 목표를 갖습니다 :```


1. As you’re coding each algorithm, keep a note of the kinds of error you encounter. A binary search is a ripe breeding ground for “off by one” and fencepost errors. As you progress through the week, see if the frequency of these errors decreases (that is, do you learn from experience in one technique when it comes to coding with a different technique?).  
```각 알고리즘을 코딩할때, 당신이 마주하는 에러의 종류를 적으세요. 바이너리 서치는 전신주 램프에러라고도 합니다. 일주일 동안 진행을 하면서, 오류의 빈도가 감소하는지 확인하세요 (즉, 너가 한가지 다른 기술로 코딩할 떄마다 다른 하나를 배웁니다.)```

2. What can you say about the relative merits of the various techniques you’ve chosen? Which is the most likely to make it in to production code? Which was the most fun to write? Which was the hardest to get working? And for all these questions, ask yourself “why?”.  
```너가 선택한 다양한 기술들 중에서 장점이 무엇인지 말 할 수 있나요? 무엇이 프로덕션 코드에 가장 근접한가요? 어떤 방법이 가장 재미있었고, 어떤 방버이 코딩하기에 가장 어려웠나요? 그리고 너에게 계속해서 질문하세요 왜? 라고  ```

3. It’s fairly hard to come up with five unique approaches to a binary chop. How did you go about coming up with approaches four and five? What techniques did you use to fire those “off the wall” neurons?  
``` binary chop 에 접근하기 위한 유니크한 5가지 접근법을 제시하는것은 어렵습니다. 4번째랑 5번째에 접근하기 위해 어떻게 했었나요? 마지막에 떨어지는 비트를 얻기 위한 사용한 방법은 무엇인가요?? ```


## Specification
Write a binary chop method that takes an integer search target and a sorted array of integers. It should return the integer index of the target in the array, or -1 if the target is not in the array. The signature will logically be:

```ruby
chop(int, array_of_int)  -> int
```
You can assume that the array has less than 100,000 elements. For the purposes of this Kata, time and memory performance are not issues (assuming the chop terminates before you get bored and kill it, and that you have enough RAM to run it).

## Test Data
Here is the Test::Unit code I used when developing my methods. Feel free to add to it. The tests assume that array indices start at zero. You’ll probably have to do a couple of global search-and-replaces to make this compile in your language of choice (unless your enlightened choice happens to be Ruby).

```ruby
def test_chop
  assert_equal(-1, chop(3, []))
  assert_equal(-1, chop(3, [1]))
  assert_equal(0,  chop(1, [1]))
  #
  assert_equal(0,  chop(1, [1, 3, 5]))
  assert_equal(1,  chop(3, [1, 3, 5]))
  assert_equal(2,  chop(5, [1, 3, 5]))
  assert_equal(-1, chop(0, [1, 3, 5]))
  assert_equal(-1, chop(2, [1, 3, 5]))
  assert_equal(-1, chop(4, [1, 3, 5]))
  assert_equal(-1, chop(6, [1, 3, 5]))
  #
  assert_equal(0,  chop(1, [1, 3, 5, 7]))
  assert_equal(1,  chop(3, [1, 3, 5, 7]))
  assert_equal(2,  chop(5, [1, 3, 5, 7]))
  assert_equal(3,  chop(7, [1, 3, 5, 7]))
  assert_equal(-1, chop(0, [1, 3, 5, 7]))
  assert_equal(-1, chop(2, [1, 3, 5, 7]))
  assert_equal(-1, chop(4, [1, 3, 5, 7]))
  assert_equal(-1, chop(6, [1, 3, 5, 7]))
  assert_equal(-1, chop(8, [1, 3, 5, 7]))
end
```