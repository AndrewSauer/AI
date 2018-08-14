I want to write a never-ending story.

It's impossible, you might say. One would say that because writers can't keep writing forever, and every story needs a writer.
But if one could mathematically define a writer the story could be defined as an infinite string of characters, which would exist in 
mathspace, even the ones that will never be written down.

2018/8/13 10:24
To do that, I first need to create a program smart enough to contain a rudimentary model of the world, which is necessary to be able to write about
worlds similar to ours. I will fail at this. But I will do it anyway. 

I want to give it an understanding of the English language so I can tell it what I know about our world and train it myself.

I need to create a data structure for concept networks with concepts organized hierarchically and linked together in different ways.

I will paste the first source code I run below.
2018/8/13 10:29

2018/8/13 10:40
Working on source...

def copy(s):
    news=[]
    for i in s:
        news.append(i)
    return news

def split_into_words(s):
    sentences=""
    words=[]
    word=""
    ignorespace=False
    for letter in s:
        if letter==' ' and ignorespace==False:
            words.append(word)
            word=""
        elif letter==' ' and ignorespace==True:
            ignorespace=False
        elif letter==".":
            words.append(word)
            sentences.append(copy(words))
            words=[]
            word=""
            ignorespace=True
        else:
            word+=letter
    return words
def alph_index(letter):
    if ord(letter)>64 and ord_letter<91:
        index=ord(letter)-64
    elif ord(letter)>96 and ord_letter<123:
        index=ord(letter)-96
    return index

vocab=[]

def add_word(word):#vocab is alphebetized
    global vocab
    low=0
    high=len(vocab)

We're going to hold off on commas and such until later. Next on the list to do is finish the alphebetizer.
8/13/2018 10:58
8/14/2018 15:26
After we have an organized list of words, we need some way to connect words to concepts, and concepts to each other.
Matters are complicated by the fact that some words correspond to different concepts in different contexts, while others correspond to no concepts and are simply grammatical.
The magic happens in the description section of the word. It must either say definitively what grammatical class the word is or divide the description into multiple descriptions based on which class. 
8/14/2018 15:29

