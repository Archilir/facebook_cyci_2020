### Problem C2: Hashtags - Medium (15 points)
In this problem, your job is to identify the most popular hashtags appearing in a set of <img src="https://latex.codecogs.com/png.latex?k"> posts.

The input will describe the posts, with each post given by two lines (and with one blank line between each pair of consecutive posts):
* The first line will consist of a single integer between 0 and 1440 (inclusive), the minute of the day at which the post was made. Multiple posts may have been made at the same time, and the posts will not necessarily be given in order of when they were made.
* The second line will consist of a non-empty string of characters (potentially including spaces), the content of the post.

A **token** is defined as a substring of non-space characters in a post’s content, immediately surrounded on the left and right by either spaces or the beginning/end of the content. Please note that a token may include punctuation. A **hashtag** is then defined as a token beginning with a “#”. It’s guaranteed that no token will include an “#” anywhere after its first character.

Output the single hashtag which **appears** in the **largest number of different posts** (noting that a hashtag appearing multiple times in the same post is counted the same as it appearing a single time in that post). It’s guaranteed that at least one hashtag appears in the input, and that multiple hashtags will not be tied for the largest number of posts. Please note that post timestamps are irrelevant in this version of this problem.

**Constraints**

<img src="https://latex.codecogs.com/png.latex?1\leq\text{}k\leq1000">

**Sample Input**
```
80
This #post has hashtag #b 5 times, #b #b #b #b

0
This is a #post

60
This #post has hashtags #a #b and #c

220
This is for the time #window

200
This #post again has hashtag #b 3 times #b #b but happens in a time #window

210
This #post is for the time #window

220
This is for the time #window

240
Now in this time #window people like talking about windows

20
This is another #post where I say how #happy I am
```
**Sample Output**
```
#post
```