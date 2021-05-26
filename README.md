# NCBO-REST-Annotator
Java application for using BioPortal annotator locally in the console

## Sources

The program has been implemented according to the documentation:
http://data.bioontology.org/documentation

Inspirated by:
https://github.com/ncbo/ncbo_rest_sample_code

Also noteworthy - REST API example in R:
https://github.com/muntisa/RNCBO

Example URL for GET:
https://data.bioontology.org/annotator?text=My+biomedical+text+for+annotation

## Sample use (run in /src dir; with examples below):

1. Just plain text, with standard API key - output in console

```java
java -classpath ".;../lib/*" AnnotateText <text to anotate>
java -classpath ".;../lib/*" AnnotateText "Cancer is a group of diseases involving abnormal cell growth with the potential to invade or spread to other parts of the body"
```

2. Plain text to output file (with standard API key)
```java
java -classpath ".;../lib/*" AnnotateText <text to anotate> > <outputfile> | type <outputfile>
java -classpath ".;../lib/*" AnnotateText "Cancer is a group of diseases involving abnormal cell growth with the potential to invade or spread to other parts of the body" > "..\output\exampleOutput1.txt" | type "..\output\exampleOutput1.txt"
```

3. Plain text to output file with own API key
```java
java -classpath ".;../lib/*" AnnotateTextAdvanced <text to anotate> <API key> > <outputfile> | type <outputfile>
java -classpath ".;../lib/*" AnnotateTextAdvanced "Cancer is a group of diseases involving abnormal cell growth with the potential to invade or spread to other parts of the body" "ddbc0f31-8c9e-4a77-bd04-b146ae01baa0"  > "..\output\exampleOutput2.txt" | type "..\output\exampleOutput2.txt"
```

4. Text from .txt file (with standard API key, output in console)
```java
java -classpath ".;../lib/*" AnnotateText `cat <file>`
java -classpath ".;../lib/*" AnnotateText `cat ../examples/exampleInput.txt`
```

*Commands above processed on Windows - similarly on Linux*