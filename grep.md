 Examples:
 
 ```sh
curl Some.XML.file | grep -Pzo "(?s)<high_url>.+?<wstrm>\K(.+?)(?=</ws)"
 ```
