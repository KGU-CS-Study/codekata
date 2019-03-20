Codekata(http://codekata.com/)
-------------------------------------------
How do you get to be a great musician? It helps to know the theory, and to understand the mechanics of your instrument. 
It helps to have talent. 
But ultimately, greatness comes from practicing; 
applying the theory over and over again, using feedback to get better every time.

How do you get to be an All-Star sports person? Obviously fitness and talent help. 
But the great athletes spend hours and hours every day, practicing.

But in the software industry we take developers trained in the theory and throw them straight in to the deep-end, working on a project. 
It’s like taking a group of fit kids and telling them that they have four quarters to beat the Redskins (hey, we manage by objectives, right?). 
In software we do our practicing on the job, and that’s why we make mistakes on the job. 
We need to find ways of splitting the practice from the profession. 
We need practice sessions.

## Codekata 번역
어떻게 하면 위대한 음악가가 될 수 있을까? - 이론을 이해하고, 악기의 메카니즘을 이해하며 재능이 있으면 위대한 음악가가 되는데 도움이 될 수는 있다.
하지만, 궁극적으로는 위대한 음악가가 되기 위해선 거듭해서 연습해야 한다.(매번 더 나은 연주를 하기 위해 끝없이 채찍질 해야한다.)

올스타 스포츠맨이 되려면 어떻게 해야 할까? - 좋은 체력과 재능은 스포츠맨이 되는데 도움이 될 수는 있다. 하지만, 정말 위대한 운동 선수들은
하루에도 수 시간을 연습한다.

그러나, 소프트웨어 산업에서 우리는 이론 교육을 받은 개발자들을 데리고 프로젝트에 참여하면서 곧바로 어려운 구현 부분을 맡기곤 한다.
이런 일은 어린이들을 데리고 위대한 스포츠 선수를 이길 수 있다고 하는 것과 같다.(단순히, 목표만 정해서 관리하는 것인가??..)

소프트웨어를 개발함에 있어서 자꾸 실수하는 이유는 연습이라고 불릴만한 것은 하지 않고, 일을 연습삼아 하기 때문이다.

**우리는 반드시 직업의 일과 연습을 분리하는 방법을 찾아야 한다. 즉, 별도의 피나는 연습이 필요하다.**

# The Kata
What makes a good practice session? You need time without interruptions, and a simple thing you want to try. 
You need to try it as many times as it takes, and be comfortable making mistakes. 
You need to look for feedback each time so you can work to improve. 
There needs to be no pressure: 
this is why it is hard to practice in a project environment. 
it helps to keep it fun: make small steps forward when you can. 
Finally, you’ll recognize a good practice session because you’ll came out of it knowing more than when you went in.

Code Kata is an attempt to bring this element of practice to software development. 
A kata is an exercise in karate where you repeat a form many, many times, making little improvements in each. 
The intent behind code kata is similar. 
Each is a short exercise (perhaps 30 minutes to an hour long). 
Some involve programming, and can be coded in many different ways. 
Some are open ended, and involve thinking about the issues behind programming. 
These are unlikely to have a single correct answer. 
I add a new kata every week or so. Invest some time in your craft and try them.

Remember that the point of the kata is not arriving at a correct answer. 
The point is the stuff you learn along the way. The goal is the practice, not the solution.

## The Kata 번역
그렇다면, 무엇이 좋은 연습이 될까? 시간을 내서 간단한 것을 만들어 보는 것이 좋은 연습이 된다.

이 연습(Kata)를 필요한 만큼 여러 번 시도하고 편안하게 실수해야 한다.  그리고 개선할 수 있는 피드백도 반드시 필요하다. 아무런 압력이 없어야 한다. 이것이 프로젝트 환경 즉, 업무 환경에서는 실행하기 어려운 이유이다.(실수해도 여러번 시도할 수 없고, 피드백도 없는 환경이 대부분이기 때문에)
가능한 작은 요구사항들로 정의된 연습부터 시작해야 한다. 결과적으로 이러한 과정들은 훌륭한 개발자가 되는 밑거름이 된다.  

코드카타(Code Kata)는 이러한 실천 요소를 소프트웨어를 개발하는 것에 적용하려는 시도이다. 카타(Kata)란 가라데에서 운동을 하며, 여러 번 반복하여 기술의 방식을 조금씩 개선하는 방법을 말한다.
CodeKata도 이런 방식과 비슷하다.  
각각 짧은 운동이다(아마도 30분 ~ 1시간 정도 소요될 수 있다.). 일부는 여러 가지 방법으로 코딩 될 수 있다. 이런 개방된 연습은 프로그래밍의 뒤에 실제 문제에 대하여 생각해 볼 수 있는 좋은 기회가 된다.
**모든 카타는 하나의 정답을 가지지 않는다.**

매주 새 카타를 추가해야 하며, 만들어 놓은 것에 시간을 투자하고 새로운 시도를 해봐야 한다.

Kata의 관점에서는 정확한 정답을 찾지 못한다는 것을 항상 기억해야 한다.(정답을 찾으려 하지 말고 방법과 다양한 시도에 집중하자)  
요점은 우리가 배우는 방식을 터득하는 것이다. 목표는 실천이라는 것을 항상 기억하고 또 기억해라.

# How It Started
(This is a long one. It explains how I discovered that something I do almost every day to improve my coding is actually a little ritual that has much in common with practice in the martial arts…)

This all starts with RubLog, some blogging software I once wrote. I wanted to experiment how it does searching (but this isn’t an article about searching, or about bit twiddling. Trust me). Because I eventually wanted to use cosine-based comparisons to find similar articles, I build vectors mapping word occurrences to each document in the blog. I basically ended up with a set of 1,200-1,500 bits for each document. To implement a basic ranked search, I needed to be able to perform a bitwise AND between each of these vectors and a vector containing the search terms, and then count the number of one-bits in the result.

I had a spare 45 minutes last night (I took Zachary to his karate lesson, but there was no room in the parent’s viewing area), so I thought I’d play with this. First I tried storing the bit vectors different ways: it turns out (to my surprise) that storing them as an array of fixnums has almost exactly the same speed as storing them as the bits in a bignum. (Also, rather pleasingly, changing between the two representations involves altering just two lines of code). Because it marshals far more compactly, I decided to stick with the bignum.

Then I had fun playing with the bit counting itself. The existing code uses the obvious algorithm:

```javascript
max_bit.times { |i| count += word[i] }
```
Just how slow was this? I wrote a simple testbed that generated one hundred 1,000 bit vectors, each with 20 random bits set, and timed the loop. For all 100, it took about .4s.

Then I tried using the ‘divide-and-conquer’ counting algorithm from chapter 5 of Hacker’s Delight (modified to deal with chunking the Bignum into 30-bit words).
```javascript
((max_bit+29)/30).times do |offset|
  x = (word >> (offset*30)) & 0x3fffffff
  x = x - ((x >> 1) & 0x55555555)
  x = (x & 0x33333333) + ((x >> 2) & 0x33333333)
  x = (x + (x >> 4)) & 0x0f0f0f0f;
  x = x + (x >> 8)
  x = x + (x >> 16)
  count += x & 0x3f
end
```
This ran about 2.5 times faster that the naive algorithm.

Then I realized that when I was comparing a set of search times with just a few words in it, the bit vector would be very sparse. Each chunk in the loop above would be likely to be zero. So I added a test:
```javascript
((max_bit+29)/30).times do |offset|
  x = (word >> (offset*30)) & 0x3fffffff
  next if x.zero?
  x = x - ((x >> 1) & 0x55555555)
  x = (x & 0x33333333) + ((x >> 2) & 0x33333333)
  x = (x + (x >> 4)) & 0x0f0f0f0f;
  x = x + (x >> 8)
  x = x + (x >> 16)
  count += x & 0x3f
end
```
Now I was seven times faster than the original. But my testbed was using vectors containing 20 set bits (out of 1,000). I changed it to generate timings with vectors containing 1, 2, 5, 10, 20, 100, and 900 set bits. This got even better: I was up to a factor of 15 faster with 1 or 2 bits in the vector.

But if I could speed things up this much by eliminating zero chunks in the bit-twiddling algorithm could I do the same in the simple counting algorithm? I tried a third algorithm:
```javascript
((max_bit+29)/30).times do |offset|
   x = (word >> (offset*30)) # & 0x3fffffff
   next if x.zero?
   30.times {|i| count += x[i]}
 end
 ```
The inner loop here is the same as for the original count, but I now count the bits in chunks of 30.

This code performs identically to the bit-twiddling code for 1 set bit, and only slightly worse for 2 set bits. However. once the number of bits starts to grow (past about 5 for my given chunk size), the performance starts to tail off. At 100 bits it’s slower than the original naive count.

So for my particular application, I could probably chose either of the chunked counting algorithms. Because the bit twiddling one scales up to larger numbers of bits, and because I’ll need that later on if I ever start doing the cosine-based matching of documents, I went with it.

So what’s the point of all this?

Yesterday I posted a blog entry about the importance of verbs. It said “Often the true value of a thing isn’t the thing itself, but instead is the activity that created it.” Chad Fowler picked this up and wrote a wonderful piece showing how this was true for musicians. And Brian Marick picked up of Chad’s piece to emphasize the value of practice when learning a creative process.

At the same time, Andy and I had been discussing a set of music tapes he had. Originally designed to help musicians practice scales and arpeggios, these had been so popular that they now encompassed a whole spectrum of practice techniques. We were bemoaning the fact that it seemed unlikely that we’d be able to get developers to do the same: to buy some aid to help them practice programming. We just felt that practicing was not something that programmers did.

Skip forward to this morning. In the shower, I got to thinking about this, and realized that my little 45 minute exploration of bit counting was actually a practice session. I wasn’t really worried about the performance of bit counting in the blog’s search algorithm; in reality it comes back pretty much instantaneously. Instead, I just wanted to play with some code and experiment with a technique I hadn’t used before. I did it in a simple, controlled environment, and I tried many different variations (more than I’ve listed here). And I’ve still got some more playing to do: I want to mess around with the effect of varying the chunk size, and I want to see if any of the other bit counting algorithms perform faster.

What made this a practice session? Well, I had some time without interruptions. I had a simple thing I wanted to try, and I tried it many times. I looked for feedback each time so I could work to improve. There was no pressure: the code was effectively throwaway. It was fun: I kept making small steps forward, which motivated me to continue. Finally, I came out of it knowing more than when I went in.

Ultimately it was having the free time that allowed me to practice. If the pressure was on, if there was a deadline to delivery the blog search functionality, then the existing performance would have been acceptable, and the practice would never have taken place. But those 45 pressure-free minutes let me play.

So how can we do this in the real world? How can we help developers do the practicing that’s clearly necessary in any creative process? I don’t know, but my gut tells me we need to do two main things.

The first is to take the pressure off every now and then. Provide a temporal oasis where it’s OK not to worry about some approaching deadline. It has to be acceptable to relax, because if you aren’t relaxed you’re not going to learn from the practice.

The second is to help folks learn how to play with code: how to make mistakes, how to improvise, how to reflect, and how to measure. This is hard: we’re trained to try to do things right, to play to the score, rather than improvise. I suspect that success here comes only after doing.

So, my challenge for the day: see if you can carve out 45 to 60 minutes to play with a small piece of code. You don’t necessarily have to look at performance: perhaps you could play with the structure, or the memory use, or the interface. In the end it doesn’t matter. Experiment, measure, improve.

Practice.


## How It Started 번역

이것은 길다. 이것은 내가 코딩을 향상시키기 위해 거의 매일하는 일이 실제로 무술연습과 공통점이 있는 작은 점이라는 것을 발견한것을 설명한다.
이것은 RubLog 로 부터 시작되어진다. 나는 그것이 어떻게 검색되어 지는지 실험하고 싶었다.
(그러나 이거는 검색에 대한 기사나 칼럼이 아니니 나를 믿어라)

나는 코사인 기반의 비교를 사용하여 비슷한 기사를 찾고 싶었서, 나는 벡터 단어 맵핑 발생을 도큐먼트 블로그로 만들었다.

기본적으로 각 문서에 대해 1200 ~ 1500 비트를 설정하였다.
서치의 기본 랭킹을 향상시키기 위해 나는 조건에 포함된 벡터와 벡터 각각의 비트 단위 AND 를 수행한 다음 결과에서 1 비트수를 계산할 수 있어야 했다.

나는 지난밤에 45분을 보냈다. (나는 Zachary 의 카라테 레슨을 보았다 그러나 그 방에는 부모님이 지켜보는 방이 업었다.)
그래서 나는 생각했다 이것을 가지고 놀면 되겠따고

첫번째로 나는 비트벡터를 다른 방법으로 쌓는것을 시도했다.
내가 발견한것은 (놀랍게도) fixnums 의 쌓는 방법의 속도가 bignum 의 속도와 거의 비슷하다는 것이다.

왜냐하면 그것은 더 정밀하게 정리하기 떄문에 나는 bignum 을 결정하였습니다.

그 다음 나는 비트 카운팅 이것 스스로 더 재미있게 놀았다. 기존 의 명백한 코드를 사용하면서.

```javascript
max_bit.times { |i| count += word[i] }
```

이게 얼마나 느린거야? 저는 각각 1,000 개의 비트 벡터를 생성하는 간단한 테스트 베드를 작성했습니다. 각각의 비트 벡터는 20 개의 랜덤 비트 세트로 구성되어 있으며 루프를 타임 아웃했습니다. 100 명 모두에게 약 0.4 초가 걸렸습니다.

그런 다음 Hacker 's Delight 5 장의 'divide-and-conquer'계산 알고리즘을 사용하여 시도했습니다 (Bignum을 30 비트 단어로 청크 처리하도록 수정 됨).

```javascript
((max_bit+29)/30).times do |offset|
  x = (word >> (offset*30)) & 0x3fffffff
  x = x - ((x >> 1) & 0x55555555)
  x = (x & 0x33333333) + ((x >> 2) & 0x33333333)
  x = (x + (x >> 4)) & 0x0f0f0f0f;
  x = x + (x >> 8)
  x = x + (x >> 16)
  count += x & 0x3f
end
```
이것은 순진 알고리즘보다 약 2.5 배 빠릅니다.

그런 다음 검색 시간을 단어 몇 개와 비교할 때 비트 벡터가 매우 희박하다는 것을 알았습니다. 위 루프의 각 청크는 0 일 가능성이 높습니다. 그래서 나는 테스트를 추가했다 :

```javascript
(max_bit+29)/30).times do |offset|
  x = (word >> (offset*30)) & 0x3fffffff
  next if x.zero?
  x = x - ((x >> 1) & 0x55555555)
  x = (x & 0x33333333) + ((x >> 2) & 0x33333333)
  x = (x + (x >> 4)) & 0x0f0f0f0f;
  x = x + (x >> 8)
  x = x + (x >> 16)
  count += x & 0x3f
end
```

이제는 원래보다 7 배 빠릅니다. 그러나 테스트 베드는 20 비트 (1,000 개 중)를 포함하는 벡터를 사용하고있었습니다. 1, 2, 5, 10, 20, 100 및 900 세트 비트를 포함하는 벡터로 타이밍을 생성하도록 변경했습니다. 이것은 더 나아졌습니다 : 저는 벡터에서 1 또는 2 비트로 15 배 빨랐습니다.

그러나 비트 - 트 와이들 링 알고리즘에서 제로 청크를 제거하여 이처럼 많은 것을 빠르게 할 수 있다면 간단한 계산 알고리즘에서도 동일한 작업을 수행 할 수 있습니까? 나는 세 번째 알고리즘을 시도했다.

```javascript
((max_bit+29)/30).times do |offset|
   x = (word >> (offset*30)) # & 0x3fffffff
   next if x.zero?
   30.times {|i| count += x[i]}
 end
```

여기에있는 내부 루프는 원래 카운트와 동일하지만 이제는 30 비트로 계산됩니다.

이 코드는 1 세트 비트에 대해 비트 - 트 와이들 링 코드와 동일하게 수행되며 2 비트 세트에 대해서만 약간 나빠집니다. 하나. 일단 비트 수가 증가하기 시작하면 (주어진 청크 크기에 대해 5를 지나면) 성능이 떨어지게됩니다. 100 비트에서 원래의 순진 횟수보다 느립니다.

따라서 특정 응용 프로그램의 경우 청크 계산 알고리즘 중 하나를 선택했을 수 있습니다. 조금씩 움직이는 비트가 더 많은 비트로 확장되기 때문에 나중에 코사인 기반 문서 매칭을 시작하면 나중에 필요하기 때문에 함께 갈 것입니다.

- 그래서 여기에서 포인트는 무엇일까?!

어제 나는 동사의 중요성에 관한 블로그 글을 올렸다. "종종 물건의 진정한 가치는 그 자체가 아니라 창조 한 활동입니다."채드 파울러 (Chad Fowler)는 이것을 받아 들여 이것이 음악가들에게 어떻게 적용되는지 보여주는 멋진 작품을 썼습니다. 브라이언 마릭 (Brian Marick)은 창작 과정을 배울 때 연습의 가치를 강조하기 위해 차드 (Chad)의 작품을 골랐습니다.

동시에 Andy와 나는 그가 갖고있는 일련의 음악 테이프에 대해 토론하고있었습니다. 원래 뮤지션들이 스케일과 아르페지오를 연습 할 수 있도록 디자인 되었기 때문에 매우 인기가있어서 이제는 전체 스펙트럼의 연습 테크닉을 포함하고 있습니다. 우리는 개발자들이 프로그래밍을 수행하는 데 도움이되는 약간의 원조를 구입하는 것과 같은 것을 할 수는 없을 것 같았습니다. 우리는 단지 연습이 프로그래머가하는 것이 아니라고 생각했습니다.

오늘 아침으로 건너가서, 소나기 속에서 나는 이것에 대해서 생각했다. 그리고 나의 작은 45분의 비트 카운트의 대한 탐사가 정확하게 연습하는 시간이라는 것을.
나는 결코 블로그의 서치알고리즘의 비트 카운트의성능에 대해서 걱정하지 않았습니다.

실제로 금방 돌아옵니다. 대신에 나는 지금까지 사용하지 않았던 몇명 기술로 몇가지 코드와 실험을 하고 싶었습니다.
그것을 단순하고 통제된 환경에서 그리고 나느 다른 많은 변수들을 실행했습니다.

그리고 나는 여전히 더 해야할 것들이 있습니다. 나는 청크 크기를 변화시키는 효과를 가지고 혼란스러워하고 싶다. 그리고 나는 다른 비트 계산 알고리즘 중 어떤 것이 더 빨리 수행되는지보고 싶다.

무엇이 이것을 연습 세션으로 만들었습니까?  
글쎄, 나는 방해받지 않고 약간의 시간을 보냈다.   
시도하고 싶었던 간단한 일을 여러 번 시도했습니다.   
개선 할 수 있도록 매번 피드백을 찾았습니다.  
압력은 없었습니다. 코드는 효과적으로 폐기되었습니다. 즐거웠습니다   
: 나는 계속 앞으로 나아가는 작은 발걸음을 내디뎠다. 마침내, 내가 들어갔을 때보다 더 많이 알게되었습니다.  

궁극적으로 이것은 나에게 연습하는 것에 대한 자유시간을 주었습니다.  
만약 블로그 서치 기능에 대해서 데드라인과 압박이 잇었다면 그 기존의 성능 그대로 받아들여 졌을것입니다.
그러나 나에게 자유스러운 45분에 있어서 그것이 잇었습니다.

그래서 현실세계에서 어떻게 할 수 있을까?
개발자가 어떻게 창조적인 프로세스에서 분명히 필요한 연습을 도울 수 있을까?
나도 잘은 모르지만, 나는 내가 느낀 것들은 나에게 우리가 해야할 2가지를 말해주고 있다.

첫번째는 압박을 받으면 안된다는 것이다. 마감기한이 다가오지 않은 일시적인 오아시스 같은 환경을 제공해라.
이것은 편안하게 해준다 만약 너가 편안하지 않다면 너는 연습을 통해서 배우지 못할 것이기 떄문입니다.

두번째는 코드를 가지고 노는법을 배우는 것입니다.

실수를 하는 방법, 향상시키는 방법, 반영하는 방법, 그리고 측정하는 방법
이것은 어렵습니다. 
:우리가 올바르게 훈련하는 방법으로 향상시키는 것보다 점수를 내는거라고 배웠습니다.
나는 성공은 단지 무언가를 한 후에 일어난다고 생각합니다.

그래서 나의 당일 도전과제로 :
작은 코드로 45~60분 정도 연스할 수 있는지 확인을 하세요.
당신이 성능을 봐야할 필요는 없습니다.
아마도 너는 구조를 다루거나, 메모리를 사용하거나, 추상화를 할 수 있습니다. 그것은 실험, 측정, 개선 은 결코 중요하지 않습니다.



# index
[Kata01-Supermarket Pricing](/01-Supermarket\ pricing/)  
