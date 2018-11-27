# SparkProject

## About Me and the Objective of our Project

I am Naresh Vunnam pursuing my masters at Northwest missouri state university. This project is a part of my "BigData" course. For this project the objective is to find the most commonly used words in a dataset. I have used spark for doing this project.

## Dataset Story:
I have taken the laila majnu stoty as my dataset. I created a text file named as laila_majnu.txt where I copied the whole content from the website showed in the below link to a text file. I used this dataset to find the wordcount.

Source : https://www.theholidayspot.com/valentine/stories/laila_majnu.htm 

## Commands Used:

```
> val inputFile = sc.textFile("C:/44517/titanic_sample/titanic.txt")
```

```
>val counts = inputFile.flatMap(line => line.split(" ")).map(word => (word,1)).reduceByKey(_ + _);
```

```
> counts.saveAsTextFile("c:/tmp/show-spark/output")
```

## Results

This is the result obtained by using the above commands  

| Word    | Count|
|---------|------|
| and     | 22   |
| the     | 22   |
| in      | 19   |
| to      | 19   |
| a       | 17   |
| love    | 14   |
| and     | 51   |
| for     | 11   |
| her     | 11   |
| of      | 11   |
| was     | 10   |

Here we can see that the most commonly repeated word is "and" and "the" which is used  like 22 times each. Here is Bar graph view for the above results.

### Result represented in bar graphs:  
![sparkgraph](https://user-images.githubusercontent.com/31740220/49095327-d96c3e80-f22d-11e8-873a-9c3a67a5e4b6.JPG) 
 

## References:

1.https://github.com/S530484/Spark_wordcount/blob/master/README.md
