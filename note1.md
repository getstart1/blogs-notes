August 21st, 2018:

I found out that it is not an efficient way to read interview questions for me directly, because they requires deeper understanding and more practice. Try tutorial point first and practice some javaScript coding.


The difficult point is that I don't know which data structure can be used.
map? -- How to construct?
list? -- problem: how to check if an element has appeared or not quickly

I reviewed how to construct hashtable.
Why hashtable? Because the search time for hashtable is O(1). Hashtable is a data structure that helps people to find a specific element fast after storing them.


resource of hashTable in Python: http://interactivepython.org/runestone/static/pythonds/SortSearch/Hashing.html
After running the demo code, I understand that hashTable at least consists of 3 parts: initialize,  insert, get.

After I walk through the answers, I realize that there are much simpler ways to solve this problem. I like the rating system in codeWar. This way, I can choose the top 3 cleverest answer and study them. The way I choose to study is as the following:
1) Use double for loop to check if there are any two characters same as each other.


How to test a javaScript program:
1) Jasmine: one popular javaScript-based unit test library.
    I installed, but I haven't figured out how to
2)  Write a html file and test javaScript code


Review the difference between i++ and ++i


Be careful when using if...else...:
Difference :
```
     function isIsogram(str){
        var i, j;
        for(i = 0; i < str.length; ++i){
            for(j = i+1; j < str.length; ++j){
                if(str[i] === str[j]){
                    return false;
                }
                else{
                    return true;
                }
            }
        }
     }
```

```
function isIsogram(str){
    var i, j;
    str = str.toLowerCase();
    for(i = 0; i < str.length; ++i)
        for(j = i + 1; j < str.length; ++j)
            if(str[i] === str[j])
                return false;
        return true;
}
```

These two functions look so similar, but actually, they are different in the for loop. For the first function, the logic is to compare every pair of two characters. Start with the first pair and end with the last pair. The result should be the same as the first pair. For the second function, it is saying that any one arbitary pair of two same characters, the result would return false. Otherwise, the program returns true.


It is good to remember some terminal shortcut:
control+a： move to the beginning of the line
control+e: move to the end of the line
command+ n: open a new tab
resource: https://support.apple.com/en-nz/guide/terminal/keyboard-shortcuts-trmlshtcts/mac


Reflective thinking:

What I did well:
  1. Be practical by actually write javaScript code and the test cases.

  2. Find different resources to learn about foundations of javaScript and programming logic.

What I can improve:
  1. Maybe next time, I can try to have a rough schedule for myself. Because there are always points that I don't understand. If I keep searching, my progress in general would be very slow. I would not be able to cover all the points that I should cover.

  2. Exploring is also good for me, because coding practice is more straightfoward than theory, so maybe I can do two parts. One practical part, another one theory part.

  3. Time management  
