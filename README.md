# sumchall

---
### Introduction to Computer Science - BU Summer Challenge - Email 0

Greetings Intro to CS Students!

My name is Austin Alexander (please feel free to call me "Austin"), and I will be your instructor for the afternoon BU Summer Challenge session, Introduction to Computer Science. As we'll briefly discuss during our first class, my formal-educational background is both in the humanities/social sciences and in math/computer science. Thus, regardless of your primary academic interests, we should be able to find some common educational ground from which I can help you to learn the fundamentals of computer science. If you already have a bit of CS knowledge under your belts, then I'll do my best to help you add to what you already know.

I am currently a software engineer at [Udacity](https://www.udacity.com/), and, since we'll be using that platform as well the [HackerRank](https://www.hackerrank.com/) platform for programming challenges (by the way, these are two of the most popular tech-education apps in Silicon Valley at the moment), please feel free to create free accounts at both sites so that your progress can be saved, and you can begin to familiarize yourselves with how the different applications work. If either platform seems confusing, don't worry too much; we'll spend a lot of time using the apps in class.

Our session syllabus is [here](https://docs.google.com/document/d/1jpz6JtxZ1sfnagKH1WcAvXeWwDjYBjHYYEej6Wvdqzs/edit?usp=sharing); please keep this link available for reference during the session, as we'll use the links inside the syllabus to navigate to our slide decks during our time together. You'll notice that I'm using Google Docs for as much as possible so that I can update our materials on-the-fly as necessary.

Please feel free to let me know if you have any questions; otherwise, I'll see you later today!

Best,

Austin
s=input().lower().replace(" ","")
alphabet=['a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z']
l=[]
for i in range(len(s)):
    if s[i] in alphabet:
        if s[i] not in l:
            l.append(s[i])
            if len(l)==26:
                print("pangram")
            #else:
            #print("not pangram")


def diff_find(N,K,my_set):
    my_set = sorted(my_set)
    i = 0
    j = 1
    res = 0
    while i < N - 1:
        while j < N - 2:
            m = int(my_set[i]) - int(my_set[j])
            if m == K or -m == K:
                res += 1
                j += 1
            if m > K or -m > K:
                i += 1
                j = i + 1
            else:
                j += 1
        i += 1
    return res

values = input()
inp_list = input()
test = diff_find(int(values.split()[0]),int(values.split()[1]),inp_list.split())
print(test)
