# Part 1 
## code for StringServer
```java
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String information="";

    public String handleRequest(URI url) {
        if(url.getPath().equals("/")){
            return information;
        }
        else if(url.getPath().contains("/add-message")){
            String[] parameters=url.getQuery().split("=");
            if(parameters[0].equals("s")){
                information=information+"\n"+parameters[1];
                return information;
            }
        }
        return "404 Not Found!";
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }
        int port = Integer.parseInt(args[0]);
        Server.start(port, new Handler());
    }
}
```

## Screenshots of using /add-message
![Execute](https://user-images.githubusercontent.com/117802747/214969694-82553585-8183-4494-94a8-8bf52cb81421.png)
![Execute2](https://user-images.githubusercontent.com/117802747/214969714-d7e1b74a-859b-4cc3-9d67-ebf6ee63e2db.png)

## methods called in my code
The handleRequest method in the Handler class and the main method in the StringServer class are called.

## relevant arguments and values of relevant fields
For the handleRequest method, I passed in a series of strings as arguments, including "Hello", "How are you", "I am fine", "Thanks", and "That's Great".

I have one variable(information) as the value of the field.

## how do the values change
Each time I called the method, a new line ("\n") and the string I entered were added to the variable information.

# Part 2
## failure-inducing input 
```java
@Test
public void testReverseInPlaceMy1() {
    int[] input1 = {1,2,3,4,5};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{5,4,3,2,1}, input1);
}
```    

## input that doesn’t induce a failure
```java
@Test 
public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
}
```
## symptom
![image](https://user-images.githubusercontent.com/117802747/214973688-9b43853c-3670-4db0-8d46-d0ed0d18ad30.png)

## bug
### before the change
```java
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
        arr[i] = arr[arr.length - i - 1];
    }
}
```

### after the change
```java
static void reverseInPlace(int[] arr) {
    int[] temp = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
        temp[arr.length - 1 - i] = arr[i];
    }
    for(int i = 0; i<arr.length;i++){
        arr[i] = temp[i];
    }
}
```
## why the fix address the issue
  For the method reverseInPlace(), the method replaced the ith element at the front with the ith element at the end. After half way through, the method is no longer correct since the original elements have already been replaced.
  In order to address this problem, I create a new array(temp), put the elements in arr in reverse order into temp, and then copy each element in temp into arr. In this case, all the original elements have been preserved.

# Part 3
In week 2 and 3, I obtained a concrete understanding of building my own server. To begin with, I need a handler that implements URLHandler interface, 
which takes a URL as input and respond with the text of a web page. In addition, I need a Server class that takes a URLHandler and starts up the server that listens for incoming connections.
Through utilizing those codes, I was able to build not only servers of all kinds, but even a mini Search Engine! 
