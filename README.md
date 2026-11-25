//Exp 1:
git init
git status
git config --global user.name "Shreeraksha277"
git config --global user.email "shreeraksha8147@gmail.com"
git config --global user.name
git config --global user.email
git add sample.txt
git add .
git commit -m "main"
git branch //to check the number of branch
git branch b1
git checkout b1
//make the changes inn the file
git add .
git commit -m "b1" // do same for branch b2
git merge b1
git merge b2

//Exp2:
dependency :
<dependency>
    <groupId>com.googlecode.json-simple</groupId>
    <artifactId>json-simple</artifactId>
    <version>1.1.1</version>
</dependency>
source code:
package javaapplication;

import java.io.FileReader;
import java.io.IOException;
import org.json.simple.JSONObject;
import org.json.simple.parser.JSONParser;
import org.json.simple.parser.ParseException;

public class ReadJSON {

    public static void main(String[] args)
            throws IOException, ParseException {

        JSONParser jsonParser = new JSONParser();

        FileReader reader =
                new FileReader("student.json");

        Object obj = jsonParser.parse(reader);

        JSONObject studentObj = (JSONObject) obj;

        String usn = (String) studentObj.get("USN");
        String name = (String) studentObj.get("name");

        System.out.println("USN: " + usn);
        System.out.println("Name: " + name);

        reader.close();
    }
}

student.json:
{
"USN":"4vv24cs272"
"name":"shreeraksha"
}
