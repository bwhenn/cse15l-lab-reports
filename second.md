## Part 1
#### StringServer Code 
```
import java.io.IOException;
import java.net.URI;


class Handler implements URLHandler {
    String showString = "";
    int count = 1; 

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Welcome");
        }
        else if (url.getPath().contains("/add-message")) {
            String[] params = url.getQuery().split("=");
            if (params[0].equals("s")) {
                showString = showString.concat(String.format("%d: ", count));
                showString = showString.concat(params[1]);
                showString = showString.concat("\n");
                count++;
            }
            return showString;
        }
        return "404 not Found!";
    }
}

class StringServer {
    public static void main(String args[]) throws IOException {
        if (args.length == 0) {
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return; 
        }
        int port = Integer.parseInt(args[0]);
        Server.start(port, new Handler());
    }
}
```

In this image, the variables `showString` (string) and `count` (int) are initialized when the server is first started during creation of the new  `Handler` object in  `main`. When we update the URL with `<domain>/add-message?s=There`, the string "there" is concatenaed to `showString` before the incremented  `count` variable. Then, a new line character is concatenated so that the next string to be added using a call to . 
## Part 2

## Part 3


